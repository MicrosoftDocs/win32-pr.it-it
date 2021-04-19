---
description: Sposta un contesto del tablet nella parte anteriore o posteriore della coda di input.
ms.assetid: ef4521b5-776b-46dc-864a-625bc221054a
title: 'Metodo ITabletContextP:: sovrapposizione'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP.Overlap
api_type:
- COM
api_location:
- Wisptis.exe
- Wisptis.exe.dll
ms.openlocfilehash: b009bc08dddb15bc7aa5b12c8846ea66c4a52e56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316824"
---
# <a name="itabletcontextpoverlap-method"></a><span data-ttu-id="dc328-103">Metodo ITabletContextP:: sovrapposizione</span><span class="sxs-lookup"><span data-stu-id="dc328-103">ITabletContextP::Overlap method</span></span>

<span data-ttu-id="dc328-104">Sposta un contesto del tablet nella parte anteriore o posteriore della coda di input.</span><span class="sxs-lookup"><span data-stu-id="dc328-104">Moves a tablet context to the front or back of the input queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc328-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dc328-105">Syntax</span></span>


```C++
HRESULT Overlap(
  [in]  BOOL  bTop,
  [out] DWORD *pdwtcid
);
```



## <a name="parameters"></a><span data-ttu-id="dc328-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="dc328-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc328-107">*bTop* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dc328-107">*bTop* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc328-108">Indica se il contesto del tablet deve essere spostato nella parte superiore o inferiore della coda di input.</span><span class="sxs-lookup"><span data-stu-id="dc328-108">Indicates if the tablet context should be moved to the top or bottom of the input queue.</span></span>

</dd> <dt>

<span data-ttu-id="dc328-109">*pdwtcid* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="dc328-109">*pdwtcid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dc328-110">Identificatore di contesto della tavoletta.</span><span class="sxs-lookup"><span data-stu-id="dc328-110">The tablet context identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc328-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dc328-111">Return value</span></span>

<span data-ttu-id="dc328-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="dc328-112">This method can return one of these values.</span></span>



| <span data-ttu-id="dc328-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="dc328-113">Return code</span></span>                                                                            | <span data-ttu-id="dc328-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dc328-114">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="dc328-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="dc328-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="dc328-116">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="dc328-116">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="dc328-117"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="dc328-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="dc328-118">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="dc328-118">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="dc328-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dc328-119">Requirements</span></span>



| <span data-ttu-id="dc328-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc328-120">Requirement</span></span> | <span data-ttu-id="dc328-121">Valore</span><span class="sxs-lookup"><span data-stu-id="dc328-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc328-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dc328-122">Minimum supported client</span></span><br/> | <span data-ttu-id="dc328-123">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="dc328-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="dc328-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dc328-124">Minimum supported server</span></span><br/> | <span data-ttu-id="dc328-125">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="dc328-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="dc328-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="dc328-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="dc328-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dc328-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc328-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dc328-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc328-129">**Interfaccia ITabletContextP**</span><span class="sxs-lookup"><span data-stu-id="dc328-129">**ITabletContextP Interface**</span></span>](itabletcontextp.md)
</dt> </dl>

 

 




