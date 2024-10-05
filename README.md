# Calculator

questions = [
  [
    "Which of the following is the branch of Artificial Intelligence?", "Machine Learning"
    ,"Cyber forensics", "Full-Stack Developer", "Network Design", 1
  ],
  [
    " Which of the following is a component of Artificial Intelligence?", "Learning", "Training", "Designing",
    "Puzzling", 1
  ],
  [
    "Which of the following is not the commonly used programming language for Artificial Intelligence?","Perl", "Java" ,"PROLOG",
"LISP", 1
  ],



  [
   " Which of the following is an example of artificial intelligent agent/agents?","Autonomous Spacecraft","Human"
,"Robot"
,"All of the mentioned"

],
  [
    "Which branch of AI enables machines to learn from data without being explicitly programmed?", "Natural Language Processing (NLP)","Robotics","Machine Learning","Computer Vision",3
  ],
  [
    "Which AI branch focuses on understanding and generating human language?", "Robotics","Computer Vision","Natural Language Processing (NLP)","Machine Learning",3
  ],
  [
    "What type of learning allows AI agents to interact with their environment and learn through trial and error?", "Supervised Learning","Unsupervised Learning","Reinforcement Learning","Deep Learning", 3
 ],
  [
    "Which industry utilizes AI for medical diagnosis, personalized treatment plans, and drug discovery?", "FinanceHealthcare","Transportation","Education", 2
  ],
  [
    "Which AI application is used to handle customer queries and improve customer support?", "Natural Language Processing (NLP)","Computer Vision","Robotics","Chatbots and Virtual Assistants" , 4
  ],
  [
      " Which of the following is not an application of artificial intelligence?", "Face recognition system"
,"Chatbots","LIDAR","DBMS" ,4
   ]

]

levels = [1000, 2000, 3000, 5000, 10000, 20000, 40000, 80000, 100000, 200000]
Score = 0
for i in range(0, len(questions)):

  question = questions[i]
  print(f"\n\nQuestion for Score {levels[i]}")
  print(f"1. {question[1]}              2. {question[2]} ")
  print(f"3. {question[3]}          4. {question[4]} ")
  reply = int(input("Enter your answer (1-4) or  0 to quit:\n" ))
  if (reply == 0):
    Score = levels[i-1]
    break
  if(reply == question[-1]):
    print(f"Correct answer, you have won Rs. {levels[i]}")
    if(i == 4):
      Score = 10000
    elif(i == 9):
      Score = 200000
    elif(i == 14):
      Score = 10000000
  else:
    print("Wrong answer!")
    break

print(f"Your total socre is {Score}")
