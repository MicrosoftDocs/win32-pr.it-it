---
title: Metodo Initialize ISoftKbd (Softkbdc. h)
description: Il metodo di inizializzazione ISoftKbd Inizializza tutti i campi necessari per una tastiera morbida e genera layout di tastiera soft standard.
ms.assetid: c997864c-2596-4086-8062-cd30f371c38f
keywords:
- Framework dei servizi di testo del metodo Initialize
- Initialize Method Text Services Framework, interfaccia ISoftKbd
- ISoftKbd Interface Text Services Framework, metodo Initialize
topic_type:
- apiref
api_name:
- ISoftKbd.Initialize
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6e820becb05d7c474004b4889735f9637e0135a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740207"
---
# <a name="isoftkbdinitialize-method"></a><span data-ttu-id="ccf2d-106">Metodo ISoftKbd:: Initialize</span><span class="sxs-lookup"><span data-stu-id="ccf2d-106">ISoftKbd::Initialize method</span></span>

<span data-ttu-id="ccf2d-107">Il metodo **ISoftKbd:: Initialize** Inizializza tutti i campi necessari per una tastiera morbida e genera layout di tastiera soft standard.</span><span class="sxs-lookup"><span data-stu-id="ccf2d-107">The **ISoftKbd::Initialize** method initializes all necessary fields for a soft keyboard and generates standard soft keyboard layouts.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccf2d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ccf2d-108">Syntax</span></span>


```C++
HRESULT Initialize();
```



## <a name="parameters"></a><span data-ttu-id="ccf2d-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ccf2d-109">Parameters</span></span>

<span data-ttu-id="ccf2d-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="ccf2d-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ccf2d-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ccf2d-111">Return value</span></span>

<span data-ttu-id="ccf2d-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="ccf2d-112">This method can return one of these values.</span></span>



| <span data-ttu-id="ccf2d-113">Valore</span><span class="sxs-lookup"><span data-stu-id="ccf2d-113">Value</span></span>                                                                                | <span data-ttu-id="ccf2d-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ccf2d-114">Description</span></span>                           |
|--------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="ccf2d-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ccf2d-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="ccf2d-116">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="ccf2d-116">The method was successful.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ccf2d-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ccf2d-117">Requirements</span></span>



| <span data-ttu-id="ccf2d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ccf2d-118">Requirement</span></span> | <span data-ttu-id="ccf2d-119">Valore</span><span class="sxs-lookup"><span data-stu-id="ccf2d-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ccf2d-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ccf2d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ccf2d-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ccf2d-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ccf2d-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ccf2d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ccf2d-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ccf2d-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ccf2d-124">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="ccf2d-124">Redistributable</span></span><br/>          | <span data-ttu-id="ccf2d-125">TSF 1,0 su Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ccf2d-125">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="ccf2d-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ccf2d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ccf2d-127"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="ccf2d-127"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="ccf2d-128">IDL</span><span class="sxs-lookup"><span data-stu-id="ccf2d-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ccf2d-129"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ccf2d-129"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="ccf2d-130">DLL</span><span class="sxs-lookup"><span data-stu-id="ccf2d-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ccf2d-131"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ccf2d-131"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccf2d-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ccf2d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccf2d-133">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="ccf2d-133">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> </dl>

 

 





