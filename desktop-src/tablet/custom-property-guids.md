---
description: I seguenti identificatori univoci globali (GUID) vengono usati da Windows Journal per identificare le proprietà personalizzate nei tratti o negli attributi di disegno.
ms.assetid: a7488c26-b61f-47d8-a19b-d630a8c00875
title: GUID proprietà personalizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eb1d9069f2c655f658752a6ae3891910ff68103
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316865"
---
# <a name="custom-property-guids"></a>GUID proprietà personalizzati

I seguenti identificatori univoci globali (GUID) vengono usati da Windows Journal per identificare le proprietà personalizzate nei tratti o negli attributi di disegno.

## <a name="guid_stroke_timestamp"></a>\_timestamp del tratto GUID \_


```C++
GUID_STROKE_TIMESTAMP = {4EA66C4-F33A-461B-B8FE-68070D9C7575}
```



Si tratta di una struttura [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) che indica l'ora in cui il tratto è stato creato o aggiunto al documento.


```C++
typedef struct _FILETIME {
    DWORD dwLowDateTime;
    DWORD dwHighDateTime;
} FILETIME, *PFILETIME;
```



## <a name="guid_stroke_timeid"></a>\_TimeID tratto \_ GUID


```C++
GUID_STROKE_TIMEID = {50B6BC8-3B7D-4816-8C61-BC7E905B2132}
```



Si tratta di una struttura **TimeID** . Consente di mantenere l'ordine del tratto tra le operazioni di Incolla e rilascio. Senza la struttura **TimeID** , il timestamp per tutti gli oggetti dell' [**interfaccia IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) tagliati e incollati in una [raccolta InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) sarà lo stesso.


```C++
typedef struct tagTIMEID {
    FILETIME  tmFiletime;
    ULONG     uiOrder;
} TIMEID;
```



## <a name="guid_highlighter"></a>\_evidenziatore GUID

Si tratta di un **bool**, dove **true**= input penna evidenziatore, **false**= normale input penna. Viene applicato agli attributi del disegno.


```C++
GUID_HIGHLIGHTER = {9B6267B8-3968-4048-AB74-F490406A2DFA}
```



## <a name="guid_ink_style_bold"></a>\_stile inchiostro GUID in \_ \_ grassetto

Si tratta di un **bool**, dove **true**= Bold Ink, **false**= Normal. Viene applicato agli attributi del disegno.


```C++
GUID_INK_STYLE_BOLD = {E02FB5C1-9693-4312-A434-00DE7F3AD493}
```



## <a name="guid_ink_style_italics"></a>\_corsivo stile GUID input penna \_ \_

Si tratta di un **bool**, dove **true**= Ink in corsivo, **false**= Normal. Viene applicato agli attributi del disegno.


```C++
GUID_INK_STYLE_ITALICS = {05253B51-49C6-4A04-8993-64DD9ABD842A}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IJournalReader**](ijournalreader.md)
</dt> </dl>

 

 
