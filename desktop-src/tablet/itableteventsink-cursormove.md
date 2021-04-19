---
description: Si verifica quando il cursore viene spostato sul digitalizzatore del tablet.
ms.assetid: cd2863af-59a9-4dd0-a679-84861a70ef53
title: 'Metodo ITabletEventSink:: CursorMove'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorMove
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: f6950e0b30c1b8fc8ccf3e60a8aaa05b9eeb3215
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317922"
---
# <a name="itableteventsinkcursormove-method"></a><span data-ttu-id="678c9-103">Metodo ITabletEventSink:: CursorMove</span><span class="sxs-lookup"><span data-stu-id="678c9-103">ITabletEventSink::CursorMove method</span></span>

<span data-ttu-id="678c9-104">Si verifica quando il cursore viene spostato sul digitalizzatore del tablet.</span><span class="sxs-lookup"><span data-stu-id="678c9-104">Occurs when the cursor moves over the tablet digitizer.</span></span>

## <a name="syntax"></a><span data-ttu-id="678c9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="678c9-105">Syntax</span></span>


```C++
HRESULT CursorMove(
   TABLET_CONTEXT_ID tcid,
   CURSOR_ID         cid,
   HWND              hWnd,
   LONG              xPos,
   LONG              yPos
);
```



## <a name="parameters"></a><span data-ttu-id="678c9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="678c9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="678c9-107">*TCID*</span><span class="sxs-lookup"><span data-stu-id="678c9-107">*tcid*</span></span> 
</dt> <dd>

<span data-ttu-id="678c9-108">Dentifier univoco del digitalizzatore del tablet.</span><span class="sxs-lookup"><span data-stu-id="678c9-108">Unique dentifier of the tablet digitizer.</span></span>

</dd> <dt>

<span data-ttu-id="678c9-109">*CID*</span><span class="sxs-lookup"><span data-stu-id="678c9-109">*cid*</span></span> 
</dt> <dd>

<span data-ttu-id="678c9-110">Identificatore univoco dello stilo del tablet.</span><span class="sxs-lookup"><span data-stu-id="678c9-110">Unique identifier of the tablet stylus.</span></span>

</dd> <dt>

<span data-ttu-id="678c9-111">*hWnd*</span><span class="sxs-lookup"><span data-stu-id="678c9-111">*hWnd*</span></span> 
</dt> <dd>

<span data-ttu-id="678c9-112">Finestra su cui è stato spostato il cursore.</span><span class="sxs-lookup"><span data-stu-id="678c9-112">The window over which the cursor moved.</span></span>

</dd> <dt>

<span data-ttu-id="678c9-113">*xPos*</span><span class="sxs-lookup"><span data-stu-id="678c9-113">*xPos*</span></span> 
</dt> <dd>

<span data-ttu-id="678c9-114">Posizione X dello stilo.</span><span class="sxs-lookup"><span data-stu-id="678c9-114">The X position of the stylus.</span></span>

</dd> <dt>

<span data-ttu-id="678c9-115">*yPos*</span><span class="sxs-lookup"><span data-stu-id="678c9-115">*yPos*</span></span> 
</dt> <dd>

<span data-ttu-id="678c9-116">Posizione Y dello stilo.</span><span class="sxs-lookup"><span data-stu-id="678c9-116">The Y position of the stylus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="678c9-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="678c9-117">Return value</span></span>

<span data-ttu-id="678c9-118">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="678c9-118">This method can return one of these values.</span></span>



| <span data-ttu-id="678c9-119">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="678c9-119">Return code</span></span>                                                                            | <span data-ttu-id="678c9-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="678c9-120">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="678c9-121"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="678c9-121"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="678c9-122">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="678c9-122">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="678c9-123"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="678c9-123"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="678c9-124">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="678c9-124">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="678c9-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="678c9-125">Requirements</span></span>



| <span data-ttu-id="678c9-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="678c9-126">Requirement</span></span> | <span data-ttu-id="678c9-127">Valore</span><span class="sxs-lookup"><span data-stu-id="678c9-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="678c9-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="678c9-128">Minimum supported client</span></span><br/> | <span data-ttu-id="678c9-129">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="678c9-129">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="678c9-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="678c9-130">Minimum supported server</span></span><br/> | <span data-ttu-id="678c9-131">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="678c9-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="678c9-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="678c9-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="678c9-133"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="678c9-133"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="678c9-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="678c9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="678c9-135">**Interfaccia ITabletEventSink**</span><span class="sxs-lookup"><span data-stu-id="678c9-135">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




