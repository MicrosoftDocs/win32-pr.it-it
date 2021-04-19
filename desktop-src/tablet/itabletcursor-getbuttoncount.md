---
description: Recupera il numero di pulsanti sullo stilo del tablet.
ms.assetid: ae4ce670-769a-4f00-b728-285020f09934
title: 'Metodo ITabletCursor:: GetButtonCount'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.GetButtonCount
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 08fdf24b2a0b69b7830a683786f18fc5df0805b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317923"
---
# <a name="itabletcursorgetbuttoncount-method"></a><span data-ttu-id="90ae6-103">Metodo ITabletCursor:: GetButtonCount</span><span class="sxs-lookup"><span data-stu-id="90ae6-103">ITabletCursor::GetButtonCount method</span></span>

<span data-ttu-id="90ae6-104">Recupera il numero di pulsanti sullo stilo del tablet.</span><span class="sxs-lookup"><span data-stu-id="90ae6-104">Retrieves the number of buttons on the tablet stylus.</span></span>

## <a name="syntax"></a><span data-ttu-id="90ae6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="90ae6-105">Syntax</span></span>


```C++
HRESULT GetButtonCount(
  [out] ULONG *pcButtons
);
```



## <a name="parameters"></a><span data-ttu-id="90ae6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="90ae6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90ae6-107">*pcButtons* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="90ae6-107">*pcButtons* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="90ae6-108">Conteggio dei pulsanti sullo stilo del tablet.</span><span class="sxs-lookup"><span data-stu-id="90ae6-108">The count of buttons on the tablet stylus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90ae6-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="90ae6-109">Return value</span></span>

<span data-ttu-id="90ae6-110">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="90ae6-110">This method can return one of these values.</span></span>



| <span data-ttu-id="90ae6-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="90ae6-111">Return code</span></span>                                                                            | <span data-ttu-id="90ae6-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="90ae6-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="90ae6-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="90ae6-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="90ae6-114">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="90ae6-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="90ae6-115"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="90ae6-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="90ae6-116">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="90ae6-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="90ae6-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="90ae6-117">Requirements</span></span>



| <span data-ttu-id="90ae6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="90ae6-118">Requirement</span></span> | <span data-ttu-id="90ae6-119">Valore</span><span class="sxs-lookup"><span data-stu-id="90ae6-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="90ae6-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="90ae6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="90ae6-121">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="90ae6-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="90ae6-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="90ae6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="90ae6-123">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="90ae6-123">None supported</span></span><br/>                                                              |
| <span data-ttu-id="90ae6-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="90ae6-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="90ae6-125"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="90ae6-125"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90ae6-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="90ae6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90ae6-127">**Interfaccia ITabletCursor**</span><span class="sxs-lookup"><span data-stu-id="90ae6-127">**ITabletCursor Interface**</span></span>](itabletcursor.md)
</dt> </dl>

 

 




