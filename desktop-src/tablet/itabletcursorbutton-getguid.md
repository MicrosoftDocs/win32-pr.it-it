---
description: Recupera l'identificatore univoco del pulsante dello stilo.
ms.assetid: 06bd6a84-46cd-4c62-92d6-50caae359e43
title: 'Metodo ITabletCursorButton:: GetGuid'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursorButton.GetGuid
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 21d63ef0c934e96bc93b5384cab1e67f9dd452d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057989"
---
# <a name="itabletcursorbuttongetguid-method"></a><span data-ttu-id="0e400-103">Metodo ITabletCursorButton:: GetGuid</span><span class="sxs-lookup"><span data-stu-id="0e400-103">ITabletCursorButton::GetGuid method</span></span>

<span data-ttu-id="0e400-104">Recupera l'identificatore univoco del pulsante dello stilo.</span><span class="sxs-lookup"><span data-stu-id="0e400-104">Retrieves the unique identifier of the stylus button.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e400-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0e400-105">Syntax</span></span>


```C++
HRESULT GetGuid(
  [out] GUID *pguidBtn
);
```



## <a name="parameters"></a><span data-ttu-id="0e400-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0e400-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e400-107">*pguidBtn* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0e400-107">*pguidBtn* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0e400-108">Valore univoco che identifica il pulsante dello stilo.</span><span class="sxs-lookup"><span data-stu-id="0e400-108">A unique value that identifies the stylus button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e400-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0e400-109">Return value</span></span>

<span data-ttu-id="0e400-110">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="0e400-110">This method can return one of these values.</span></span>



| <span data-ttu-id="0e400-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="0e400-111">Return code</span></span>                                                                            | <span data-ttu-id="0e400-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0e400-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="0e400-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0e400-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="0e400-114">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="0e400-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="0e400-115"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="0e400-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="0e400-116">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="0e400-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0e400-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0e400-117">Requirements</span></span>



| <span data-ttu-id="0e400-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e400-118">Requirement</span></span> | <span data-ttu-id="0e400-119">Valore</span><span class="sxs-lookup"><span data-stu-id="0e400-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e400-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e400-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0e400-121">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="0e400-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0e400-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e400-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0e400-123">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="0e400-123">None supported</span></span><br/>                                                              |
| <span data-ttu-id="0e400-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="0e400-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="0e400-125"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0e400-125"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e400-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0e400-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e400-127">**Interfaccia ITabletCursorButton**</span><span class="sxs-lookup"><span data-stu-id="0e400-127">**ITabletCursorButton Interface**</span></span>](itabletcursorbutton.md)
</dt> </dl>

 

 




