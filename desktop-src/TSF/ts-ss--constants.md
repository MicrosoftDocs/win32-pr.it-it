---
title: Costanti TS_SS_ (Textstor. h)
description: Le \_ costanti SS \_ \ ts \, definite prima della fase di esecuzione nella \_ struttura di stato TS, descrivono gli Stati dei documenti statici.
ms.assetid: 17264527-946a-4648-a4eb-30db751602ab
topic_type:
- apiref
api_name:
- TS_SS_DISJOINTSEL
- TS_SS_REGIONS
- TS_SS_TRANSITORY
- TS_SS_NOHIDDENTEXT
- TS_SS_TKBAUTOCORRECTENABLE
- TS_SS_TKBPREDICTIONENABLE
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 773645b8a75b7e8eeafa40ed9fa95067743628d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301061"
---
# <a name="ts_ss_-constants"></a><span data-ttu-id="c1168-103">\_Costanti SS \_ di Servizi terminal \*</span><span class="sxs-lookup"><span data-stu-id="c1168-103">TS\_SS\_\* Constants</span></span>

<span data-ttu-id="c1168-104">Le \_ costanti SS di Servizi terminal \_ \* , definite prima della fase di esecuzione nella struttura di [**\_ stato TS**](/windows/desktop/api/Textstor/ns-textstor-ts_status) , descrivono gli Stati dei documenti statici.</span><span class="sxs-lookup"><span data-stu-id="c1168-104">The TS\_SS\_\* constants, defined before run time in the [**TS\_STATUS**](/windows/desktop/api/Textstor/ns-textstor-ts_status) structure, describe static document states.</span></span>



| <span data-ttu-id="c1168-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="c1168-105">Constant/value</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="c1168-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c1168-106">Description</span></span>                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| <span id="TS_SS_DISJOINTSEL"></span><span id="ts_ss_disjointsel"></span><dl> <span data-ttu-id="c1168-107"><dt>**Servizi terminal \_ SS \_ DISJOINTSEL**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="c1168-107"><dt>**TS\_SS\_DISJOINTSEL**</dt> <dt>( 0x1 )</dt></span></span> </dl>                             | <span data-ttu-id="c1168-108">Il documento supporta selezioni multiple.</span><span class="sxs-lookup"><span data-stu-id="c1168-108">The document supports multiple selections.</span></span><br/>                                                          |
| <span id="TS_SS_REGIONS"></span><span id="ts_ss_regions"></span><dl> <span data-ttu-id="c1168-109"><dt>**Servizi terminal \_ \_Aree SS**</dt> <dt>(0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="c1168-109"><dt>**TS\_SS\_REGIONS**</dt> <dt>( 0x2 )</dt></span></span> </dl>                                         | <span data-ttu-id="c1168-110">Il documento può contenere più aree.</span><span class="sxs-lookup"><span data-stu-id="c1168-110">The document can contain multiple regions.</span></span><br/>                                                          |
| <span id="TS_SS_TRANSITORY"></span><span id="ts_ss_transitory"></span><dl> <span data-ttu-id="c1168-111"><dt>**Servizi terminal \_ SS \_ transitorio**</dt> <dt>(0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="c1168-111"><dt>**TS\_SS\_TRANSITORY**</dt> <dt>( 0x4 )</dt></span></span> </dl>                                | <span data-ttu-id="c1168-112">Si prevede un breve ciclo di utilizzo del documento.</span><span class="sxs-lookup"><span data-stu-id="c1168-112">The document is expected to have a short usage cycle.</span></span><br/>                                               |
| <span id="TS_SS_NOHIDDENTEXT"></span><span id="ts_ss_nohiddentext"></span><dl> <span data-ttu-id="c1168-113"><dt>**Servizi terminal \_ SS \_ NOHIDDENTEXT**</dt> <dt>(0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="c1168-113"><dt>**TS\_SS\_NOHIDDENTEXT**</dt> <dt>( 0x8 )</dt></span></span> </dl>                          | <span data-ttu-id="c1168-114">Il documento non conterrà mai il testo nascosto.</span><span class="sxs-lookup"><span data-stu-id="c1168-114">The document will never contain hidden text.</span></span><br/>                                                        |
| <span id="TS_SS_TKBAUTOCORRECTENABLE"></span><span id="ts_ss_tkbautocorrectenable"></span><dl> <span data-ttu-id="c1168-115"><dt>**Servizi terminal \_ SS \_ TKBAUTOCORRECTENABLE**</dt> <dt>(0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="c1168-115"><dt>**TS\_SS\_TKBAUTOCORRECTENABLE**</dt> <dt>( 0x10 )</dt></span></span> </dl> | <span data-ttu-id="c1168-116">**A partire da Windows 8:** Il documento supporta la correzione automatica fornita dalla tastiera touch.</span><span class="sxs-lookup"><span data-stu-id="c1168-116">**Starting with Windows 8:** The document supports autocorrection provided by the touch keyboard.</span></span><br/>   |
| <span id="TS_SS_TKBPREDICTIONENABLE"></span><span id="ts_ss_tkbpredictionenable"></span><dl> <span data-ttu-id="c1168-117"><dt>**Servizi terminal \_ SS \_ TKBPREDICTIONENABLE**</dt> <dt>(0x20)</dt></span><span class="sxs-lookup"><span data-stu-id="c1168-117"><dt>**TS\_SS\_TKBPREDICTIONENABLE**</dt> <dt>( 0x20 )</dt></span></span> </dl>    | <span data-ttu-id="c1168-118">**A partire da Windows 8:** Il documento supporta i suggerimenti di testo forniti dalla tastiera touch.</span><span class="sxs-lookup"><span data-stu-id="c1168-118">**Starting with Windows 8:** The document supports text suggestions provided by the touch keyboard.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c1168-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="c1168-119">Remarks</span></span>

<span data-ttu-id="c1168-120">Il membro **dwStaticFlags** della struttura **di \_ stato TS** usa queste costanti.</span><span class="sxs-lookup"><span data-stu-id="c1168-120">The **dwStaticFlags** member of the **TS\_STATUS** structure uses these constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1168-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c1168-121">Requirements</span></span>



| <span data-ttu-id="c1168-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1168-122">Requirement</span></span> | <span data-ttu-id="c1168-123">Valore</span><span class="sxs-lookup"><span data-stu-id="c1168-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1168-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1168-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c1168-125">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c1168-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c1168-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1168-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c1168-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c1168-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c1168-128">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="c1168-128">Redistributable</span></span><br/>          | <span data-ttu-id="c1168-129">TSF 1,0 su Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c1168-129">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="c1168-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c1168-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1168-131"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1168-131"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="c1168-132">IDL</span><span class="sxs-lookup"><span data-stu-id="c1168-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c1168-133"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c1168-133"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1168-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c1168-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1168-135">**stato di Servizi terminal \_**</span><span class="sxs-lookup"><span data-stu-id="c1168-135">**TS\_STATUS**</span></span>](/windows/desktop/api/Textstor/ns-textstor-ts_status)
</dt> <dt>

<span data-ttu-id="c1168-136">[**\_stato TF**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c1168-136">[**TF\_STATUS**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))</span></span>
</dt> </dl>

 

