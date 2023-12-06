1. Introduction
    What is Artificial Intelligence (AI)?

    AI, or Artificial Intelligence, is a branch of computer science focused on creating systems that can perform tasks that would normally require human intelligence. These tasks range from understanding natural language, recognizing patterns, making decisions, and learning from experience. AI is a broad field with numerous subfields, each with its unique objectives and specializations. Check out our full guide, What is AI? to find out more. You can also explore how AI is different from machine learning in a separate article. 

    What are the different types of artificial intelligence?

    As AI grows in popularity, the technology is discussed in various ways. To simplify the remainder of the article, it’s important to look at the different types of AI. AI can be categorized into three levels based on its capabilities:

    Artificial Narrow Intelligence (ANI): This is the most common form of AI we interact with today. ANI is designed to perform a single task, like voice recognition or recommendations on streaming services.
    Artificial General Intelligence (AGI): An AI with AGI possesses the ability to understand, learn, adapt, and implement knowledge across a wide range of tasks at a human level. While large language models and tools such as ChatGPT have shown the ability to generalize across many tasks—as of 2023, this is still a theoretical concept.
    Artificial Super Intelligence (ASI): The final level of AI, ASI, refers to a future scenario where AI surpasses human intelligence in nearly all economically valuable work. This concept, while intriguing, remains largely speculative.

2. Intelligent Agents
    a. Agents
        - An agent is an entity that
            -> Perceives through sensors (eg. cameras, infrared sensors)
            -> Acts through effectors (eg. motors)
   
    b. Rational Agents
        - Rational Agent is one that does the right thing
        - Rational action is an action that maximises the expected value of an objective performance measure given the percept sequence
        - Rationality depends on the following:
            1. Performance measure
            2. Percept sequence
            3. Built-in knowledge of the environment
            4. Agent's range of actions
    
    c. Types of Environment
        - Accessible vs Inaccessible: Can the agent's sensors give it access to the full and complete state of the environment?
        - Deterministic vs Non-deterministic: Can the next state of action be determined by the current state and actions takes by the agent?
        - Episodic vs Sequential: Are the future states affected by previous states?
        - Static vs Dynamic: Does the environment change as the agent is perceiving and making a decision?
        - Discrete or Continuous: Affected by a single variable or multiple variables?
    
    d. Design of Problem-Solving Agent
    Problem-solving agents are intelligent entities that are capable of analyzing situation, identifying goals and devising effective strategies to achieve these goals. Designing these agents involves a structures approach that encompasses four key steps:
        1. Goal formulation - Clearly define the desired outcome, the specific objective tha the agent strives to attain
        2. Problem formulation - Construct a formal representation of the problem, specifying the initial state, permissible actions, and the conditions that indicate a successful solution
        3. Solution - Devising a sequence of legal actions, a step-by-step plan that guides the agent from the initial state to the desired goal state
        4. Search - Employing a search algorithm, a systematic procedure for exploring the space of possible actions and identifying an optimal or satisfactory solution

    Effectively designing problem-solving agents require careful consideration of these steps and the appropriate selection of search algorithm based on the agent's knowledge and the problem characteristics.

