---
description: Si verifica quando lo stilo lascia l'intervallo di rilevamento fisico (prossimità) del tablet.
ms.assetid: ded01278-126d-415d-9a7b-1e6fe3650a37
title: 'Metodo ITabletEventSink:: CursorOutOfRange'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorOutOfRange
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: e2250401f3888bd07ff250549c11c34e6a54576d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885322"
---
# <a name="itableteventsinkcursoroutofrange-method"></a><span data-ttu-id="8bdc1-103">Metodo ITabletEventSink:: CursorOutOfRange</span><span class="sxs-lookup"><span data-stu-id="8bdc1-103">ITabletEventSink::CursorOutOfRange method</span></span>

<span data-ttu-id="8bdc1-104">Si verifica quando lo stilo lascia l'intervallo di rilevamento fisico (prossimità) del tablet.</span><span class="sxs-lookup"><span data-stu-id="8bdc1-104">Occurs when the stylus leaves the physical detection range (proximity) of the tablet.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bdc1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8bdc1-105">Syntax</span></span>


```C++
HRESULT CursorOutOfRange(
  [in] TABLET_CONTEXT_ID tcid,
       t                 cid
);
```



## <a name="parameters"></a><span data-ttu-id="8bdc1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8bdc1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8bdc1-107">*TCID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8bdc1-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8bdc1-108">Identificatore del tablet.</span><span class="sxs-lookup"><span data-stu-id="8bdc1-108">The identifier of the tablet.</span></span>

</dd> <dt>

<span data-ttu-id="8bdc1-109">*CID*</span><span class="sxs-lookup"><span data-stu-id="8bdc1-109">*cid*</span></span> 
</dt> <dd>

<span data-ttu-id="8bdc1-110">Identificatore dello stilo.</span><span class="sxs-lookup"><span data-stu-id="8bdc1-110">The identifier of the stylus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8bdc1-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8bdc1-111">Return value</span></span>

<span data-ttu-id="8bdc1-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="8bdc1-112">This method can return one of these values.</span></span>



| <span data-ttu-id="8bdc1-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="8bdc1-113">Return code</span></span>                                                                            | <span data-ttu-id="8bdc1-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8bdc1-114">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="8bdc1-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8bdc1-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="8bdc1-116">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="8bdc1-116">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="8bdc1-117"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="8bdc1-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="8bdc1-118">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="8bdc1-118">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8bdc1-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8bdc1-119">Requirements</span></span>



| <span data-ttu-id="8bdc1-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8bdc1-120">Requirement</span></span> | <span data-ttu-id="8bdc1-121">Valore</span><span class="sxs-lookup"><span data-stu-id="8bdc1-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8bdc1-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8bdc1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8bdc1-123">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="8bdc1-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="8bdc1-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8bdc1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8bdc1-125">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="8bdc1-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="8bdc1-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="8bdc1-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="8bdc1-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8bdc1-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bdc1-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8bdc1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bdc1-129">**Interfaccia ITabletEventSink**</span><span class="sxs-lookup"><span data-stu-id="8bdc1-129">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




