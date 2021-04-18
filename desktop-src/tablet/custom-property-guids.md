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
# <a name="custom-property-guids"></a><span data-ttu-id="04a45-103">GUID proprietà personalizzati</span><span class="sxs-lookup"><span data-stu-id="04a45-103">Custom Property GUIDs</span></span>

<span data-ttu-id="04a45-104">I seguenti identificatori univoci globali (GUID) vengono usati da Windows Journal per identificare le proprietà personalizzate nei tratti o negli attributi di disegno.</span><span class="sxs-lookup"><span data-stu-id="04a45-104">The following globally unique identifiers (GUIDs) are used by Windows Journal to identify custom properties on strokes or drawing attributes.</span></span>

## <a name="guid_stroke_timestamp"></a><span data-ttu-id="04a45-105">\_timestamp del tratto GUID \_</span><span class="sxs-lookup"><span data-stu-id="04a45-105">GUID\_STROKE\_TIMESTAMP</span></span>


```C++
GUID_STROKE_TIMESTAMP = {4EA66C4-F33A-461B-B8FE-68070D9C7575}
```



<span data-ttu-id="04a45-106">Si tratta di una struttura [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) che indica l'ora in cui il tratto è stato creato o aggiunto al documento.</span><span class="sxs-lookup"><span data-stu-id="04a45-106">This is a [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure that indicates the time at which the stroke was created or added to the document.</span></span>


```C++
typedef struct _FILETIME {
    DWORD dwLowDateTime;
    DWORD dwHighDateTime;
} FILETIME, *PFILETIME;
```



## <a name="guid_stroke_timeid"></a><span data-ttu-id="04a45-107">\_TimeID tratto \_ GUID</span><span class="sxs-lookup"><span data-stu-id="04a45-107">GUID\_STROKE\_TIMEID</span></span>


```C++
GUID_STROKE_TIMEID = {50B6BC8-3B7D-4816-8C61-BC7E905B2132}
```



<span data-ttu-id="04a45-108">Si tratta di una struttura **TimeID** .</span><span class="sxs-lookup"><span data-stu-id="04a45-108">This is a **TIMEID** structure.</span></span> <span data-ttu-id="04a45-109">Consente di mantenere l'ordine del tratto tra le operazioni di Incolla e rilascio.</span><span class="sxs-lookup"><span data-stu-id="04a45-109">It allows stroke order to be maintained across paste and drop operations.</span></span> <span data-ttu-id="04a45-110">Senza la struttura **TimeID** , il timestamp per tutti gli oggetti dell' [**interfaccia IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) tagliati e incollati in una [raccolta InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) sarà lo stesso.</span><span class="sxs-lookup"><span data-stu-id="04a45-110">Without the **TIMEID** structure, the timestamp for all [**IInkStrokeDisp Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects cut and pasted in a [InkStrokes Collection](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) will be the same.</span></span>


```C++
typedef struct tagTIMEID {
    FILETIME  tmFiletime;
    ULONG     uiOrder;
} TIMEID;
```



## <a name="guid_highlighter"></a><span data-ttu-id="04a45-111">\_evidenziatore GUID</span><span class="sxs-lookup"><span data-stu-id="04a45-111">GUID\_HIGHLIGHTER</span></span>

<span data-ttu-id="04a45-112">Si tratta di un **bool**, dove **true**= input penna evidenziatore, **false**= normale input penna.</span><span class="sxs-lookup"><span data-stu-id="04a45-112">This is a **BOOL**, where **TRUE**=highlighter ink, **FALSE**=regular ink.</span></span> <span data-ttu-id="04a45-113">Viene applicato agli attributi del disegno.</span><span class="sxs-lookup"><span data-stu-id="04a45-113">This is applied to drawing attributes.</span></span>


```C++
GUID_HIGHLIGHTER = {9B6267B8-3968-4048-AB74-F490406A2DFA}
```



## <a name="guid_ink_style_bold"></a><span data-ttu-id="04a45-114">\_stile inchiostro GUID in \_ \_ grassetto</span><span class="sxs-lookup"><span data-stu-id="04a45-114">GUID\_INK\_STYLE\_BOLD</span></span>

<span data-ttu-id="04a45-115">Si tratta di un **bool**, dove **true**= Bold Ink, **false**= Normal.</span><span class="sxs-lookup"><span data-stu-id="04a45-115">This is a **BOOL**, where **TRUE**=bold ink, **FALSE**=normal.</span></span> <span data-ttu-id="04a45-116">Viene applicato agli attributi del disegno.</span><span class="sxs-lookup"><span data-stu-id="04a45-116">This is applied to drawing attributes.</span></span>


```C++
GUID_INK_STYLE_BOLD = {E02FB5C1-9693-4312-A434-00DE7F3AD493}
```



## <a name="guid_ink_style_italics"></a><span data-ttu-id="04a45-117">\_corsivo stile GUID input penna \_ \_</span><span class="sxs-lookup"><span data-stu-id="04a45-117">GUID\_INK\_STYLE\_ITALICS</span></span>

<span data-ttu-id="04a45-118">Si tratta di un **bool**, dove **true**= Ink in corsivo, **false**= Normal.</span><span class="sxs-lookup"><span data-stu-id="04a45-118">This is a **BOOL**, where **TRUE**=italicized ink, **FALSE**=normal.</span></span> <span data-ttu-id="04a45-119">Viene applicato agli attributi del disegno.</span><span class="sxs-lookup"><span data-stu-id="04a45-119">This is applied to drawing attributes.</span></span>


```C++
GUID_INK_STYLE_ITALICS = {05253B51-49C6-4A04-8993-64DD9ABD842A}
```



## <a name="related-topics"></a><span data-ttu-id="04a45-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="04a45-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04a45-121">**Interfaccia IJournalReader**</span><span class="sxs-lookup"><span data-stu-id="04a45-121">**IJournalReader Interface**</span></span>](ijournalreader.md)
</dt> </dl>

 

 
