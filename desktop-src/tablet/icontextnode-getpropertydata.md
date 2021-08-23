---
description: Recupera dati specifici dell'applicazione o altri dati di proprietà per l'identificatore specificato.
ms.assetid: eaf95ff8-7b31-4c05-aa49-0c3bb9e996c0
title: Metodo IContextNode::GetPropertyData (IACom.h)
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
ms.openlocfilehash: 89e7ab9fb5213b41d53695b516b95b47193e8d803b207efd09216c743085927e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660721"
---
# <a name="icontextnodegetpropertydata-method"></a>Metodo IContextNode::GetPropertyData

Recupera dati specifici dell'applicazione o altri dati di proprietà per l'identificatore specificato.

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

*pPropertyDataId* \[ Pollici\]
</dt> <dd>

Identificatore per i dati.

</dd> <dt>

*pulPropertyDataSize* \[ in, out\]
</dt> <dd>

Dimensioni in byte dei dati. Il valore passato non viene usato.

</dd> <dt>

*ppbPropertyData* \[ Cambio\]
</dt> <dd>

Puntatore a una matrice di interi senza segno a 8 bit che contiene i dati delle proprietà.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, usare [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) per rilasciare la memoria da \* *ppbPropertyData* quando non sono più necessarie le informazioni.

 

Oltre a recuperare i dati specifici dell'applicazione aggiunti con [**IContextNode::AddPropertyData,**](icontextnode-addpropertydata.md)questo metodo viene usato per recuperare le proprietà comuni descritte dalle costanti [Context Node Properties.](context-node-properties.md)

Le proprietà di tipo stringa includono:

-   GUID \_ CNP \_ RECOGNIZEDSTRING
-   GUID \_ CNP \_ SHAPENAME
-   GUID \_ AHP \_ ANALYSISHINTNAME
-   GUID \_ AHP \_ PREFIXTEXT
-   GUID \_ AHP \_ SUFFIXTEXT
-   GUID \_ AHP \_ FACTOID

Il valore restituito è **WCHAR \**_. Se si esegue il cast del \_ *parametro ppbPropertyData* a **WCHAR, \**_ la lunghezza restituita è `(length of the string + 1) _ sizeof(WCHAR)` .

Le proprietà di tipo booleano includono:

-   GUID \_ AHP \_ OVERRIDELANGUAGEID
-   GUID \_ AHP \_ COERCETOFACTOID
-   GUID \_ AHP \_ WORDMODE

Il valore restituito è **VARIANT \_ BOOL.** Se si esegue il cast \* *del parametro ppbPropertyData* a **VARIANT \_ BOOL, \*** la lunghezza restituita è `sizeof(VARIANT_BOOL)` .

GUID \_ AHP \_ GUIDE è una proprietà di tipo guida. Il valore restituito è **InkAnalysisRecognitionGuide \** _. Se si esegue il cast del \_ *parametro ppbPropertyData* **a \* InkAnalysisRecognitionGuide,** la lunghezza restituita è `sizeof(InkAnalysisRecognitionGuide)` .

Le proprietà di tipo Integer includono:

-   GUID \_ CNP \_ LINENUMBER
-   GUID \_ CNP \_ POINTSPERINCH
-   GUID \_ CNP \_ CONFIDENCELEVEL
-   CONFERMA \_ CNP \_ GUID
-   GUID \_ CNP \_ MAXIMUMSTROKECOUNT
-   SEGMENTAZIONE \_ CNP \_ GUID
-   GUID \_ CNP \_ ALIGNMENTLEVEL

Il valore restituito è **LONG \** _. Se si esegue il cast del \_ *parametro ppbPropertyData* a **LONG, \*** la lunghezza restituita è `sizeof(LONG)` .

Le proprietà di tipo metriche linea includono:

-   GUID \_ CNP \_ ASCENDERS
-   DISCENDENTI \_ CNP \_ GUID
-   GUID \_ CNP \_ BASELINE
-   GUID \_ CNP \_ MIDLINE

Il valore restituito è **\* LONG.*_Se si esegue il cast del parametro \_ *ppbPropertyData* a **LONG, \**_ la lunghezza restituita è , che indica i valori (x, y) per i punti iniziali seguiti dai valori (x, y) per i punti `sizeof(LONG)_4` finali.

GUID \_ CNP \_ TEXTRECOGNIZERID è una **proprietà GUID.** Il valore restituito è **GUID \** _. Se si esegue il cast del \_ *parametro ppbPropertyData* al **GUID, \*** la lunghezza restituita è `sizeof(GUID)` .

GUID \_ CNP \_ ROTATEDBOUNDINGBOX è una proprietà del rettangolo di selezione ruotato. Il valore restituito è **\* LONG.*_Se si esegue il cast del parametro \_ *ppbPropertyData* a **LONG, \**_ la lunghezza restituita è , che indica i valori (x, y) per i `sizeof(LONG)_8` quattro angoli della casella.

GUID \_ CNP \_ HOTPOINT è una proprietà del punto di accesso. Il valore restituito è **\* LONG.*_Se si esegue il cast del \_ *parametro ppbPropertyData* a **LONG, \**_ la lunghezza restituita è , che indica `sizeof(LONG)_2` i valori (x, y) per il punto.

GUID \_ AHP \_ WORDLIST è una proprietà dell'elenco di parole. Il valore restituito è **WCHAR \**_. Se si esegue il cast del parametro \_ *ppbPropertyData* a **WCHAR, \**_ la lunghezza restituita è , dove è la somma delle lunghezze di stringa del numero di stringhe nell'elenco più 1 per ogni carattere di terminazione NULL per `n _ sizeof(WCHAR)` ogni `n` stringa. 

## <a name="examples"></a>Esempio

Questo esempio illustra un metodo che accede alla proprietà del nodo di contesto AlignmentLevel di un tipo di nodo di contesto Paragraph.


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
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md)
</dt> <dt>

[**IContextNode::RemovePropertyData**](icontextnode-removepropertydata.md)
</dt> <dt>

[**IContextNode::GetPropertyDataIds**](icontextnode-getpropertydataids.md)
</dt> <dt>

[**IContextNode::ContainsPropertyData**](icontextnode-containspropertydata.md)
</dt> <dt>

[**IContextNode::LoadPropertiesData**](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[**IContextNode::SavePropertiesData**](icontextnode-savepropertiesdata.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

