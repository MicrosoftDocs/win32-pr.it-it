---
title: Nomi in IStorage
description: Un set di proprietà viene identificato con un identificatore di formato (FMTID) nell'interfaccia IPropertySetStorage.
ms.assetid: 5f8eba37-c589-413e-9971-7ecb01dc6734
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cef9417f2f5fad7fd17dcc3d431f1d3565a3843
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104516111"
---
# <a name="names-in-istorage"></a><span data-ttu-id="c7b07-103">Nomi in IStorage</span><span class="sxs-lookup"><span data-stu-id="c7b07-103">Names in IStorage</span></span>

<span data-ttu-id="c7b07-104">Un set di proprietà viene identificato con un identificatore di formato (FMTID) nell'interfaccia [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) .</span><span class="sxs-lookup"><span data-stu-id="c7b07-104">A property set is identified with a format identifier (FMTID) in the [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) interface.</span></span> <span data-ttu-id="c7b07-105">Nell'interfaccia [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) un set di proprietà viene denominato con una stringa Unicode con terminazione null con una lunghezza massima di 32 caratteri.</span><span class="sxs-lookup"><span data-stu-id="c7b07-105">In the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface, a property set is named with a null-terminated Unicode string with a maximum length of 32 characters.</span></span> <span data-ttu-id="c7b07-106">Per consentire l'interoperabilità, è necessario stabilire un mapping tra un FMTID e una stringa Unicode con terminazione null corrispondente.</span><span class="sxs-lookup"><span data-stu-id="c7b07-106">To enable interoperability, a mapping between an FMTID and a corresponding null-terminated Unicode string must be established.</span></span>

## <a name="converting-a-property-set-from-a-fmtid-to-a-string-name"></a><span data-ttu-id="c7b07-107">Conversione di un set di proprietà da un FMTID in un nome di stringa</span><span class="sxs-lookup"><span data-stu-id="c7b07-107">Converting a property set from a FMTID to a string name</span></span>

<span data-ttu-id="c7b07-108">Quando si esegue la conversione da un FMTID a un nome di stringa Unicode corrispondente, verificare innanzitutto che FMTID sia un valore noto, elencato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="c7b07-108">When converting from an FMTID to a corresponding Unicode string name, first verify that the FMTID is a well-known value, listed in the following table.</span></span> <span data-ttu-id="c7b07-109">In tal caso, usare il nome di stringa noto corrispondente.</span><span class="sxs-lookup"><span data-stu-id="c7b07-109">If so, then use the corresponding well-known string name.</span></span>

| <span data-ttu-id="c7b07-110">FMTID</span><span class="sxs-lookup"><span data-stu-id="c7b07-110">FMTID</span></span>                                                                                | <span data-ttu-id="c7b07-111">Nome della stringa</span><span class="sxs-lookup"><span data-stu-id="c7b07-111">String name</span></span>                       | <span data-ttu-id="c7b07-112">Semantica</span><span class="sxs-lookup"><span data-stu-id="c7b07-112">Semantic</span></span>                                                         |
|--------------------------------------------------------------------------------------|-----------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="c7b07-113">F29F85E0-4FF9-1068-AB91-08002B27B3D9</span><span class="sxs-lookup"><span data-stu-id="c7b07-113">F29F85E0-4FF9-1068-AB91-08002B27B3D9</span></span>                                                 | <span data-ttu-id="c7b07-114">" \\ 005SummaryInformation"</span><span class="sxs-lookup"><span data-stu-id="c7b07-114">"\\005SummaryInformation"</span></span>         | <span data-ttu-id="c7b07-115">Informazioni di riepilogo di COM2</span><span class="sxs-lookup"><span data-stu-id="c7b07-115">COM2 summary information</span></span>                                         |
| <span data-ttu-id="c7b07-116">D5CDD502-2E9C-101B-9397-08002B2CF9AE D5CDD505-2E9C-101B-9397-08002B2CF9AE</span><span class="sxs-lookup"><span data-stu-id="c7b07-116">D5CDD502-2E9C-101B-9397-08002B2CF9AE D5CDD505-2E9C-101B-9397-08002B2CF9AE</span></span><br/> | <span data-ttu-id="c7b07-117">" \\ 005DocumentSummaryInformation"</span><span class="sxs-lookup"><span data-stu-id="c7b07-117">"\\005DocumentSummaryInformation"</span></span> | <span data-ttu-id="c7b07-118">Informazioni di riepilogo sui documenti di Office e proprietà definite dall'utente.</span><span class="sxs-lookup"><span data-stu-id="c7b07-118">Office document summary information and user-defined properties.</span></span> |



 

