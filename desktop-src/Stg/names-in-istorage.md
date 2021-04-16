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
# <a name="names-in-istorage"></a>Nomi in IStorage

Un set di proprietà viene identificato con un identificatore di formato (FMTID) nell'interfaccia [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) . Nell'interfaccia [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) un set di proprietà viene denominato con una stringa Unicode con terminazione null con una lunghezza massima di 32 caratteri. Per consentire l'interoperabilità, è necessario stabilire un mapping tra un FMTID e una stringa Unicode con terminazione null corrispondente.

## <a name="converting-a-property-set-from-a-fmtid-to-a-string-name"></a>Conversione di un set di proprietà da un FMTID in un nome di stringa

Quando si esegue la conversione da un FMTID a un nome di stringa Unicode corrispondente, verificare innanzitutto che FMTID sia un valore noto, elencato nella tabella seguente. In tal caso, usare il nome di stringa noto corrispondente.

| FMTID                                                                                | Nome della stringa                       | Semantica                                                         |
|--------------------------------------------------------------------------------------|-----------------------------------|------------------------------------------------------------------|
| F29F85E0-4FF9-1068-AB91-08002B27B3D9                                                 | " \\ 005SummaryInformation"         | Informazioni di riepilogo di COM2                                         |
| D5CDD502-2E9C-101B-9397-08002B2CF9AE D5CDD505-2E9C-101B-9397-08002B2CF9AE<br/> | " \\ 005DocumentSummaryInformation" | Informazioni di riepilogo sui documenti di Office e proprietà definite dall'utente. |



 

> [!Note]  
> Il set di proprietà **DocumentSummaryInformation** e **UserDefined** è univoco in quanto contiene due sezioni. Non sono consentite più sezioni in nessun altro set di proprietà. Per altre informazioni, vedere [formato di set di proprietà serializzato di archiviazione strutturata](structured-storage-serialized-property-set-format.md)e [set di proprietà DocumentSummaryInformation e UserDefined](the-documentsummaryinformation-and-userdefined-property-sets.md). La prima sezione è stata definita come parte di COM; il secondo è stato definito da Microsoft Office.

 

Se FMTID non è un valore noto, usare la procedura seguente per algoritmicamente formare un nome di stringa.

**Per algoritmicamente formare un nome di stringa**

1.  Convertire FMTID in ordine di byte little-endian, se necessario.
2.  Prendere i 128 bit di FMTID e considerarli come una stringa di bit lungo concatenando ogni byte insieme. Il primo bit del valore di bit 128 è il bit meno significativo del primo byte in memoria di FMTID; l'ultimo bit del valore di bit 128 è il bit più significativo dell'ultimo byte in memoria del FMTID. Estendere questi 128 bit a 130 bit aggiungendo due bit zero alla fine.
3.  Dividere i 130 bit in gruppi di cinque bit; saranno presenti 26 gruppi di questo tipo. Considerare ogni gruppo come un numero intero con precedenza in bit invertita. Ad esempio, il primo di 128 bit è il bit meno significativo del primo gruppo di cinque bit; il quinto dei 128 bit è il bit più significativo del primo gruppo.
4.  Eseguire il mapping di ognuno di questi integer come indice nella matrice di 32 caratteri: ABCDEFGHIJKLMNOPQRSTUVWXYZ012345. Viene restituita una sequenza di 26 caratteri Unicode che utilizza solo caratteri maiuscoli e numerici. Le considerazioni relative a maiuscole e minuscole e senza distinzione tra maiuscole e minuscole non si applicano, rendendo ogni carattere univoco nelle impostazioni locali.
5.  Creare la stringa finale concatenando la stringa " \\ 005" sulla parte anteriore dei 26 caratteri, per una lunghezza totale di 27 caratteri.

Nell'esempio di codice seguente viene illustrato come eseguire il mapping da un FMTID a una stringa di proprietà.


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



## <a name="converting-a-property-set-from-a-string-name-to-a-fmtid"></a>Conversione di un set di proprietà da un nome di stringa in un FMTID

I convertitori di nomi di stringa di proprietà nei GUID devono accettare lettere minuscole come sinonimi delle rispettive controparti maiuscole.

Nell'esempio di codice seguente viene illustrato come eseguire il mapping da una stringa di proprietà a un FMTID.


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



Quando si tenta di aprire un set di proprietà esistente, in [IPropertySetStorage:: Open](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)il fmtid (radice) viene convertito in una stringa come descritto in precedenza. Se è presente un elemento di [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) con tale nome, viene utilizzato. In caso contrario, l'apertura non riesce.

Quando si crea un nuovo set di proprietà, il mapping precedente determina il nome della stringa usata.

 

 





