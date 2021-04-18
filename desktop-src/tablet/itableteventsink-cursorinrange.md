---
description: Si verifica quando uno stilo rientra nell'intervallo di rilevamento del digitalizzatore.
ms.assetid: 22be233a-fc33-4a8f-91b6-28b2f2910b69
title: 'Metodo ITabletEventSink:: CursorInRange'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorInRange
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: eec2b4f309480ecaecd50de2120d701c916b6fff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318706"
---
# <a name="itableteventsinkcursorinrange-method"></a><span data-ttu-id="69aeb-103">Metodo ITabletEventSink:: CursorInRange</span><span class="sxs-lookup"><span data-stu-id="69aeb-103">ITabletEventSink::CursorInRange method</span></span>

<span data-ttu-id="69aeb-104">Si verifica quando uno stilo rientra nell'intervallo di rilevamento del digitalizzatore.</span><span class="sxs-lookup"><span data-stu-id="69aeb-104">Occurs when a stylus comes within the digitizer's range of detection.</span></span>

## <a name="syntax"></a><span data-ttu-id="69aeb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="69aeb-105">Syntax</span></span>


```C++
HRESULT CursorInRange(
  [in] TABLET_CONTEXT_ID tcid,
       t                 cid
);
```



## <a name="parameters"></a><span data-ttu-id="69aeb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="69aeb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69aeb-107">*TCID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="69aeb-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69aeb-108">Identificatore dell'oggetto Tablet che ha rilevato lo stilo.</span><span class="sxs-lookup"><span data-stu-id="69aeb-108">The identifier of the tablet object that detected the stylus.</span></span>

</dd> <dt>

<span data-ttu-id="69aeb-109">*CID*</span><span class="sxs-lookup"><span data-stu-id="69aeb-109">*cid*</span></span> 
</dt> <dd>

<span data-ttu-id="69aeb-110">Identificatore dell'oggetto stilo che rientra nell'intervallo del digitalizzatore.</span><span class="sxs-lookup"><span data-stu-id="69aeb-110">The identifier of the stylus object that has come in range of the digitizer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69aeb-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="69aeb-111">Return value</span></span>

<span data-ttu-id="69aeb-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="69aeb-112">This method can return one of these values.</span></span>



| <span data-ttu-id="69aeb-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="69aeb-113">Return code</span></span>                                                                            | <span data-ttu-id="69aeb-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="69aeb-114">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="69aeb-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="69aeb-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="69aeb-116">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="69aeb-116">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="69aeb-117"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="69aeb-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="69aeb-118">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="69aeb-118">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="69aeb-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="69aeb-119">Requirements</span></span>



| <span data-ttu-id="69aeb-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="69aeb-120">Requirement</span></span> | <span data-ttu-id="69aeb-121">Valore</span><span class="sxs-lookup"><span data-stu-id="69aeb-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="69aeb-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="69aeb-122">Minimum supported client</span></span><br/> | <span data-ttu-id="69aeb-123">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="69aeb-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="69aeb-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="69aeb-124">Minimum supported server</span></span><br/> | <span data-ttu-id="69aeb-125">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="69aeb-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="69aeb-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="69aeb-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="69aeb-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="69aeb-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69aeb-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="69aeb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69aeb-129">**Interfaccia ITabletEventSink**</span><span class="sxs-lookup"><span data-stu-id="69aeb-129">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