> [!Note]  
> <span data-ttu-id="c7b07-119">Il set di proprietà **DocumentSummaryInformation** e **UserDefined** è univoco in quanto contiene due sezioni.</span><span class="sxs-lookup"><span data-stu-id="c7b07-119">The **DocumentSummaryInformation** and **UserDefined** property set is unique in that it contains two sections.</span></span> <span data-ttu-id="c7b07-120">Non sono consentite più sezioni in nessun altro set di proprietà.</span><span class="sxs-lookup"><span data-stu-id="c7b07-120">Multiple sections are not permitted in any other property set.</span></span> <span data-ttu-id="c7b07-121">Per altre informazioni, vedere [formato di set di proprietà serializzato di archiviazione strutturata](structured-storage-serialized-property-set-format.md)e [set di proprietà DocumentSummaryInformation e UserDefined](the-documentsummaryinformation-and-userdefined-property-sets.md).</span><span class="sxs-lookup"><span data-stu-id="c7b07-121">For more information, see [Structured Storage Serialized Property Set Format](structured-storage-serialized-property-set-format.md), and [The DocumentSummaryInformation and UserDefined Property Sets](the-documentsummaryinformation-and-userdefined-property-sets.md).</span></span> <span data-ttu-id="c7b07-122">La prima sezione è stata definita come parte di COM; il secondo è stato definito da Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="c7b07-122">The first section was defined as part of COM; the second was defined by Microsoft Office.</span></span>

 

<span data-ttu-id="c7b07-123">Se FMTID non è un valore noto, usare la procedura seguente per algoritmicamente formare un nome di stringa.</span><span class="sxs-lookup"><span data-stu-id="c7b07-123">If the FMTID is not a well-known value, then use the following procedure to algorithmically form a string name.</span></span>

<span data-ttu-id="c7b07-124">**Per algoritmicamente formare un nome di stringa**</span><span class="sxs-lookup"><span data-stu-id="c7b07-124">**To algorithmically form a string name**</span></span>

1.  <span data-ttu-id="c7b07-125">Convertire FMTID in ordine di byte little-endian, se necessario.</span><span class="sxs-lookup"><span data-stu-id="c7b07-125">Convert the FMTID to little-endian byte order, if necessary.</span></span>
2.  <span data-ttu-id="c7b07-126">Prendere i 128 bit di FMTID e considerarli come una stringa di bit lungo concatenando ogni byte insieme.</span><span class="sxs-lookup"><span data-stu-id="c7b07-126">Take the 128 bits of the FMTID and consider them as one long bit string by concatenating each of the bytes together.</span></span> <span data-ttu-id="c7b07-127">Il primo bit del valore di bit 128 è il bit meno significativo del primo byte in memoria di FMTID; l'ultimo bit del valore di bit 128 è il bit più significativo dell'ultimo byte in memoria del FMTID.</span><span class="sxs-lookup"><span data-stu-id="c7b07-127">The first bit of the 128 bit value is the least significant bit of the first byte in memory of the FMTID; the last bit of the 128 bit value is the most significant bit of the last byte in memory of the FMTID.</span></span> <span data-ttu-id="c7b07-128">Estendere questi 128 bit a 130 bit aggiungendo due bit zero alla fine.</span><span class="sxs-lookup"><span data-stu-id="c7b07-128">Extend these 128 bits to 130 bits by adding two zero bits to the end.</span></span>
3.  <span data-ttu-id="c7b07-129">Dividere i 130 bit in gruppi di cinque bit; saranno presenti 26 gruppi di questo tipo.</span><span class="sxs-lookup"><span data-stu-id="c7b07-129">Divide the 130 bits into groups of five bits; there will be 26 such groups.</span></span> <span data-ttu-id="c7b07-130">Considerare ogni gruppo come un numero intero con precedenza in bit invertita.</span><span class="sxs-lookup"><span data-stu-id="c7b07-130">Consider each group as an integer with reversed bit precedence.</span></span> <span data-ttu-id="c7b07-131">Ad esempio, il primo di 128 bit è il bit meno significativo del primo gruppo di cinque bit; il quinto dei 128 bit è il bit più significativo del primo gruppo.</span><span class="sxs-lookup"><span data-stu-id="c7b07-131">For example, the first of the 128 bits is the least significant bit of the first group of five bits; the fifth of the 128 bits is the most significant bit of the first group.</span></span>
4.  <span data-ttu-id="c7b07-132">Eseguire il mapping di ognuno di questi integer come indice nella matrice di 32 caratteri: ABCDEFGHIJKLMNOPQRSTUVWXYZ012345.</span><span class="sxs-lookup"><span data-stu-id="c7b07-132">Map each of these integers as an index into the array of thirty-two characters: ABCDEFGHIJKLMNOPQRSTUVWXYZ012345.</span></span> <span data-ttu-id="c7b07-133">Viene restituita una sequenza di 26 caratteri Unicode che utilizza solo caratteri maiuscoli e numerici.</span><span class="sxs-lookup"><span data-stu-id="c7b07-133">This yields a sequence of 26 Unicode characters that uses only uppercase characters and numerals.</span></span> <span data-ttu-id="c7b07-134">Le considerazioni relative a maiuscole e minuscole e senza distinzione tra maiuscole e minuscole non si applicano, rendendo ogni carattere univoco nelle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="c7b07-134">Case sensitive and case insensitive considerations do not apply, causing each character to be unique in any locale.</span></span>
5.  <span data-ttu-id="c7b07-135">Creare la stringa finale concatenando la stringa " \\ 005" sulla parte anteriore dei 26 caratteri, per una lunghezza totale di 27 caratteri.</span><span class="sxs-lookup"><span data-stu-id="c7b07-135">Create the final string by concatenating the string "\\005" onto the front of these 26 characters, for a total length of 27 characters.</span></span>

