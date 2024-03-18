% Define the graph with edges and their costs
edge(a, b, 4).
edge(a, c, 2).
edge(b, d, 5).
edge(c, e, 3).
edge(c, f, 6).
edge(d, g, 1).
edge(e, g, 7).
edge(f, g, 9).

% Best First Search Algorithm
best_first_search(Start, Goal, Path) :-
    best_first_search(Start, Goal, [Start], 0, Path).

% Base case: Goal is reached
best_first_search(Goal, Goal, Path, _, Path).

% Recursive case: Search for the goal node
best_first_search(Current, Goal, Visited, Cost, Path) :-
    edge(Current, Next, EdgeCost),
    \+ member(Next, Visited), % Ensure Next has not been visited yet
    NewCost is Cost + EdgeCost,
    best_first_search(Next, Goal, [Next|Visited], NewCost, Path).

% Helper predicate to initiate the search
search(Start, Goal) :-
    best_first_search(Start, Goal, Path),
    reverse(Path, PathInOrder),
    write('Path from '), write(Start), write(' to '), write(Goal), write(': '), write(PathInOrder).
E
