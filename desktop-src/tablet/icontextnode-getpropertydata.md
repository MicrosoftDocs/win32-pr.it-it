---
description: Recupera i dati specifici dell'applicazione o altri dati della proprietà per l'identificatore specificato.
ms.assetid: eaf95ff8-7b31-4c05-aa49-0c3bb9e996c0
title: 'Metodo IContextNode:: GetPropertyData (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetPropertyData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 381d137dd73056a2a6f4c2e9cd3746f9f16c5b2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751847"
---
# <a name="icontextnodegetpropertydata-method"></a>Metodo IContextNode:: GetPropertyData

Recupera i dati specifici dell'applicazione o altri dati della proprietà per l'identificatore specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetPropertyData(
  [in]      const GUID  *pPropertyDataId,
  [in, out]       ULONG *pulPropertyDataSize,
  [out]           BYTE  **ppbPropertyData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pPropertyDataId* \[ in\]
</dt> <dd>

Identificatore per i dati.

</dd> <dt>

*pulPropertyDataSize* \[ in uscita\]
</dt> <dd>

Dimensioni dei dati in byte. Il valore passato non viene utilizzato.

</dd> <dt>

*ppbPropertyData* \[ out\]
</dt> <dd>

Puntatore a una matrice di Unsigned Integer a 8 bit che contiene i dati della proprietà.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, usare [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) per rilasciare la memoria da \* *ppbPropertyData* quando le informazioni non sono più necessarie.

 

Oltre a recuperare i dati specifici dell'applicazione aggiunti con [**IContextNode:: AddPropertyData**](icontextnode-addpropertydata.md), questo metodo viene usato per recuperare le proprietà comuni descritte dalle costanti delle [proprietà del nodo di contesto](context-node-properties.md) .

Le proprietà di tipo stringa includono:

-   GUID \_ CNP \_ RECOGNIZEDSTRING
-   GUID \_ CNP \_ ShapeName
-   GUID \_ AHP \_ ANALYSISHINTNAME
-   GUID \_ AHP \_ PREFIXTEXT
-   GUID \_ AHP \_ SUFFIXTEXT
-   controllo controllo \_ AHP GUID \_

Il valore restituito è **WCHAR \**_. Se si esegue il cast del \_ parametro *ppbPropertyData* a **\* WCHAR*_ la lunghezza restituita è `(length of the string + 1) _ sizeof(WCHAR)` .

Le proprietà di tipo booleano includono:

-   GUID \_ AHP \_ OVERRIDELANGUAGEID
-   GUID \_ AHP \_ COERCETOFACTOID
-   GUID \_ AHP \_ WORDMODE

Il valore restituito è la **variante \_ bool**. Se si esegue il cast del \* parametro *ppbPropertyData* a **Variant \_ bool \** _ la lunghezza restituita è `sizeof(VARIANT_BOOL)` .

GUID \_ AHP \_ guide è una proprietà di tipo guida. Il valore restituito è _*InkAnalysisRecognitionGuide \**_. Se si esegue il cast del \_ parametro *ppbPropertyData* a **InkAnalysisRecognitionGuide \** _ la lunghezza restituita è `sizeof(InkAnalysisRecognitionGuide)` .

Le proprietà di tipo integer includono:

-   GUID \_ CNP \_ LINENUMBER
-   GUID \_ CNP \_ POINTSPERINCH
-   GUID \_ CNP \_ CONFIDENCELEVEL
-   \_conferma CNP \_ GUID
-   GUID \_ CNP \_ MAXIMUMSTROKECOUNT
-   \_ \_ segmentazione GUID CNP
-   GUID \_ CNP \_ ALIGNMENTLEVEL

Il valore restituito è _*Long \**_. Se si esegue il cast del \_ parametro *ppbPropertyData* a **Long \** _ la lunghezza restituita è `sizeof(LONG)` .

Metrica riga: le proprietà del tipo includono:

-   GUID \_ CNP \_ ascenders
-   \_CNP \_ DISCENDEnti GUID
-   \_linea di \_ base CNP GUID
-   linea \_ media CNP GUID \_

Il valore restituito è _*Long \**_. Se si esegue il cast del \_ parametro *ppbPropertyData* a **\* Long* _ la lunghezza restituita è, indicando `sizeof(LONG)_4` i valori (x, y) per i punti iniziali seguiti dai valori (x, y) per i punti finali.

GUID \_ CNP \_ TEXTRECOGNIZERID è una proprietà **GUID** . Il valore restituito è **GUID \**_. Se si esegue il cast del \_ parametro *ppbPropertyData* in **\* GUID*_ , la lunghezza restituita è `sizeof(GUID)` .

GUID \_ CNP \_ ROTATEDBOUNDINGBOX è una proprietà del rettangolo di delimitazione ruotata. Il valore restituito è _*Long \**_. Se si esegue il cast del \_ parametro *ppbPropertyData* a **\* Long* _ la lunghezza restituita è, indicando `sizeof(LONG)_8` i valori (x, y) per i quattro angoli della casella.

GUID \_ CNP \_ Hotpoint è una proprietà di punti sensibili. Il valore restituito è **Long \**_. Se si esegue il cast del \_ parametro *ppbPropertyData* a **Long \**_ la lunghezza restituita è, indicando `sizeof(LONG)_2` i valori (x, y) per il punto.

GUID \_ AHP \_ è una proprietà dell'elenco di parole. Il valore restituito è **WCHAR \**_. Se si esegue il cast del \_ parametro *ppbPropertyData* a **\* WCHAR*_ la lunghezza restituita è `n _ sizeof(WCHAR)` , dove `n` è la somma delle lunghezze di stringa del numero di stringhe nell'elenco più 1 per ogni carattere di terminazione **null** per ogni stringa.

## <a name="examples"></a>Esempio

Questo esempio mostra un metodo che accede alla proprietà del nodo di contesto AlignmentLevel di un tipo di nodo di contesto di paragrafo.


```C++
// Checks a paragraph context node's alignment level property.
// Only paragraph type context nodes contain the alignment level property.
HRESULT CMyClass::ExploreParagraphNode(
    IContextNode *pParagraphNode)
{
    // Get the AlignmentLevel property data for the paragraph.
    LONG * alignmentLevel = NULL;
    ULONG ulDataLen = 0;

    HRESULT hr = pParagraphNode->GetPropertyData(
        (const GUID*)&GUID_CNP_ALIGNMENTLEVEL,
        &ulDataLen,
        (BYTE**)&alignmentLevel);

    if( FAILED(hr) ||
        ulDataLen != sizeof(LONG) ||
        alignmentLevel == NULL )
    {
        // Insert code that handles an error here.
    }
    else
    {
        // Insert code that uses the alignment level here.
    }

    // Free the memory allocated for the property data.
    ::CoTaskMemFree(alignmentLevel);

    return hr;
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom. h (richiede anche IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNode:: AddPropertyData**](icontextnode-addpropertydata.md)
</dt> <dt>

[**IContextNode:: RemovePropertyData**](icontextnode-removepropertydata.md)
</dt> <dt>

[**IContextNode:: GetPropertyDataIds**](icontextnode-getpropertydataids.md)
</dt> <dt>

[**IContextNode:: ContainsPropertyData**](icontextnode-containspropertydata.md)
</dt> <dt>

[**IContextNode:: LoadPropertiesData**](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[**IContextNode:: SavePropertiesData**](icontextnode-savepropertiesdata.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

