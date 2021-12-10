---
id: use-media-query
title: useMediaQuery
---

`useMediaQuery` is a custom hook used to help detect whether a single media query or multiple media queries individually match. React Native does not natively support media queries, so `useMediaQuery` is still limited.

## Import

```jsx
import { useMediaQuery } from 'native-base';
```

## Example

### max-height

```SnackPlayer name=useMediaQuery%20Usage(max-height)
import React from "react";
import { Text, useMediaQuery, NativeBaseProvider, Center } from "native-base";

function UseMediaQueryExample() {
  const [isSmallScreen] = useMediaQuery({ minHeight: 280, maxHeight: 480 });
  return (
    <Box>
      {isSmallScreen ? (
        <Box
          rounded="lg"
          overflow="hidden"
          width="72"
          borderWidth="1"
          shadow={1}
          _light={{ backgroundColor: 'gray.50', borderColor: 'coolGray.200' }}
          _dark={{ borderColor: 'coolGray.600', backgroundColor: 'gray.700' }}
        >
          <Box>
            <AspectRatio ratio={16 / 9}>
              <Image
                source={{
                  uri:
                    'https://www.holidify.com/images/cmsuploads/compressed/Bangalore_citycover_20190613234056.jpg',
                }}
                alt="image"
              />
            </AspectRatio>
            <Center
              bg="violet.500"
              _text={{ color: 'white', fontWeight: '700', fontSize: 'xs' }}
              position="absolute"
              bottom={0}
              px="3"
              py="1.5"
            >
              PHOTOS
            </Center>
          </Box>
          <Stack p="4" space={3}>
            <Stack space={2}>
              <Heading size="md" ml="-1">
                The Garden City
              </Heading>
              <Text
                fontSize="xs"
                _light={{ color: 'violet.500' }}
                _dark={{ color: 'violet.300' }}
                fontWeight="500"
                ml="-0.5"
                mt="-1"
              >
                The Silicon Valley of India.
              </Text>
            </Stack>
            <Text fontWeight="400">
              Bengaluru (also called Bangalore) is the center of India's
              high-tech industry. The city is also known for its parks and
              nightlife.
            </Text>
            <HStack
              alignItems="center"
              space={4}
              justifyContent="space-between"
            >
              <HStack alignItems="center">
                <Text color="gray.500" fontWeight="400">
                  6 mins ago
                </Text>
              </HStack>
            </HStack>
          </Stack>
        </Box>
      ) : (
        <HStack
          rounded="lg"
          overflow="hidden"
          shadow={1}
          _light={{ backgroundColor: 'gray.50' }}
          _dark={{ backgroundColor: 'gray.700' }}
        >
          <Stack p="2" pt="3" flex="2" space={1}>
            <Stack space={2}>
              <Heading size="md" ml="-1">
                The Garden City
              </Heading>
              <Text
                fontSize="xs"
                _light={{ color: 'violet.500' }}
                _dark={{ color: 'violet.300' }}
                fontWeight="500"
                ml="-0.5"
                mt="-1"
              >
                The Silicon Valley of India.
              </Text>
            </Stack>
            <Text fontSize="xs" fontWeight="400">
              Bengaluru (also called Bangalore) is the center of India's
              high-tech industry. The city is also known for its parks and
              nightlife.
            </Text>
            <HStack
              alignItems="center"
              space={4}
              justifyContent="space-between"
            >
              <HStack alignItems="center">
                <Text
                  _dark={{ color: 'warmGray.200' }}
                  fontSize="xs"
                  color="gray.500"
                  fontWeight="400"
                >
                  6 mins ago
                </Text>
              </HStack>
            </HStack>
          </Stack>
        </HStack>
      )}
    </Box>
  );
}
export default function () {
  return (
    <NativeBaseProvider>
      <Center flex={1}>
        <UseMediaQueryExample />
      </Center>
    </NativeBaseProvider>
  );
}
```

### min-width

```SnackPlayer name=useMediaQuery%20Usage(min-width)
import React from "react";
import { Text, useMediaQuery, NativeBaseProvider, Center } from "native-base";

function UseMediaQueryExample() {
  const [isSmallScreen] = useMediaQuery({ minWidth: 280 });
  return (
    <Box>
      {isSmallScreen ? (
        <Box
          rounded="lg"
          overflow="hidden"
          width="72"
          borderColor="coolGray.200"
          borderWidth="1"
          _dark={{ borderColor: 'coolGray.600', backgroundColor: 'gray.700' }}
          shadow={2}
          _light={{ backgroundColor: 'gray.50' }}
        >
          <Box>
            <AspectRatio ratio={16 / 9}>
              <Image
                source={{
                  uri:
                    'https://www.holidify.com/images/cmsuploads/compressed/Bangalore_citycover_20190613234056.jpg',
                }}
                alt="image"
              />
            </AspectRatio>
            <Center
              bg="violet.500"
              _text={{ color: 'white', fontWeight: '700', fontSize: 'xs' }}
              position="absolute"
              bottom={0}
              px="3"
              py="1.5"
            >
              PHOTOS
            </Center>
          </Box>
          <Stack p="4" space={3}>
            <Stack space={2}>
              <Heading size="md" ml="-1">
                The Garden City
              </Heading>
              <Text
                fontSize="xs"
                _light={{ color: 'violet.500' }}
                _dark={{ color: 'violet.300' }}
                fontWeight="500"
                ml="-0.5"
                mt="-1"
              >
                The Silicon Valley of India.
              </Text>
            </Stack>
            <Text fontWeight="400">
              Bengaluru (also called Bangalore) is the center of India's
              high-tech industry. The city is also known for its parks and
              nightlife.
            </Text>
            <HStack
              alignItems="center"
              space={4}
              justifyContent="space-between"
            >
              <HStack alignItems="center">
                <Text color="gray.500" fontWeight="400">
                  6 mins ago
                </Text>
              </HStack>
            </HStack>
          </Stack>
        </Box>
      ) : (
        <HStack
          rounded="lg"
          overflow="hidden"
          shadow={1}
          _light={{ backgroundColor: 'gray.50' }}
          _dark={{ backgroundColor: 'gray.700' }}
        >
          <Stack p="2" pt="3" flex="2" space={1}>
            <Stack space={2}>
              <Heading size="md" ml="-1">
                The Garden City
              </Heading>
              <Text
                fontSize="xs"
                _light={{ color: 'violet.500' }}
                _dark={{ color: 'violet.300' }}
                fontWeight="500"
                ml="-0.5"
                mt="-1"
              >
                The Silicon Valley of India.
              </Text>
            </Stack>
            <Text fontSize="xs" fontWeight="400">
              Bengaluru (also called Bangalore) is the center of India's
              high-tech industry. The city is also known for its parks and
              nightlife.
            </Text>
            <HStack
              alignItems="center"
              space={4}
              justifyContent="space-between"
            >
              <HStack alignItems="center">
                <Text
                  _dark={{ color: 'warmGray.200' }}
                  fontSize="xs"
                  color="gray.500"
                  fontWeight="400"
                >
                  6 mins ago
                </Text>
              </HStack>
            </HStack>
          </Stack>
        </HStack>
      )}
    </Box>
  );
}
export default function () {
  return (
    <NativeBaseProvider>
      <Center flex={1}>
        <UseMediaQueryExample />
      </Center>
    </NativeBaseProvider>
  );
}
```

