---
description: Si verifica quando un nuovo stilo viene aggiunto al sistema.
ms.assetid: bd0f0d2a-c0d9-48fc-bc90-f63f038639f3
title: 'Metodo ITabletEventSink:: CursorNew'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorNew
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 31db152eb15d6f980234dc556e277691d3f14959
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233873"
---
# <a name="itableteventsinkcursornew-method"></a><span data-ttu-id="7168d-103">Metodo ITabletEventSink:: CursorNew</span><span class="sxs-lookup"><span data-stu-id="7168d-103">ITabletEventSink::CursorNew method</span></span>

<span data-ttu-id="7168d-104">Si verifica quando un nuovo stilo viene aggiunto al sistema.</span><span class="sxs-lookup"><span data-stu-id="7168d-104">Occurs when a new stylus is added to the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="7168d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7168d-105">Syntax</span></span>


```C++
HRESULT CursorNew(
  [in] TABLET_CONTEXT_ID tcid,
       t                 cid
);
```



## <a name="parameters"></a><span data-ttu-id="7168d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7168d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7168d-107">*TCID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7168d-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7168d-108">Identificatore del contesto della tavoletta in cui è stato aggiunto il nuovo stilo.</span><span class="sxs-lookup"><span data-stu-id="7168d-108">The identifier of the tablet context where the new stylus was added.</span></span>

</dd> <dt>

<span data-ttu-id="7168d-109">*CID*</span><span class="sxs-lookup"><span data-stu-id="7168d-109">*cid*</span></span> 
</dt> <dd>

<span data-ttu-id="7168d-110">Identificatore del nuovo oggetto stilo.</span><span class="sxs-lookup"><span data-stu-id="7168d-110">The identifier of the new stylus object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7168d-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7168d-111">Return value</span></span>

<span data-ttu-id="7168d-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="7168d-112">This method can return one of these values.</span></span>



| <span data-ttu-id="7168d-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="7168d-113">Return code</span></span>                                                                            | <span data-ttu-id="7168d-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7168d-114">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="7168d-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7168d-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="7168d-116">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="7168d-116">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="7168d-117"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="7168d-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="7168d-118">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="7168d-118">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7168d-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7168d-119">Requirements</span></span>



| <span data-ttu-id="7168d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7168d-120">Requirement</span></span> | <span data-ttu-id="7168d-121">Valore</span><span class="sxs-lookup"><span data-stu-id="7168d-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7168d-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7168d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7168d-123">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="7168d-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="7168d-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7168d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7168d-125">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="7168d-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="7168d-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="7168d-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="7168d-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7168d-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7168d-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7168d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7168d-129">**Interfaccia ITabletEventSink**</span><span class="sxs-lookup"><span data-stu-id="7168d-129">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




