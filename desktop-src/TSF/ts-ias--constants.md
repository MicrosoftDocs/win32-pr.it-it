---
title: Costanti TS_IAS_ (Textstor. h)
description: Le \_ costanti IAS \_ di Servizi terminal vengono utilizzate come flag bit per controllare l'inserimento di testo o di oggetti incorporati in una selezione o in un punto di inserimento.
ms.assetid: 58e0d13c-d90c-41d2-bd93-4eba5fe0a69a
topic_type:
- apiref
api_name:
- TS_IAS_NOQUERY
- TS_IAS_QUERYONLY
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d59584295567c586ebd8db7e5f63366fd8272f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119862"
---
# <a name="ts_ias_-constants"></a><span data-ttu-id="777bb-103">\_Costanti IAS \_ di Servizi terminal \*</span><span class="sxs-lookup"><span data-stu-id="777bb-103">TS\_IAS\_\* Constants</span></span>

<span data-ttu-id="777bb-104">Le \_ costanti IAS di Servizi terminal \_ \* vengono utilizzate come flag bit per controllare l'inserimento di testo o oggetti incorporati in una selezione o in un punto di inserimento.</span><span class="sxs-lookup"><span data-stu-id="777bb-104">The TS\_IAS\_\* constants are used as bitfield flags to control insertion of text or embedded objects at a selection or insertion point.</span></span>



| <span data-ttu-id="777bb-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="777bb-105">Constant/value</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="777bb-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="777bb-106">Description</span></span>                                                                                                                                   |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_IAS_NOQUERY"></span><span id="ts_ias_noquery"></span><dl> <span data-ttu-id="777bb-107"><dt>**Servizi terminal \_ IAS \_ noquery**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="777bb-107"><dt>**TS\_IAS\_NOQUERY**</dt> <dt>( 0x1 )</dt></span></span> </dl>       | <span data-ttu-id="777bb-108">Il testo viene inserito e il puntatore di intervallo è impostato su **null** all'uscita.</span><span class="sxs-lookup"><span data-stu-id="777bb-108">Text is inserted and the range pointer is set to **NULL** upon exit.</span></span> <span data-ttu-id="777bb-109">Non può essere combinato con il \_ flag QUERYONLY IAS di Servizi terminal \_ .</span><span class="sxs-lookup"><span data-stu-id="777bb-109">Cannot be combined with the TS\_IAS\_QUERYONLY flag.</span></span><br/>          |
| <span id="TS_IAS_QUERYONLY"></span><span id="ts_ias_queryonly"></span><dl> <span data-ttu-id="777bb-110"><dt>**Servizi terminal \_ IAS \_ QUERYONLY**</dt> <dt>(0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="777bb-110"><dt>**TS\_IAS\_QUERYONLY**</dt> <dt>( 0x2 )</dt></span></span> </dl> | <span data-ttu-id="777bb-111">Non eseguire l'inserimento.</span><span class="sxs-lookup"><span data-stu-id="777bb-111">Do not perform the insertion.</span></span> <span data-ttu-id="777bb-112">Il chiamante richiede l'impostazione del puntatore di intervallo.</span><span class="sxs-lookup"><span data-stu-id="777bb-112">Caller only requires the range pointer to be set.</span></span> <span data-ttu-id="777bb-113">Non possono essere combinati con \_ il \_ flag noquery IAS di Servizi terminal.</span><span class="sxs-lookup"><span data-stu-id="777bb-113">Cannot be combined with the TS\_IAS\_NOQUERY flag.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="777bb-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="777bb-114">Requirements</span></span>



| <span data-ttu-id="777bb-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="777bb-115">Requirement</span></span> | <span data-ttu-id="777bb-116">Valore</span><span class="sxs-lookup"><span data-stu-id="777bb-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="777bb-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="777bb-117">Minimum supported client</span></span><br/> | <span data-ttu-id="777bb-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="777bb-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="777bb-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="777bb-119">Minimum supported server</span></span><br/> | <span data-ttu-id="777bb-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="777bb-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="777bb-121">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="777bb-121">Redistributable</span></span><br/>          | <span data-ttu-id="777bb-122">TSF 1,0 su Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="777bb-122">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="777bb-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="777bb-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="777bb-124"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="777bb-124"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="777bb-125">IDL</span><span class="sxs-lookup"><span data-stu-id="777bb-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="777bb-126"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="777bb-126"><dt>Textstor.idl</dt></span></span> </dl> |



 

 





