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
# <a name="how-to-enumerate-fonts"></a>Come enumerare i tipi di carattere

In questa panoramica viene illustrato come enumerare i tipi di carattere nella raccolta di tipi di carattere del sistema, in base al nome della famiglia.

Questa panoramica è costituita dalle parti seguenti:

-   [Passaggio 1: ottenere la raccolta di tipi di carattere di sistema.](#step-1-get-the-system-font-collection)
-   [Passaggio 2: ottenere il conteggio delle famiglie di caratteri.](#step-2-get-the-font-family-count)
-   [Creare un ciclo for.](#make-a-for-loop)
    -   [Passaggio 3: ottenere la famiglia di caratteri.](#step-3-get-the-font-family)
    -   [Passaggio 4: ottenere i nomi di famiglia.](#step-4-get-the-family-names)
    -   [Passaggio 5: trovare il nome delle impostazioni locali.](#step-5-find-the-locale-name)
    -   [Passaggio 6: ottenere la lunghezza della stringa del nome della famiglia e della stringa.](#step-6-get-the-length-of-the-family-name-string-length-and-the-string)
-   [Conclusione](#conclusion)
-   [Codice di esempio](#example-code)

## <a name="step-1-get-the-system-font-collection"></a>Passaggio 1: ottenere la raccolta di tipi di carattere di sistema.

Usare il metodo [**GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) fornito dalla factory DirectWrite per restituire un [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) con tutti i tipi di carattere di sistema.


```C++
IDWriteFontCollection* pFontCollection = NULL;

// Get the system font collection.
if (SUCCEEDED(hr))
{
    hr = pDWriteFactory->GetSystemFontCollection(&pFontCollection);
}
```



## <a name="step-2-get-the-font-family-count"></a>Passaggio 2: ottenere il conteggio delle famiglie di caratteri.

Ottenere quindi il conteggio delle famiglie di caratteri dalla raccolta dei tipi di carattere usando [**IDWriteFontCollection:: GetFontFamilyCount**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollection-getfontfamilycount). Questa operazione verrà usata per eseguire il ciclo di ogni famiglia di caratteri nella raccolta.


```C++
UINT32 familyCount = 0;

// Get the number of font families in the collection.
if (SUCCEEDED(hr))
{
    familyCount = pFontCollection->GetFontFamilyCount();
}
```



## <a name="make-a-for-loop"></a>Creare un ciclo for.


```C++
for (UINT32 i = 0; i < familyCount; ++i)
```



Ora che si dispone della raccolta dei tipi di carattere e del conteggio dei tipi di carattere, i passaggi rimanenti eseguono il ciclo su ogni famiglia di caratteri, recuperando l'oggetto [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) ed eseguendo una query su di esso.

### <a name="step-3-get-the-font-family"></a>Passaggio 3: ottenere la famiglia di caratteri.

Ottenere un oggetto [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) usando [**IDWriteFontCollection:: GetFontFamily**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollection-getfontfamily) e passandogli l'indice corrente, *i*.


```C++
IDWriteFontFamily* pFontFamily = NULL;

// Get the font family.
if (SUCCEEDED(hr))
{
    hr = pFontCollection->GetFontFamily(i, &pFontFamily);
}
```



### <a name="step-4-get-the-family-names"></a>Passaggio 4: ottenere i nomi di famiglia.

Ottenere i nomi delle famiglie di caratteri usando [**IDWriteFontFamily:: GetFamilyNames**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfamily-getfamilynames). Si tratta di un oggetto [**IDWriteLocalizedStrings**](/windows/win32/api/dwrite/nn-dwrite-idwritelocalizedstrings) . Può avere più versioni localizzate del nome della famiglia per la famiglia di caratteri.


```C++
IDWriteLocalizedStrings* pFamilyNames = NULL;

// Get a list of localized strings for the family name.
if (SUCCEEDED(hr))
{
    hr = pFontFamily->GetFamilyNames(&pFamilyNames);
}
```



### <a name="step-5-find-the-locale-name"></a>Passaggio 5: trovare il nome delle impostazioni locali.

Ottenere il nome del tipo di carattere famliy nelle impostazioni locali desiderate usando il metodo [**IDWriteLocalizedStrings:: FindLocaleName**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-findlocalename) . In questo caso, vengono recuperate e richieste prima le impostazioni locali predefinite. Se l'operazione non funziona, le impostazioni locali "en-US" sono richieste. Se una delle impostazioni locali specificate non viene trovata, questo esempio esegue semplicemente il fallback all'indice 0, ovvero le prime impostazioni locali disponibili.


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



### <a name="step-6-get-the-length-of-the-family-name-string-length-and-the-string"></a>Passaggio 6: ottenere la lunghezza della stringa del nome della famiglia e della stringa.

Infine, ottenere la lunghezza della stringa del nome della famiglia utilizzando [**IDWriteLocalizedStrings:: GetStringLength**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-getstringlength). Usare questa lunghezza per allocare una stringa sufficientemente grande da mantenere il nome e quindi ottenere il nome della famiglia di caratteri usando [**IDWriteLocalizedStrings:: GetString**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-getstring).


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



## <a name="conclusion"></a>Conclusione

Una volta ottenuto il nome della famiglia o i nomi nelle impostazioni locali, è possibile elencarli per consentire all'utente di scegliere o passarli a CreateTextFormat per iniziare a formattare il testo con la famiglia di caratteri specificata e così via.

## <a name="example-code"></a>Codice di esempio

Per visualizzare il codice sorgente completo per questo esempio, vedere l' [esempio di enumerazione dei tipi di carattere](/samples/browse/?redirectedfrom=MSDN-samples).

 

 