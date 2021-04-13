---
title: Come enumerare i tipi di carattere
description: In questa panoramica viene illustrato come enumerare i tipi di carattere nella raccolta di tipi di carattere del sistema, in base al nome della famiglia.
ms.assetid: c1ec7721-2a30-4de3-b986-932f098228a6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9db05deb6b367f1392151ac8c12f2792d6e34f0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399312"
---
# <a name="how-to-enumerate-fonts"></a><span data-ttu-id="bd28a-103">Come enumerare i tipi di carattere</span><span class="sxs-lookup"><span data-stu-id="bd28a-103">How to Enumerate Fonts</span></span>

<span data-ttu-id="bd28a-104">In questa panoramica viene illustrato come enumerare i tipi di carattere nella raccolta di tipi di carattere del sistema, in base al nome della famiglia.</span><span class="sxs-lookup"><span data-stu-id="bd28a-104">This overview will show how to enumerate the fonts in the system font collection, by family name.</span></span>

<span data-ttu-id="bd28a-105">Questa panoramica è costituita dalle parti seguenti:</span><span class="sxs-lookup"><span data-stu-id="bd28a-105">This overview consists of the following parts:</span></span>

-   [<span data-ttu-id="bd28a-106">Passaggio 1: ottenere la raccolta di tipi di carattere di sistema.</span><span class="sxs-lookup"><span data-stu-id="bd28a-106">Step 1: Get the System Font Collection.</span></span>](#step-1-get-the-system-font-collection)
-   [<span data-ttu-id="bd28a-107">Passaggio 2: ottenere il conteggio delle famiglie di caratteri.</span><span class="sxs-lookup"><span data-stu-id="bd28a-107">Step 2: Get the Font Family Count.</span></span>](#step-2-get-the-font-family-count)
-   [<span data-ttu-id="bd28a-108">Creare un ciclo for.</span><span class="sxs-lookup"><span data-stu-id="bd28a-108">Make a For Loop.</span></span>](#make-a-for-loop)
    -   [<span data-ttu-id="bd28a-109">Passaggio 3: ottenere la famiglia di caratteri.</span><span class="sxs-lookup"><span data-stu-id="bd28a-109">Step 3: Get the Font Family.</span></span>](#step-3-get-the-font-family)
    -   [<span data-ttu-id="bd28a-110">Passaggio 4: ottenere i nomi di famiglia.</span><span class="sxs-lookup"><span data-stu-id="bd28a-110">Step 4: Get the Family Names.</span></span>](#step-4-get-the-family-names)
    -   [<span data-ttu-id="bd28a-111">Passaggio 5: trovare il nome delle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="bd28a-111">Step 5: Find the Locale Name.</span></span>](#step-5-find-the-locale-name)
    -   [<span data-ttu-id="bd28a-112">Passaggio 6: ottenere la lunghezza della stringa del nome della famiglia e della stringa.</span><span class="sxs-lookup"><span data-stu-id="bd28a-112">Step 6: Get the Length of the Family Name String Length and the String.</span></span>](#step-6-get-the-length-of-the-family-name-string-length-and-the-string)
-   [<span data-ttu-id="bd28a-113">Conclusione</span><span class="sxs-lookup"><span data-stu-id="bd28a-113">Conclusion</span></span>](#conclusion)
-   [<span data-ttu-id="bd28a-114">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="bd28a-114">Example Code</span></span>](#example-code)

## <a name="step-1-get-the-system-font-collection"></a><span data-ttu-id="bd28a-115">Passaggio 1: ottenere la raccolta di tipi di carattere di sistema.</span><span class="sxs-lookup"><span data-stu-id="bd28a-115">Step 1: Get the System Font Collection.</span></span>

<span data-ttu-id="bd28a-116">Usare il metodo [**GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) fornito dalla factory DirectWrite per restituire un [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) con tutti i tipi di carattere di sistema.</span><span class="sxs-lookup"><span data-stu-id="bd28a-116">Use the [**GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) method provided by the DirectWrite Factory to return an [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) with all of the system fonts in it.</span></span>


```C++
IDWriteFontCollection* pFontCollection = NULL;

// Get the system font collection.
if (SUCCEEDED(hr))
{
    hr = pDWriteFactory->GetSystemFontCollection(&pFontCollection);
}
```



## <a name="step-2-get-the-font-family-count"></a><span data-ttu-id="bd28a-117">Passaggio 2: ottenere il conteggio delle famiglie di caratteri.</span><span class="sxs-lookup"><span data-stu-id="bd28a-117">Step 2: Get the Font Family Count.</span></span>

<span data-ttu-id="bd28a-118">Ottenere quindi il conteggio delle famiglie di caratteri dalla raccolta dei tipi di carattere usando [**IDWriteFontCollection:: GetFontFamilyCount**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollection-getfontfamilycount).</span><span class="sxs-lookup"><span data-stu-id="bd28a-118">Next, get the font family count from the font collection by using [**IDWriteFontCollection::GetFontFamilyCount**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollection-getfontfamilycount).</span></span> <span data-ttu-id="bd28a-119">Questa operazione verrà usata per eseguire il ciclo di ogni famiglia di caratteri nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="bd28a-119">We'll use this to loop over each font family in the collection.</span></span>


```C++
UINT32 familyCount = 0;

// Get the number of font families in the collection.
if (SUCCEEDED(hr))
{
    familyCount = pFontCollection->GetFontFamilyCount();
}
```



## <a name="make-a-for-loop"></a><span data-ttu-id="bd28a-120">Creare un ciclo for.</span><span class="sxs-lookup"><span data-stu-id="bd28a-120">Make a For Loop.</span></span>


```C++
for (UINT32 i = 0; i < familyCount; ++i)
```



<span data-ttu-id="bd28a-121">Ora che si dispone della raccolta dei tipi di carattere e del conteggio dei tipi di carattere, i passaggi rimanenti eseguono il ciclo su ogni famiglia di caratteri, recuperando l'oggetto [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) ed eseguendo una query su di esso.</span><span class="sxs-lookup"><span data-stu-id="bd28a-121">Now that you have the font collection and the font count, the remaining steps loop over each font family, retrieving the [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) object and querying it.</span></span>

### <a name="step-3-get-the-font-family"></a><span data-ttu-id="bd28a-122">Passaggio 3: ottenere la famiglia di caratteri.</span><span class="sxs-lookup"><span data-stu-id="bd28a-122">Step 3: Get the Font Family.</span></span>

<span data-ttu-id="bd28a-123">Ottenere un oggetto [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) usando [**IDWriteFontCollection:: GetFontFamily**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollection-getfontfamily) e passandogli l'indice corrente, *i*.</span><span class="sxs-lookup"><span data-stu-id="bd28a-123">Get a [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) object by using [**IDWriteFontCollection::GetFontFamily**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollection-getfontfamily) and passing it the current index, *i*.</span></span>


```C++
IDWriteFontFamily* pFontFamily = NULL;

// Get the font family.
if (SUCCEEDED(hr))
{
    hr = pFontCollection->GetFontFamily(i, &pFontFamily);
}
```



### <a name="step-4-get-the-family-names"></a><span data-ttu-id="bd28a-124">Passaggio 4: ottenere i nomi di famiglia.</span><span class="sxs-lookup"><span data-stu-id="bd28a-124">Step 4: Get the Family Names.</span></span>

<span data-ttu-id="bd28a-125">Ottenere i nomi delle famiglie di caratteri usando [**IDWriteFontFamily:: GetFamilyNames**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfamily-getfamilynames).</span><span class="sxs-lookup"><span data-stu-id="bd28a-125">Get the font family names by using the [**IDWriteFontFamily::GetFamilyNames**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfamily-getfamilynames).</span></span> <span data-ttu-id="bd28a-126">Si tratta di un oggetto [**IDWriteLocalizedStrings**](/windows/win32/api/dwrite/nn-dwrite-idwritelocalizedstrings) .</span><span class="sxs-lookup"><span data-stu-id="bd28a-126">This is an [**IDWriteLocalizedStrings**](/windows/win32/api/dwrite/nn-dwrite-idwritelocalizedstrings) object.</span></span> <span data-ttu-id="bd28a-127">Può avere più versioni localizzate del nome della famiglia per la famiglia di caratteri.</span><span class="sxs-lookup"><span data-stu-id="bd28a-127">It can have multiple localized versions of the family name for the font family.</span></span>


```C++
IDWriteLocalizedStrings* pFamilyNames = NULL;

// Get a list of localized strings for the family name.
if (SUCCEEDED(hr))
{
    hr = pFontFamily->GetFamilyNames(&pFamilyNames);
}
```



### <a name="step-5-find-the-locale-name"></a><span data-ttu-id="bd28a-128">Passaggio 5: trovare il nome delle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="bd28a-128">Step 5: Find the Locale Name.</span></span>

<span data-ttu-id="bd28a-129">Ottenere il nome del tipo di carattere famliy nelle impostazioni locali desiderate usando il metodo [**IDWriteLocalizedStrings:: FindLocaleName**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-findlocalename) .</span><span class="sxs-lookup"><span data-stu-id="bd28a-129">Get the font famliy name in the locale you want by using the [**IDWriteLocalizedStrings::FindLocaleName**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-findlocalename) method.</span></span> <span data-ttu-id="bd28a-130">In questo caso, vengono recuperate e richieste prima le impostazioni locali predefinite.</span><span class="sxs-lookup"><span data-stu-id="bd28a-130">In this case, first the default locale is retrieved and requested.</span></span> <span data-ttu-id="bd28a-131">Se l'operazione non funziona, le impostazioni locali "en-US" sono richieste.</span><span class="sxs-lookup"><span data-stu-id="bd28a-131">If that does not work, the "en-us" locale is requested.</span></span> <span data-ttu-id="bd28a-132">Se una delle impostazioni locali specificate non viene trovata, questo esempio esegue semplicemente il fallback all'indice 0, ovvero le prime impostazioni locali disponibili.</span><span class="sxs-lookup"><span data-stu-id="bd28a-132">If either of the specified locales are not found, this example simply falls back to index 0, the first available locale.</span></span>


```C++
UINT32 index = 0;
BOOL exists = false;

wchar_t localeName[LOCALE_NAME_MAX_LENGTH];

if (SUCCEEDED(hr))
{
    // Get the default locale for this user.
    int defaultLocaleSuccess = GetUserDefaultLocaleName(localeName, LOCALE_NAME_MAX_LENGTH);

    // If the default locale is returned, find that locale name, otherwise use "en-us".
    if (defaultLocaleSuccess)
    {
        hr = pFamilyNames->FindLocaleName(localeName, &index, &exists);
    }
    if (SUCCEEDED(hr) && !exists) // if the above find did not find a match, retry with US English
    {
        hr = pFamilyNames->FindLocaleName(L"en-us", &index, &exists);
    }
}

// If the specified locale doesn't exist, select the first on the list.
if (!exists)
    index = 0;
```



### <a name="step-6-get-the-length-of-the-family-name-string-length-and-the-string"></a><span data-ttu-id="bd28a-133">Passaggio 6: ottenere la lunghezza della stringa del nome della famiglia e della stringa.</span><span class="sxs-lookup"><span data-stu-id="bd28a-133">Step 6: Get the Length of the Family Name String Length and the String.</span></span>

<span data-ttu-id="bd28a-134">Infine, ottenere la lunghezza della stringa del nome della famiglia utilizzando [**IDWriteLocalizedStrings:: GetStringLength**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-getstringlength).</span><span class="sxs-lookup"><span data-stu-id="bd28a-134">Finally, get the length of the family name string by using [**IDWriteLocalizedStrings::GetStringLength**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-getstringlength).</span></span> <span data-ttu-id="bd28a-135">Usare questa lunghezza per allocare una stringa sufficientemente grande da mantenere il nome e quindi ottenere il nome della famiglia di caratteri usando [**IDWriteLocalizedStrings:: GetString**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-getstring).</span><span class="sxs-lookup"><span data-stu-id="bd28a-135">Use this length to allocate a string large enough to hold the name and then get the font family name by using [**IDWriteLocalizedStrings::GetString**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-getstring).</span></span>


```C++
UINT32 length = 0;

// Get the string length.
if (SUCCEEDED(hr))
{
    hr = pFamilyNames->GetStringLength(index, &length);
}

// Allocate a string big enough to hold the name.
wchar_t* name = new (std::nothrow) wchar_t[length+1];
if (name == NULL)
{
    hr = E_OUTOFMEMORY;
}

// Get the family name.
if (SUCCEEDED(hr))
{
    hr = pFamilyNames->GetString(index, name, length+1);
}
```



## <a name="conclusion"></a><span data-ttu-id="bd28a-136">Conclusione</span><span class="sxs-lookup"><span data-stu-id="bd28a-136">Conclusion</span></span>

<span data-ttu-id="bd28a-137">Una volta ottenuto il nome della famiglia o i nomi nelle impostazioni locali, è possibile elencarli per consentire all'utente di scegliere o passarli a CreateTextFormat per iniziare a formattare il testo con la famiglia di caratteri specificata e così via.</span><span class="sxs-lookup"><span data-stu-id="bd28a-137">Once you have the family name or names in the locale, you can list them for the user to choose from, or pass it to CreateTextFormat to begin formatting text with the specified font family, and so on.</span></span>

## <a name="example-code"></a><span data-ttu-id="bd28a-138">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="bd28a-138">Example Code</span></span>

<span data-ttu-id="bd28a-139">Per visualizzare il codice sorgente completo per questo esempio, vedere l' [esempio di enumerazione dei tipi di carattere](/samples/browse/?redirectedfrom=MSDN-samples).</span><span class="sxs-lookup"><span data-stu-id="bd28a-139">To see the full source code for this example see the [Font Enumeration Sample](/samples/browse/?redirectedfrom=MSDN-samples).</span></span>

 

 