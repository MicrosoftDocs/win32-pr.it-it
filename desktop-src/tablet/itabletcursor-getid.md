---
description: Recupera l'identificatore dello stilo.
ms.assetid: 27320a2f-1e4a-4d7d-a1f8-5244f4a03415
title: 'Metodo ITabletCursor:: GetId'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.GetId
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 5d4f71d2cd465bfd2d1ff4c245154a300c431df2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104401758"
---
# <a name="itabletcursorgetid-method"></a><span data-ttu-id="af9e8-103">Metodo ITabletCursor:: GetId</span><span class="sxs-lookup"><span data-stu-id="af9e8-103">ITabletCursor::GetId method</span></span>

<span data-ttu-id="af9e8-104">Recupera l'identificatore dello stilo.</span><span class="sxs-lookup"><span data-stu-id="af9e8-104">Retrieves the stylus identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="af9e8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="af9e8-105">Syntax</span></span>


```C++
HRESULT GetId(
  [out] CURSOR_ID *pCid
);
```



## <a name="parameters"></a><span data-ttu-id="af9e8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="af9e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af9e8-107">*pCid* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="af9e8-107">*pCid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="af9e8-108">Identificatore dello stilo del tablet.</span><span class="sxs-lookup"><span data-stu-id="af9e8-108">The identifier of the tablet stylus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af9e8-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="af9e8-109">Return value</span></span>

<span data-ttu-id="af9e8-110">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="af9e8-110">This method can return one of these values.</span></span>



| <span data-ttu-id="af9e8-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="af9e8-111">Return code</span></span>                                                                            | <span data-ttu-id="af9e8-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="af9e8-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="af9e8-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="af9e8-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="af9e8-114">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="af9e8-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="af9e8-115"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="af9e8-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="af9e8-116">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="af9e8-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="af9e8-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="af9e8-117">Remarks</span></span>

<span data-ttu-id="af9e8-118">\_L'ID del cursore viene definito come un valore DWORD.</span><span class="sxs-lookup"><span data-stu-id="af9e8-118">CURSOR\_ID is defined as a DWORD.</span></span>

## <a name="requirements"></a><span data-ttu-id="af9e8-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="af9e8-119">Requirements</span></span>



| <span data-ttu-id="af9e8-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="af9e8-120">Requirement</span></span> | <span data-ttu-id="af9e8-121">Valore</span><span class="sxs-lookup"><span data-stu-id="af9e8-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="af9e8-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af9e8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="af9e8-123">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="af9e8-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="af9e8-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af9e8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="af9e8-125">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="af9e8-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="af9e8-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="af9e8-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="af9e8-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="af9e8-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af9e8-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="af9e8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af9e8-129">**Interfaccia ITabletCursor**</span><span class="sxs-lookup"><span data-stu-id="af9e8-129">**ITabletCursor Interface**</span></span>](itabletcursor.md)
</dt> </dl>

 

 




