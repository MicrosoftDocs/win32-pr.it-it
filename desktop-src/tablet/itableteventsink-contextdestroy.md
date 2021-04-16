---
description: Si verifica quando un contesto del Tablet viene eliminato definitivamente.
ms.assetid: 805289d8-267e-488b-8092-6b07b37dd6d4
title: 'Metodo ITabletEventSink:: ContextDestroy'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.ContextDestroy
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: c9b5d78d4ce4032c1a7a2082fb749afc5a39949a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530031"
---
# <a name="itableteventsinkcontextdestroy-method"></a><span data-ttu-id="f97dd-103">Metodo ITabletEventSink:: ContextDestroy</span><span class="sxs-lookup"><span data-stu-id="f97dd-103">ITabletEventSink::ContextDestroy method</span></span>

<span data-ttu-id="f97dd-104">Si verifica quando un contesto del Tablet viene eliminato definitivamente.</span><span class="sxs-lookup"><span data-stu-id="f97dd-104">Occurs when a tablet context is being destroyed.</span></span>

## <a name="syntax"></a><span data-ttu-id="f97dd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f97dd-105">Syntax</span></span>


```C++
HRESULT ContextDestroy(
  [in] TABLET_CONTEXT_ID tcid
);
```



## <a name="parameters"></a><span data-ttu-id="f97dd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f97dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f97dd-107">*TCID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f97dd-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f97dd-108">Identificatore del contesto del tablet da eliminare definitivamente.</span><span class="sxs-lookup"><span data-stu-id="f97dd-108">The identifier of the tablet context being destroyed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f97dd-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f97dd-109">Return value</span></span>

<span data-ttu-id="f97dd-110">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="f97dd-110">This method can return one of these values.</span></span>



| <span data-ttu-id="f97dd-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="f97dd-111">Return code</span></span>                                                                            | <span data-ttu-id="f97dd-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f97dd-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="f97dd-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f97dd-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="f97dd-114">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="f97dd-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="f97dd-115"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="f97dd-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="f97dd-116">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="f97dd-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f97dd-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f97dd-117">Requirements</span></span>



| <span data-ttu-id="f97dd-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f97dd-118">Requirement</span></span> | <span data-ttu-id="f97dd-119">Valore</span><span class="sxs-lookup"><span data-stu-id="f97dd-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f97dd-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f97dd-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f97dd-121">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="f97dd-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="f97dd-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f97dd-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f97dd-123">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f97dd-123">None supported</span></span><br/>                                                              |
| <span data-ttu-id="f97dd-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="f97dd-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="f97dd-125"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f97dd-125"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f97dd-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f97dd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f97dd-127">**Interfaccia ITabletEventSink**</span><span class="sxs-lookup"><span data-stu-id="f97dd-127">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