### orientation

```SnackPlayer name=useMediaQuery%20Usage(orientation)
import React from "react";
import { Text, useMediaQuery, NativeBaseProvider, Center } from "native-base";

function UseMediaQueryExample() {
 const [isLandScape, isPortrait] = useMediaQuery([
    { orientation: 'landscape' },
    { orientation: 'portrait' },
  ]);
  return (
    <Box>
      {isPortrait ? (
        <Box
          rounded="lg"
          overflow="hidden"
          width="72"
          shadow={1}
          borderWidth="1"
          _light={{ backgroundColor: 'gray.50', borderColor: 'coolGray.200' }}
          _dark={{ borderColor: 'coolGray.600', backgroundColor: 'gray.700' }}
        >
          <Box>
            <AspectRatio ratio={16 / 9}>
              <Image
                source={{
                  uri:
                    'https://www.holidify.com/images/cmsuploads/compressed/Bangalore_citycover_20190613234056.jpg',
                }}
                alt="image"
              />
            </AspectRatio>
            <Center
              bg="violet.500"
              _text={{ color: 'white', fontWeight: '700', fontSize: 'xs' }}
              position="absolute"
              bottom={0}
              px="3"
              py="1.5"
            >
              PHOTOS
            </Center>
          </Box>
          <Stack p="4" space={3}>
            <Stack space={2}>
              <Heading size="md" ml="-1">
                The Garden City
              </Heading>
              <Text
                fontSize="xs"
                _light={{ color: 'violet.500' }}
                _dark={{ color: 'violet.300' }}
                fontWeight="500"
                ml="-0.5"
                mt="-1"
              >
                The Silicon Valley of India.
              </Text>
            </Stack>
            <Text fontWeight="400">
              Bengaluru (also called Bangalore) is the center of India's
              high-tech industry. The city is also known for its parks and
              nightlife.
            </Text>
            <HStack
              alignItems="center"
              space={4}
              justifyContent="space-between"
            >
              <HStack alignItems="center">
                <Text color="gray.500" fontWeight="400">
                  6 mins ago
                </Text>
              </HStack>
            </HStack>
          </Stack>
        </Box>
      ) : (
        <></>
      )}
      {isLandScape ? (
        <HStack
          rounded="lg"
          overflow="hidden"
          shadow={1}
          _light={{ backgroundColor: 'gray.50' }}
          _dark={{ backgroundColor: 'gray.700' }}
        >
          <Stack p="2" pt="3" flex="2" space={1}>
            <Stack space={2}>
              <Heading size="md" ml="-1">
                The Garden City
              </Heading>
              <Text
                fontSize="xs"
                _light={{ color: 'violet.500' }}
                _dark={{ color: 'violet.300' }}
                fontWeight="500"
                ml="-0.5"
                mt="-1"
              >
                The Silicon Valley of India.
              </Text>
            </Stack>
            <Text fontSize="xs" fontWeight="400">
              Bengaluru (also called Bangalore) is the center of India's
              high-tech industry. The city is also known for its parks and
              nightlife.
            </Text>
            <HStack
              alignItems="center"
              space={4}
              justifyContent="space-between"
            >
              <HStack alignItems="center">
                <Text
                  _dark={{ color: 'warmGray.200' }}
                  fontSize="xs"
                  color="gray.500"
                  fontWeight="400"
                >
                  6 mins ago
                </Text>
              </HStack>
            </HStack>
          </Stack>
        </HStack>
      ) : (
        <></>
      )}
    </Box>
  );
}
export default function () {
  return (
    <NativeBaseProvider>
      <Center flex={1}>
        <UseMediaQueryExample />
      </Center>
    </NativeBaseProvider>
  );
}
```

## Return value

The `useMediaQuery` hook returns an array of booleans, indicating whether the given query matches or queries match.

Why an array? `useMediaQuery` accepts both an object and an array of object, but will always return an array. This way, you can combine multiple media queries which will be individually matched in a single call. The options to use are still limited to `maxWidth`, `minWidth`, `maxHeight`, `minHeight`, `orientation`.