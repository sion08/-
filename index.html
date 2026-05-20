import tkinter as tk
from tkinter import messagebox

class DrugTycoonApp:
    def __init__(self, root):
        self.root = root
        self.root.title("신약 개발 퀴즈 타이쿤")
        self.root.geometry("600x550")
        self.root.configure(bg="#f0f8ff")

        # 게임 상태 변수
        self.initial_funds = 1000
        self.funds = self.initial_funds
        self.earned_funds = 0
        self.safety_score = 0             # 추가된 안전성 점수 변수
        self.required_safety_score = 30   # 신약 개발 성공을 위한 최소 안전성 점수 (3문제 정답 필요)
        self.current_q_idx = 0
        self.current_stage_idx = 0

        # 생명과학 I 퀴즈 데이터
        self.questions = [
            {
                "q": "1. [신약 타겟 발굴] 수많은 신약들은 우리 몸의 '물질대사'를 조절해 병을 치료합니다.\n이러한 반응 속도를 조절해주는 단백질인 '생체 촉매'는 무엇일까요?",
                "options": ["1. 호르몬", "2. 효소", "3. 비타민", "4. 무기염류"],
                "answer": 2
            },
            {
                "q": "2. [생명 활동] 세포가 포도당과 같은 영양소를 분해하여\n생명 활동에 필요한 에너지(ATP)를 얻는 과정은?",
                "options": ["1. 광합성", "2. 세포 호흡", "3. 소화 작용", "4. 혈액 순환"],
                "answer": 2
            },
            {
                "q": "3. [항생제 개발] 페니실린 같은 '항생제'를 이용해 치료할 수 있으며,\n결핵이나 식중독을 일으키는 단세포 생물 병원체는 무엇일까요?",
                "options": ["1. 바이러스", "2. 프라이온", "3. 세균(박테리아)", "4. 곰팡이"],
                "answer": 3
            },
            {
                "q": "4. [백신 연구] 질병 예방을 위해 독성을 약화시킨 병원체나 그 일부를\n미리 몸에 주사하여, 인공적으로 면역력을 기억하게 만드는 약품은?",
                "options": ["1. 항생제", "2. 진통제", "3. 백신", "4. 소화제"],
                "answer": 3
            },
            {
                "q": "5. [항원-항체 반응] 우리 몸이 만든 방어 물질인 '항체'가\n침입자인 '항원'과 자물쇠-열쇠처럼 짝이 맞을 때만 결합하는 현상은?",
                "options": ["1. 항원-항체 반응", "2. 알레르기 반응", "3. 혈액 응고 반응", "4. 염증 반응"],
                "answer": 1
            },
            {
                # 요청하신 대로 멘트를 삭제한 6번 문제
                "q": "6. [유전자 분석] 사람의 염색체 46개 중 성별에 관계없이\n공통으로 가지는 44개의 염색체는 무엇일까요?",
                "options": ["1. 상염색체", "2. 성염색체", "3. 상동 염색체", "4. 대립 유전자"],
                "answer": 1
            }
        ]

        # 신약 개발 투자 단계 데이터
        self.stages = [
            {"name": "기초 연구", "cost": 200},
            {"name": "동물 실험", "cost": 300},
            {"name": "임상시험", "cost": 500},
            {"name": "판매 허가", "cost": 400}
        ]

        # 화면 프레임 생성
        self.start_frame = tk.Frame(self.root, bg="#f0f8ff")
        self.quiz_frame = tk.Frame(self.root, bg="#f0f8ff")
        self.invest_frame = tk.Frame(self.root, bg="#f0f8ff")
        self.result_frame = tk.Frame(self.root, bg="#f0f8ff")

        # 각 화면 UI 구성
        self.create_start_screen()
        self.create_quiz_screen()
        self.create_invest_screen()
        self.create_result_screen()

        # 시작 화면 띄우기
        self.show_frame(self.start_frame)

    def show_frame(self, frame):
        """특정 프레임을 화면에 표시하는 함수"""
        self.start_frame.pack_forget()
        self.quiz_frame.pack_forget()
        self.invest_frame.pack_forget()
        self.result_frame.pack_forget()
        frame.pack(fill="both", expand=True)

    def create_start_screen(self):
        """시작 화면 구성"""
        tk.Label(self.start_frame, text="🧪 신약 개발 퀴즈 타이쿤 🧬", font=("Malgun Gothic", 24, "bold"), bg="#f0f8ff", fg="#2c3e50").pack(pady=40)
        
        desc_text = (
            "생명공학 퀴즈를 풀어 연구비와 안전성 점수를 획득하세요!\n"
            "정답을 맞히면 100만 원과 안전성 점수 10점이 지급됩니다.\n\n"
            "획득한 자금으로 [기초연구 -> 동물실험 -> 임상시험 -> 판매허가]\n"
            "단계를 거쳐 신약 개발을 성공시켜야 합니다.\n\n"
            f"⚠️ 주의: 최종 판매 허가를 받으려면 안전성 점수가\n최소 {self.required_safety_score}점 이상이어야 합니다!\n\n"
            "(초기 정부 지원금: 1,000만 원)"
        )
        tk.Label(self.start_frame, text=desc_text, font=("Malgun Gothic", 12), bg="#f0f8ff", justify="center", lineheight=1.5).pack(pady=15)
        
        tk.Button(self.start_frame, text="게임 시작하기", font=("Malgun Gothic", 14, "bold"), bg="#3498db", fg="white", 
                  width=15, height=2, command=lambda: self.show_frame(self.quiz_frame)).pack(pady=20)

    def create_quiz_screen(self):
        """퀴즈 화면 구성"""
        self.quiz_status_label = tk.Label(self.quiz_frame, text=f"💰 연구비: {self.funds}만 원  |  🛡️ 안전성: {self.safety_score}점", font=("Malgun Gothic", 14, "bold"), bg="#f0f8ff", fg="#e74c3c")
        self.quiz_status_label.pack(pady=20)

        self.q_label = tk.Label(self.quiz_frame, text="", font=("Malgun Gothic", 14), bg="#f0f8ff", justify="center", height=3)
        self.q_label.pack(pady=20)

        self.radio_var = tk.IntVar(value=0)
        self.radio_buttons = []
        
        for i in range(4):
            rb = tk.Radiobutton(self.quiz_frame, text="", variable=self.radio_var, value=i+1, font=("Malgun Gothic", 12), bg="#f0f8ff", anchor="w")
            rb.pack(fill="x", padx=100, pady=5)
            self.radio_buttons.append(rb)

        tk.Button(self.quiz_frame, text="정답 제출", font=("Malgun Gothic", 12, "bold"), bg="#2ecc71", fg="white", 
                  width=12, height=2, command=self.check_answer).pack(pady=30)

        self.update_quiz_ui()

    def create_invest_screen(self):
        """투자 및 경영 화면 구성"""
        tk.Label(self.invest_frame, text="📊 신약 연구 개발 (R&D)", font=("Malgun Gothic", 20, "bold"), bg="#f0f8ff", fg="#2c3e50").pack(pady=30)
        
        self.invest_status_label = tk.Label(self.invest_frame, text="", font=("Malgun Gothic", 16, "bold"), bg="#f0f8ff", fg="#e74c3c")
        self.invest_status_label.pack(pady=10)

        self.stage_label = tk.Label(self.invest_frame, text="", font=("Malgun Gothic", 16), bg="#f0f8ff")
        self.stage_label.pack(pady=20)

        self.invest_btn = tk.Button(self.invest_frame, text="투자하기", font=("Malgun Gothic", 14, "bold"), bg="#9b59b6", fg="white", 
                                    width=15, height=2, command=self.process_investment)
        self.invest_btn.pack(pady=30)

    def create_result_screen(self):
        """최종 결과 화면 구성"""
        tk.Label(self.result_frame, text="🎉 신약 개발 성공! 🎉", font=("Malgun Gothic", 24, "bold"), bg="#f0f8ff", fg="#e67e22").pack(pady=40)
        
        self.result_details = tk.Label(self.result_frame, text="", font=("Malgun Gothic", 14), bg="#f0f8ff", justify="center", lineheight=1.5)
        self.result_details.pack(pady=20)

        tk.Button(self.result_frame, text="게임 종료", font=("Malgun Gothic", 12, "bold"), bg="#95a5a6", fg="white", 
                  width=12, height=2, command=self.root.destroy).pack(pady=30)

    def update_quiz_ui(self):
        """현재 퀴즈 데이터를 화면에 업데이트"""
        q_data = self.questions[self.current_q_idx]
        self.q_label.config(text=q_data["q"])
        
        for i in range(4):
            self.radio_buttons[i].config(text=q_data["options"][i])
            
        self.radio_var.set(0) # 선택 없음 초기화
        self.quiz_status_label.config(text=f"💰 연구비: {self.funds}만 원  |  🛡️ 안전성: {self.safety_score}점")

    def check_answer(self):
        """사용자가 선택한 답안을 확인하고 보상 지급"""
        selected = self.radio_var.get()
        if selected == 0:
            messagebox.showwarning("경고", "보기를 선택해주세요!")
            return

        correct_answer = self.questions[self.current_q_idx]["answer"]
        
        if selected == correct_answer:
            self.funds += 100
            self.earned_funds += 100
            self.safety_score += 10  # 정답 시 안전성 점수 10점 추가
            messagebox.showinfo("정답!", "정답입니다!\n연구비 100만 원과 안전성 점수 10점을 획득했습니다.")
        else:
            messagebox.showerror("오답", "틀렸습니다.\n아쉽게도 보상을 획득하지 못했습니다.")

        self.current_q_idx += 1

        if self.current_q_idx < len(self.questions):
            self.update_quiz_ui()
        else:
            messagebox.showinfo("퀴즈 종료", "모든 퀴즈가 끝났습니다.\n이제 획득한 자금으로 신약 개발 투자를 시작합니다!")
            self.update_invest_ui()
            self.show_frame(self.invest_frame)

    def update_invest_ui(self):
        """투자 화면 정보 업데이트"""
        self.invest_status_label.config(text=f"보유 연구비: {self.funds}만 원  |  안전성: {self.safety_score}점")
        
        if self.current_stage_idx < len(self.stages):
            stage = self.stages[self.current_stage_idx]
            self.stage_label.config(text=f"다음 단계: {stage['name']}\n필요 자금: {stage['cost']}만 원")
            self.invest_btn.config(text=f"{stage['name']} 진행")
        else:
            self.show_final_result()

    def process_investment(self):
        """연구비 투자 처리 및 안전성 검증 로직"""
        stage = self.stages[self.current_stage_idx]
        cost = stage["cost"]

        if self.funds >= cost:
            # 판매 허가(최종) 단계 진입 시 안전성 점수 미달이면 실패 처리
            if stage["name"] == "판매 허가" and self.safety_score < self.required_safety_score:
                messagebox.showerror("판매 허가 실패", f"안전성 평가에서 탈락했습니다!\n\n"
                                                      f"현재 안전성: {self.safety_score}점 / 필요 안전성: {self.required_safety_score}점\n\n"
                                                      f"심각한 부작용 위험으로 인해 신약 출시가 무산되고 회사가 파산했습니다.")
                self.root.destroy()
                return

            self.funds -= cost
            messagebox.showinfo("투자 성공", f"[{stage['name']}] 단계를 성공적으로 완료했습니다!\n차감된 금액: {cost}만 원")
            self.current_stage_idx += 1
            self.update_invest_ui()
        else:
            messagebox.showerror("자금 부족", f"연구비가 부족합니다!\n필요 자금: {cost}만 원 / 현재 자금: {self.funds}만 원\n신약 개발에 실패하여 회사가 파산했습니다.")
            self.root.destroy()

    def show_final_result(self):
        """최종 성공 결과 출력"""
        company_value = self.funds * 10 + 5000 
        
        result_text = (
            f"엄격한 안전성 평가({self.safety_score}점)를 통과하고\n"
            f"혁신적인 신약이 시장에 출시되었습니다!\n\n"
            f"■ 초기 지원금: {self.initial_funds}만 원\n"
            f"■ 퀴즈로 번 연구비: {self.earned_funds}만 원\n"
            f"■ 남은 연구 자금: {self.funds}만 원\n\n"
            f"📈 평가된 제약 회사 가치: {company_value}만 원\n"
            f"🌍 사회적 기여도 등급: S등급 (수많은 생명을 구함)"
        )
        self.result_details.config(text=result_text)
        self.show_frame(self.result_frame)

if __name__ == "__main__":
    root = tk.Tk()
    app = DrugTycoonApp(root)
    root.mainloop()