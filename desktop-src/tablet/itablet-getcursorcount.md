---
description: Restituisce il numero di oggetti cursori associati al tablet.
ms.assetid: 7aa5802c-1255-41a4-b1fa-23e5f56c0b80
title: 'Metodo ITablet:: GetCursorCount'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetCursorCount
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 2309384e4aa36383277ba72cc407cabef7ab4b27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316828"
---
# <a name="itabletgetcursorcount-method"></a><span data-ttu-id="fe710-103">Metodo ITablet:: GetCursorCount</span><span class="sxs-lookup"><span data-stu-id="fe710-103">ITablet::GetCursorCount method</span></span>

<span data-ttu-id="fe710-104">Restituisce il numero di oggetti cursori associati al tablet.</span><span class="sxs-lookup"><span data-stu-id="fe710-104">Returns the number of cursor objects associated with the tablet.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe710-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fe710-105">Syntax</span></span>


```C++
HRESULT GetCursorCount(
  [out] ULONG *pcCurs
);
```



## <a name="parameters"></a><span data-ttu-id="fe710-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fe710-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe710-107">*pcCurs* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fe710-107">*pcCurs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe710-108">Numero di oggetti cursori associati al tablet.</span><span class="sxs-lookup"><span data-stu-id="fe710-108">The number of cursor objects associated with the tablet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe710-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fe710-109">Return value</span></span>

<span data-ttu-id="fe710-110">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="fe710-110">This method can return one of these values.</span></span>



| <span data-ttu-id="fe710-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="fe710-111">Return code</span></span>                                                                            | <span data-ttu-id="fe710-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fe710-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="fe710-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fe710-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="fe710-114">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="fe710-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="fe710-115"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="fe710-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="fe710-116">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="fe710-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="fe710-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fe710-117">Requirements</span></span>



| <span data-ttu-id="fe710-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe710-118">Requirement</span></span> | <span data-ttu-id="fe710-119">Valore</span><span class="sxs-lookup"><span data-stu-id="fe710-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe710-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fe710-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fe710-121">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="fe710-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="fe710-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fe710-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fe710-123">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="fe710-123">None supported</span></span><br/>                                                              |
| <span data-ttu-id="fe710-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="fe710-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="fe710-125"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fe710-125"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe710-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fe710-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe710-127">**Interfaccia ITablet**</span><span class="sxs-lookup"><span data-stu-id="fe710-127">**ITablet Interface**</span></span>](itablet.md)
</dt> </dl>

 

 