<span data-ttu-id="c7b07-136">Nell'esempio di codice seguente viene illustrato come eseguire il mapping da un FMTID a una stringa di proprietà.</span><span class="sxs-lookup"><span data-stu-id="c7b07-136">The following example code shows how to map from an FMTID to a property string.</span></span>


```C++
#define CBIT_BYTE        8
#define CBIT_CHARMASK    5
#define CCH_MAP          (1 << CBIT_CHARMASK)    // 32
#define CHARMASK         (CCH_MAP - 1)           // 0x1f
 
CHAR awcMap[CCH_MAP + 1] = "abcdefghijklmnopqrstuvwxyz012345";
 
WCHAR MapChar(ULONG I) {
    return((WCHAR) awcMap[i & CHARMASK]);
    }
 
VOID GuidToPropertyStringName(GUID *pguid, WCHAR awcname[]) {
    BYTE *pb = (BYTE *) pguid;
    BYTE *pbEnd = pb + sizeof(*pguid);
    ULONG cbitRemain = CBIT_BYTE;
    WCHAR *pwc = awcname;
 
    *pwc++ = ((WCHAR) 0x0005);
    while (pb < pbEnd) {
        ULONG i = *pb >> (CBIT_BYTE - cbitRemain);
        if (cbitRemain >= CBIT_CHARMASK) {
            *pwc = MapChar(i);
            if (cbitRemain == CBIT_BYTE && 
                                    *pwc >= L'a' && *pwc <= L'z')
                {
                *pwc += (WCHAR) (L'A' - L'a');
                }
            pwc++;
            cbitRemain -= CBIT_CHARMASK;
            if (cbitRemain == 0) {
                pb++;
                cbitRemain = CBIT_BYTE;
                }
            }
        else {
            if (++pb < pbEnd) {
                i |= *pb << cbitRemain;
                }
            *pwc++ = MapChar(i);
            cbitRemain += CBIT_BYTE - CBIT_CHARMASK;
            }
        }
    *pwc = L'\0';
    }
```



## <a name="converting-a-property-set-from-a-string-name-to-a-fmtid"></a><span data-ttu-id="c7b07-137">Conversione di un set di proprietà da un nome di stringa in un FMTID</span><span class="sxs-lookup"><span data-stu-id="c7b07-137">Converting a property set from a string name to a FMTID</span></span>

<span data-ttu-id="c7b07-138">I convertitori di nomi di stringa di proprietà nei GUID devono accettare lettere minuscole come sinonimi delle rispettive controparti maiuscole.</span><span class="sxs-lookup"><span data-stu-id="c7b07-138">Converters of property string names to GUIDs should accept lowercase letters as synonymous with their uppercase counterparts.</span></span>

<span data-ttu-id="c7b07-139">Nell'esempio di codice seguente viene illustrato come eseguire il mapping da una stringa di proprietà a un FMTID.</span><span class="sxs-lookup"><span data-stu-id="c7b07-139">The following example code shows how to map from a property string to an FMTID.</span></span>


