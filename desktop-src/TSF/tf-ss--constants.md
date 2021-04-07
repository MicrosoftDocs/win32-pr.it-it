---
title: Costanti TF_SS_ (msctf. h)
description: Le \_ costanti TF SS \_ \, definite prima della fase di esecuzione nella \_ struttura di stato TF, descrivono gli Stati dei documenti statici.
ms.assetid: 371aeeda-f081-4506-ba51-79c6a8bc8768
topic_type:
- apiref
api_name:
- TF_SS_DISJOINTSEL
- TF_SS_REGIONS
- TF_SS_TRANSITORY
- TF_SS_TKBAUTOCORRECTENABLE
- TF_SS_TKBPREDICTIONENABLE
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1028b78e74ed10c572feb904baa8ec395087ee3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048468"
---
# <a name="tf_ss_-constants"></a><span data-ttu-id="90175-103">\_Costanti TF SS \_ \*</span><span class="sxs-lookup"><span data-stu-id="90175-103">TF\_SS\_\* Constants</span></span>

<span data-ttu-id="90175-104">Le \_ costanti TF SS \_ \* , definite prima della fase di esecuzione nella struttura di [**\_ stato TF**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85)) , descrivono gli Stati dei documenti statici.</span><span class="sxs-lookup"><span data-stu-id="90175-104">The TF\_SS\_\* constants, defined before run time in the [**TF\_STATUS**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85)) structure, describe static document states.</span></span>



| <span data-ttu-id="90175-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="90175-105">Constant/value</span></span>                                                                                                                                                                                                                                                                              | <span data-ttu-id="90175-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="90175-106">Description</span></span>                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| <span id="TF_SS_DISJOINTSEL"></span><span id="tf_ss_disjointsel"></span><dl> <span data-ttu-id="90175-107"><dt>**Tf \_ SS \_ DISJOINTSEL**</dt> <dt>(TS \_ SS \_ DISJOINTSEL)</dt></span><span class="sxs-lookup"><span data-stu-id="90175-107"><dt>**TF\_SS\_DISJOINTSEL**</dt> <dt>( TS\_SS\_DISJOINTSEL )</dt></span></span> </dl>                                     | <span data-ttu-id="90175-108">Il documento supporta selezioni multiple.</span><span class="sxs-lookup"><span data-stu-id="90175-108">The document supports multiple selections.</span></span><br/>                                                          |
| <span id="TF_SS_REGIONS"></span><span id="tf_ss_regions"></span><dl> <span data-ttu-id="90175-109"><dt>**Tf \_ \_aree SS**</dt> <dt>( \_ aree SS \_ di servizi Terminal)</dt></span><span class="sxs-lookup"><span data-stu-id="90175-109"><dt>**TF\_SS\_REGIONS**</dt> <dt>( TS\_SS\_REGIONS )</dt></span></span> </dl>                                                     | <span data-ttu-id="90175-110">Il documento può contenere più aree.</span><span class="sxs-lookup"><span data-stu-id="90175-110">The document can contain multiple regions.</span></span><br/>                                                          |
| <span id="TF_SS_TRANSITORY"></span><span id="tf_ss_transitory"></span><dl> <span data-ttu-id="90175-111"><dt>**Tf \_ SS \_ transitorio**</dt> <dt>(TS \_ SS \_ transitorio)</dt></span><span class="sxs-lookup"><span data-stu-id="90175-111"><dt>**TF\_SS\_TRANSITORY**</dt> <dt>( TS\_SS\_TRANSITORY )</dt></span></span> </dl>                                         | <span data-ttu-id="90175-112">Si prevede un breve ciclo di utilizzo del documento.</span><span class="sxs-lookup"><span data-stu-id="90175-112">The document is expected to have a short usage cycle.</span></span><br/>                                               |
| <span id="TF_SS_TKBAUTOCORRECTENABLE"></span><span id="tf_ss_tkbautocorrectenable"></span><dl> <span data-ttu-id="90175-113"><dt>**Tf \_ SS \_ TKBAUTOCORRECTENABLE**</dt> <dt>(TS \_ SS \_ TKBAUTOCORRECTENABLE)</dt></span><span class="sxs-lookup"><span data-stu-id="90175-113"><dt>**TF\_SS\_TKBAUTOCORRECTENABLE**</dt> <dt>( TS\_SS\_TKBAUTOCORRECTENABLE )</dt></span></span> </dl> | <span data-ttu-id="90175-114">**A partire da Windows 8:** Il documento supporta la correzione automatica fornita dalla tastiera touch.</span><span class="sxs-lookup"><span data-stu-id="90175-114">**Starting with Windows 8:** The document supports autocorrection provided by the touch keyboard.</span></span><br/>   |
| <span id="TF_SS_TKBPREDICTIONENABLE"></span><span id="tf_ss_tkbpredictionenable"></span><dl> <span data-ttu-id="90175-115"><dt>**Tf \_ SS \_ TKBPREDICTIONENABLE**</dt> <dt>(TS \_ SS \_ TKBPREDICTIONENABLE)</dt></span><span class="sxs-lookup"><span data-stu-id="90175-115"><dt>**TF\_SS\_TKBPREDICTIONENABLE**</dt> <dt>( TS\_SS\_TKBPREDICTIONENABLE )</dt></span></span> </dl>     | <span data-ttu-id="90175-116">**A partire da Windows 8:** Il documento supporta i suggerimenti di testo forniti dalla tastiera touch.</span><span class="sxs-lookup"><span data-stu-id="90175-116">**Starting with Windows 8:** The document supports text suggestions provided by the touch keyboard.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="90175-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="90175-117">Remarks</span></span>

<span data-ttu-id="90175-118">Il membro **dwStaticFlags** della struttura di \_ stato TF usa queste costanti.</span><span class="sxs-lookup"><span data-stu-id="90175-118">The **dwStaticFlags** member of the TF\_STATUS structure uses these constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="90175-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="90175-119">Requirements</span></span>



| <span data-ttu-id="90175-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="90175-120">Requirement</span></span> | <span data-ttu-id="90175-121">Valore</span><span class="sxs-lookup"><span data-stu-id="90175-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="90175-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="90175-122">Minimum supported client</span></span><br/> | <span data-ttu-id="90175-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="90175-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="90175-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="90175-124">Minimum supported server</span></span><br/> | <span data-ttu-id="90175-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="90175-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="90175-126">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="90175-126">Redistributable</span></span><br/>          | <span data-ttu-id="90175-127">TSF 1,0 su Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="90175-127">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="90175-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="90175-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="90175-129"><dt>Msctf. h</dt></span><span class="sxs-lookup"><span data-stu-id="90175-129"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="90175-130">IDL</span><span class="sxs-lookup"><span data-stu-id="90175-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="90175-131"><dt>Msctf. idl</dt></span><span class="sxs-lookup"><span data-stu-id="90175-131"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90175-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="90175-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="90175-133">[**\_stato TF**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="90175-133">[**TF\_STATUS**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))</span></span>
</dt> </dl>

 

