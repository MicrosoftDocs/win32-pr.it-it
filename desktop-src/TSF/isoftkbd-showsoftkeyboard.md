---
title: Metodo ISoftKbd ShowSoftKeyboard (Softkbdc. h)
description: Il metodo ISoftKbd ShowSoftKeyboard Visualizza una tastiera soft.
ms.assetid: 7e24bef1-accb-40f6-a549-fb676abf9971
keywords:
- Framework servizi di testo Metodo ShowSoftKeyboard
- Framework dei servizi di testo del metodo ShowSoftKeyboard, interfaccia ISoftKbd
- ISoftKbd Interface Text Services Framework, metodo ShowSoftKeyboard
topic_type:
- apiref
api_name:
- ISoftKbd.ShowSoftKeyboard
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b319e7782a19571cf827175566e1af056c34cd4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047818"
---
# <a name="isoftkbdshowsoftkeyboard-method"></a><span data-ttu-id="3a7ad-106">Metodo ISoftKbd:: ShowSoftKeyboard</span><span class="sxs-lookup"><span data-stu-id="3a7ad-106">ISoftKbd::ShowSoftKeyboard method</span></span>

<span data-ttu-id="3a7ad-107">Il metodo **ISoftKbd:: ShowSoftKeyboard** Visualizza una tastiera soft.</span><span class="sxs-lookup"><span data-stu-id="3a7ad-107">The **ISoftKbd::ShowSoftKeyboard** method displays a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a7ad-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3a7ad-108">Syntax</span></span>


```C++
HRESULT ShowSoftKeyboard(
  [in] INT iShow
);
```



## <a name="parameters"></a><span data-ttu-id="3a7ad-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="3a7ad-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a7ad-110">*iShow* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3a7ad-110">*iShow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a7ad-111">Integer che indica il tipo di tastiera soft da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="3a7ad-111">Integer indicating the type of soft keyboard to display.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a7ad-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3a7ad-112">Return value</span></span>

<span data-ttu-id="3a7ad-113">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="3a7ad-113">This method can return one of these values.</span></span>



| <span data-ttu-id="3a7ad-114">Valore</span><span class="sxs-lookup"><span data-stu-id="3a7ad-114">Value</span></span>                                                                                | <span data-ttu-id="3a7ad-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3a7ad-115">Description</span></span>                           |
|--------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="3a7ad-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3a7ad-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="3a7ad-117">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="3a7ad-117">The method was successful.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3a7ad-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3a7ad-118">Requirements</span></span>



| <span data-ttu-id="3a7ad-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a7ad-119">Requirement</span></span> | <span data-ttu-id="3a7ad-120">Valore</span><span class="sxs-lookup"><span data-stu-id="3a7ad-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3a7ad-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3a7ad-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3a7ad-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3a7ad-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3a7ad-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3a7ad-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3a7ad-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3a7ad-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3a7ad-125">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="3a7ad-125">Redistributable</span></span><br/>          | <span data-ttu-id="3a7ad-126">TSF 1,0 su Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="3a7ad-126">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="3a7ad-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3a7ad-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a7ad-128"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a7ad-128"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="3a7ad-129">IDL</span><span class="sxs-lookup"><span data-stu-id="3a7ad-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3a7ad-130"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3a7ad-130"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="3a7ad-131">DLL</span><span class="sxs-lookup"><span data-stu-id="3a7ad-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a7ad-132"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a7ad-132"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a7ad-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3a7ad-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a7ad-134">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="3a7ad-134">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> </dl>

 

 





