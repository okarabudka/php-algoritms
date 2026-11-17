# PHP Algorithms Exercises

A set of classic algorithm and data structure exercises implemented in PHP, each covered by PHPUnit tests.

## Context

Learning project built in July 2023 to prepare for algorithm questions in technical interviews.

## Features

Exercises in `exercises/`, one class per topic:

- Strings: [Anagram](./exercises/Anagram/Anagram.php), [Capitalize](./exercises/Capitalize/Capitalize.php), [MaxChar](./exercises/MaxChar/MaxChar.php), [Palindrome](./exercises/Palindrome/Palindrome.php), [Reverse](./exercises/Reverse/Reverse.php), [Vowels](./exercises/Vowels/Vowels.php)
- Arrays and numbers: [ArrayGroup](./exercises/ArrayGroup/ArrayGroup.php), [Fibonacci](./exercises/Fibonacci/Fibonacci.php), [FizzBuzz](./exercises/FizzBuzz/FizzBuzz.php), [MaxSubArraySum](./exercises/MaxSubArraySum/MaxSubArraySum.php), [Numbers](./exercises/Numbers/Numbers.php), [Spiral](./exercises/Spiral/Spiral.php)
- Printing patterns: [Ladder](./exercises/Ladder/Ladder.php), [Pyramid](./exercises/Pyramid/Pyramid.php)
- Searching: [Search](./exercises/Search/Search.php) (linear, binary, naive string search)
- Sorting: [Sort](./exercises/Sort/Sort.php) (bubble, selection, insertion, merge, quick sort in two variants, radix)
- Data structures: [Stack](./exercises/Stack/Stack.php), [Queue](./exercises/Queue/Queue.php), [QueueFromStacks](./exercises/QueueFromStacks/QueueFromStacks.php), [Tree](./exercises/Tree/Tree.php), [BinarySearchTree](./exercises/BinarySearchTree/BinarySearchTree.php), [MaxHeap](./exercises/MaxHeap/MaxHeap.php)
- Event emitter: [Events](./exercises/Events/Events.php) (`on`, `fire`, `off`)

## Tech stack

- PHP 8.1 (Docker image `php:8.1-apache`)
- PHPUnit 9.5, `spatie/phpunit-watcher`, `codedungeon/phpunit-result-printer`
- Composer, Docker Compose

## Architecture

- `exercises/<Name>/<Name>.php`: solution, namespace `Exercises\`
- `tests/<Name>/<Name>Test.php`: tests, namespace `Tests\`
- `tests/GetReflectionMethod.php`: helper for testing non-public methods via reflection

## Getting started

```bash
cp .env.example .env
docker compose up -d
docker compose exec app composer install
```

## Testing

```bash
docker compose exec app ./vendor/bin/phpunit
```

Or run the tests on every file change:

```bash
docker compose exec app ./vendor/bin/phpunit-watcher watch
```

## Status

Finished learning project (2023), not maintained.

## License

MIT, see [LICENSE](LICENSE).