```C++
#include "stdafx.h"
#define _INC_OLE
#include <windows.h>
#include <stdlib.h>
#include <stdio.h>
#include <string.h>
#include <ctype.h>
#define CBIT_CHARMASK 5
#define CBIT_BYTE     8
#define CBIT_GUID    (CBIT_BYTE * sizeof(GUID))
#define CWC_PROPSET  (1 + (CBIT_GUID + CBIT_CHARMASK-1)/CBIT_CHARMASK)
#define WC_PROPSET0  ((WCHAR) 0x0005)
#define CCH_MAP      (1 << CBIT_CHARMASK)        // 32
#define CHARMASK     (CCH_MAP - 1)            // 0x1f
CHAR awcMap[CCH_MAP + 1] = "abcdefghijklmnopqrstuvwxyz012345";
#define CALPHACHARS  ('z' - 'a' + 1)

GUID guidSummary =
{ 0xf29f85e0,0x4ff9, 0x1068,
{ 0xab, 0x91, 0x08, 0x00, 0x2b, 0x27, 0xb3, 0xd9 } };

WCHAR wszSummary[] = L"SummaryInformation";

GUID guidDocumentSummary =
    { 0xd5cdd502,
      0x2e9c, 0x101b,
      { 0x93, 0x97, 0x08, 0x00, 0x2b, 0x2c, 0xf9, 0xae } };

WCHAR wszDocumentSummary[] = L"DocumentSummaryInformation";
__inline WCHAR

MapChar(IN ULONG i)
{
    return((WCHAR) awcMap[i & CHARMASK]);
}

ULONG PropertySetNameToGuid(
    IN ULONG cwcname,
    IN WCHAR const awcname[],
    OUT GUID *pguid)
{
    ULONG Status = ERROR_INVALID_PARAMETER;
    WCHAR const *pwc = awcname;

    if (pwc[0] == WC_PROPSET0)
    {
        //Note: cwcname includes the WC_PROPSET0, and
        //sizeof(wsz...) includes the trailing L'\0', but
        //the comparison excludes both the leading
        //WC_PROPSET0 and the trailing L'\0'.
        if (cwcname == sizeof(wszSummary)/sizeof(WCHAR) &&
            wcsnicmp(&pwc[1], wszSummary, cwcname - 1) == 0)
        {
            *pguid = guidSummary;
            return(NO_ERROR);
        }
        if (cwcname == CWC_PROPSET)
        {
            ULONG cbit;
            BYTE *pb = (BYTE *) pguid - 1;
            ZeroMemory(pguid, sizeof(*pguid));
            for (cbit = 0; cbit < CBIT_GUID; cbit += 
            CBIT_CHARMASK)
            {
                ULONG cbitUsed = cbit % CBIT_BYTE;
                ULONG cbitStored;
                WCHAR wc;
                if (cbitUsed == 0)
                {
                    pb++;
                }
                wc = *++pwc - L'A';        //assume uppercase
                if (wc > CALPHACHARS)
                {
                    wc += (WCHAR) (L'A' - L'a'); //try lowercase
                    if (wc > CALPHACHARS)
                    {
                        wc += L'a' - L'0' + CALPHACHARS; 
                        if (wc > CHARMASK)
                        {
                            goto fail;       //invalid character
                        }
                    }
                }
                *pb |= (BYTE) (wc << cbitUsed);
                cbitStored = min(CBIT_BYTE - cbitUsed, 
                CBIT_CHARMASK);

                //If the translated bits will not fit in the 
                //current byte
                if (cbitStored < CBIT_CHARMASK)
                {
                    wc >>= CBIT_BYTE - cbitUsed;
                    if (cbit + cbitStored == CBIT_GUID)
                    {
                       if (wc != 0)
                       {
                           goto fail;        //extra bits
                       }
                       break;
                    }
                    pb++;
                    *pb |= (BYTE) wc;
                }
           }
           Status = NO_ERROR;
      }
    }
fail:
    return(Status);
}
```



<span data-ttu-id="c7b07-140">Quando si tenta di aprire un set di proprietà esistente, in [IPropertySetStorage:: Open](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)il fmtid (radice) viene convertito in una stringa come descritto in precedenza.</span><span class="sxs-lookup"><span data-stu-id="c7b07-140">When attempting to open an existing property set, in [IPropertySetStorage::Open](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open), the (root) FMTID is converted to a string as described above.</span></span> <span data-ttu-id="c7b07-141">Se è presente un elemento di [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) con tale nome, viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="c7b07-141">If an element of the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) of that name exists, it is used.</span></span> <span data-ttu-id="c7b07-142">In caso contrario, l'apertura non riesce.</span><span class="sxs-lookup"><span data-stu-id="c7b07-142">Otherwise, the open fails.</span></span>

<span data-ttu-id="c7b07-143">Quando si crea un nuovo set di proprietà, il mapping precedente determina il nome della stringa usata.</span><span class="sxs-lookup"><span data-stu-id="c7b07-143">When creating a new property set, the above mapping determines the string name used.</span></span>

 

 





