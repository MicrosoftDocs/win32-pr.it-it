---
title: Costanti TS_AS_ (Textstor. h)
description: I flag seguenti specificano gli eventi che chiamano i metodi AdviseSink.
ms.assetid: 8f406b67-f846-4712-b4be-811dbcc6ad55
topic_type:
- apiref
api_name:
- TS_AS_TEXT_CHANGE
- TS_AS_SEL_CHANGE
- TS_AS_LAYOUT_CHANGE
- TS_AS_ATTR_CHANGE
- TS_AS_STATUS_CHANGE
- TS_AS_ALL_SINKS
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c7b36bdc2c3b559693503b2a8e408a0782855f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302233"
---
# <a name="ts_as_-constants"></a><span data-ttu-id="1cbf2-103">\_Costanti di \_ Servizi terminal \*</span><span class="sxs-lookup"><span data-stu-id="1cbf2-103">TS\_AS\_\* Constants</span></span>

<span data-ttu-id="1cbf2-104">I flag seguenti specificano gli eventi che chiamano i metodi **adviseSink** .</span><span class="sxs-lookup"><span data-stu-id="1cbf2-104">The following flags specify the events that call the **AdviseSink** methods.</span></span>



| <span data-ttu-id="1cbf2-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="1cbf2-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                                                                         | <span data-ttu-id="1cbf2-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1cbf2-106">Description</span></span>                                                          |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| <span id="TS_AS_TEXT_CHANGE"></span><span id="ts_as_text_change"></span><dl> <span data-ttu-id="1cbf2-107"><dt>**Servizi terminal \_ COME \_ \_ modifica del testo**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="1cbf2-107"><dt>**TS\_AS\_TEXT\_CHANGE**</dt> <dt>( 0x1 )</dt></span></span> </dl>                                                                                                               | <span data-ttu-id="1cbf2-108">Il testo viene modificato nel documento.</span><span class="sxs-lookup"><span data-stu-id="1cbf2-108">Text is changed in the document.</span></span><br/>                          |
| <span id="TS_AS_SEL_CHANGE"></span><span id="ts_as_sel_change"></span><dl> <span data-ttu-id="1cbf2-109"><dt>**Servizi terminal \_ COME \_ \_ modifica SEL**</dt> <dt>(0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="1cbf2-109"><dt>**TS\_AS\_SEL\_CHANGE**</dt> <dt>( 0x2 )</dt></span></span> </dl>                                                                                                                  | <span data-ttu-id="1cbf2-110">Il testo è selezionato nel documento.</span><span class="sxs-lookup"><span data-stu-id="1cbf2-110">Text is selected in the document.</span></span><br/>                         |
| <span id="TS_AS_LAYOUT_CHANGE"></span><span id="ts_as_layout_change"></span><dl> <span data-ttu-id="1cbf2-111"><dt>**Servizi terminal \_ COME \_ \_ modifica del layout**</dt> <dt>(0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="1cbf2-111"><dt>**TS\_AS\_LAYOUT\_CHANGE**</dt> <dt>( 0x4 )</dt></span></span> </dl>                                                                                                         | <span data-ttu-id="1cbf2-112">Il layout del documento è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="1cbf2-112">The layout of the document is changed.</span></span><br/>                    |
| <span id="TS_AS_ATTR_CHANGE"></span><span id="ts_as_attr_change"></span><dl> <span data-ttu-id="1cbf2-113"><dt>**Servizi terminal \_ AS \_ attr \_ Change**</dt> <dt>(0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="1cbf2-113"><dt>**TS\_AS\_ATTR\_CHANGE**</dt> <dt>( 0x8 )</dt></span></span> </dl>                                                                                                               | <span data-ttu-id="1cbf2-114">Gli attributi del documento vengono modificati.</span><span class="sxs-lookup"><span data-stu-id="1cbf2-114">The attributes of the document is changed.</span></span><br/>                |
| <span id="TS_AS_STATUS_CHANGE"></span><span id="ts_as_status_change"></span><dl> <span data-ttu-id="1cbf2-115"><dt>**Servizi terminal \_ COME \_ \_ modifica dello stato**</dt> <dt>(0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="1cbf2-115"><dt>**TS\_AS\_STATUS\_CHANGE**</dt> <dt>( 0x10 )</dt></span></span> </dl>                                                                                                        | <span data-ttu-id="1cbf2-116">Lo stato del documento è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="1cbf2-116">The status of the document is changed.</span></span><br/>                    |
| <span id="TS_AS_ALL_SINKS"></span><span id="ts_as_all_sinks"></span><dl> <span data-ttu-id="1cbf2-117"><dt>**Servizi terminal \_ COME \_ tutti i \_ sink**</dt> <dt>(TS \_ come \_ testo \_ modificano \| TS \_ come \_ SEL \_ modificare \| TS \_ come layout modificare TS come \_ \_ \| \_ \_ attr \_ modificare TS come \| \_ \_ \_ modifica dello stato)</dt></span><span class="sxs-lookup"><span data-stu-id="1cbf2-117"><dt>**TS\_AS\_ALL\_SINKS**</dt> <dt>( TS\_AS\_TEXT\_CHANGE \| TS\_AS\_SEL\_CHANGE \| TS\_AS\_LAYOUT\_CHANGE \| TS\_AS\_ATTR\_CHANGE \| TS\_AS\_STATUS\_CHANGE )</dt></span></span> </dl> | <span data-ttu-id="1cbf2-118">Uno dei quattro eventi precedenti si è verificato nel documento.</span><span class="sxs-lookup"><span data-stu-id="1cbf2-118">One of the previous four events occurred in the document.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="1cbf2-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1cbf2-119">Requirements</span></span>



| <span data-ttu-id="1cbf2-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cbf2-120">Requirement</span></span> | <span data-ttu-id="1cbf2-121">Valore</span><span class="sxs-lookup"><span data-stu-id="1cbf2-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1cbf2-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1cbf2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1cbf2-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1cbf2-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1cbf2-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1cbf2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1cbf2-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1cbf2-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1cbf2-126">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="1cbf2-126">Redistributable</span></span><br/>          | <span data-ttu-id="1cbf2-127">TSF 1,0 su Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1cbf2-127">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="1cbf2-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1cbf2-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="1cbf2-129"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="1cbf2-129"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="1cbf2-130">IDL</span><span class="sxs-lookup"><span data-stu-id="1cbf2-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1cbf2-131"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1cbf2-131"><dt>Textstor.idl</dt></span></span> </dl> |



 

 