3. Search Algorithms
    Search algorithms are a fundamental component of artificial intelligence, enabling agents to navigate complex problem spaces and find solutions to challenging tasks. At the heart of search algorithms lie the concept of exploring the state space.

    - State Space
    The state space represents the collection of all possible configurations or situations that the agent can encounter in its environment. Each state is represented by a node in the state space, and the connections between nodes represent the possible actions that the agent can take to transition from one state to another.

    - Expanding Nodes
    The core operation of search algorithms is to expand nodes. Expanding a node involves generating its successors, which represent the new states that the agent can reach by taking a single action from the current node.

    - Frontier and Explored Set
    To maintain an organized search process, two data structures are commonly used:

    -> Frontier: The frontier, also known as the open set, is a collection of nodes that have been explored but not yet expanded. It represents the candidate nodes for expansion in the next iteration of the search algorithm.

    -> Explored Set: The explored set, also known as the closed set, is a collection of nodes that have already been expanded. It maintains a record of visited states to avoid revisiting them and ensure efficient exploration.

    There are multiple search strategies and a strategy is defined as the order of node expansion. Strategies can either be uninformed or informed. Strategies are evaluated using the following metrics:
        1. Completeness -> Is a solution found if it exists?
        2. Time complexity -> How long does it take?
        3. Space Complexity -> How much memory does it take?
        4. Optimal -> Is the solution found in the best (least-cost)?

    Uninformed Search Strats use only information available in the problem definition. 
        The following are some expamples of uninformed search strats:
        - Breadth-first search (BDS)
        - Uniform-cost search (UCS)
        - Depth-first search (DFS)
        - Iterative Deepending search (IDS)
    Uniformed search strategies are systematic in generating of new states but are inefficient (exponential space and time complexity)

    Informed Search strats use problem specific knowledge to guide the search and they are usually more efficient. 
        The following are some examples of informed search strats:
        - A-star Search / A* Search
        - Greedy BFS
    Informed search strategies use an evaluation function to estimate the "desirability" of each node. So what is this evaluation function?
    
    Evaluation function consists of path-cost function and a heuristic function.
        - Path-cost function g(n)
            -> Cost from initial state to current state n
            -> Information of the cost toward the goal is not required
        - Heuristic function h(n)
            -> Estimated cost of the cheapest pth from n to a goal state
                ~ Exact cost cannot be determined
            -> Depends only on the state at that node
            -> h(n) is not larger than the real cost (admissible)

    The various search strategies can also be categorised based on the mentioned evaluation metrics.

    1. Completeness:
        - Refers to the ability to guarantee to finding a solution if it exists. These algorithms will exhaustively explore the state space until a solution is found. The following are some examples of complete search strategies:
        a. BFS
        b. DFS
        c. A* Search with heuristic

    2. Time Complexity:
        - Refers to the amount of time it takes for an algorithm to find a solution, typically represented in terms of the number of nodes generated/expanded. A search strategy with lower time complexity is more efficient and faster at finding solutions.
        The following are some examples of time-efficient strategies:
        a. A* strategies
        b. Greedy BFS
    
    3. Space Complexity:
        - Refers to the maximum amount of memory required by a search algorithm during execution. A search strategy with lower space complexity means it is more memory-efficient and can handle larger problem spaces. 
        The following are some examples of space-efficient strategies:
        a. DFS
    
    4. Optimality:
        - Refers to the ability to consistently find the best or least-cost solution to a problem. An optimal search algorithm guarantees that the solution found is the best possible solution.
        The following are some examples of optimal search strategies:
        a. A* search
        b. UCS
        c. IDS

    However, choosing a search algorithm is not that easy as there are trade-offs between search strategies. For instance, complete search algorithms like BFS and DFS are guaranteed to find a solution if one exists but may have high time and space complexity. Informed search algorithms like A* and Greedy Best-First Search can be more time and space efficient but may not always find the optimal solution.

    The choice of search strategy depends on the specific problem being solved and the desired balance between completeness, time complexity, space complexity, and optimality. In some cases, a trade-off may be necessary to achieve a balance between these factors.

    Here are some resources on the searches mentioned in this chapter:

    - Depth-First Search
        -> Video: https://m.youtube.com/watch?v=iaBEKo5sM7w
        -> Article: https://en.wikipedia.org/wiki/Depth-first_search
        -> Visualization: https://visualgo.net/en/dfsbfs
    
    - Breadth-First Search
        -> Video: https://m.youtube.com/watch?v=HZ5YTanv5QE
        -> Article: https://stackoverflow.com/questions/15990639/find-shortest-path-between-two-articles-in-english-wikipedia-in-python
        -> Visualization: https://visualgo.net/en/dfsbfs

    - A* Search
        -> Video: https://www.youtube.com/watch?v=dYeUNdMtBdY
        -> Article: https://en.wikipedia.org/wiki/Star

    - Iterative Deepening Search (IDS):
        -> Video: https://m.youtube.com/watch?v=Y85ECk_H3h4
        -> Article: https://en.wikipedia.org/wiki/Iterative_deepening_depth-first_search

    - Iterative Cost Search:
        -> Article: https://en.wikipedia.org/wiki/Search_algorithm

    - Greedy Best-First Search:
        -> Video: https://m.youtube.com/watch?v=dv1m3L6QXWs
        -> Article: https://www.geeksforgeeks.org/greedy-best-first-search-algorithm/
        -> Visualization: https://m.youtube.com/watch?v=dv1m3L6QXWs
        
    - Uniform Cost Search:
        -> Video: https://m.youtube.com/watch?v=dRMvK76xQJI
        -> Article: https://gmarti.gitlab.io/quant/2023/05/07/wikipedia-network-companies-sentence-transformers.html

    - Additional Search Algorithms:
        -> Beam Search: https://en.wikipedia.org/wiki/Beam_search
        -> Bidirectional Search: https://en.wikipedia.org/wiki/Bidirectional_search
        -> Hill Climbing: https://en.wikipedia.org/wiki/Hill_climbing
        -> Dynamic Programming: https://en.wikipedia.org/wiki/Dynamic_programming


4. Constraint Satisfaction
    a.
5. Markov Decision Process
    a.
6. Reinforcement Learning
    a.
7. Game Theory
    a.
8. Logical Agent
    a.
9. Propositional Logic
    a.
10. First Order Logic
    a.
11. Default Logic
    a.
12. Fuzzy Logic
    a.

OTHER NOTEWORTHY RESOURCE MENTIONS:
- https://www.youtube.com/watch?v=0IAPZzGSbME
- https://medium.com/machine-learning-in-practice/my-curated-list-of-ai-and-machine-learning-resources-from-around-the-web-9a97823b8524
- https://www.interestedinai.com/post/best-free-resources-to-learn-artificial-intelligence
- https://www.mltut.com/best-resources-to-learn-artificial-intelligence/
- https://ocw.mit.edu/courses/6-006-introduction-to-algorithms-spring-2020/