---
title: MsimtfIsWindowFiltered (funzione)
description: La funzione MsimtfIsWindowFiltered verifica se la finestra specificata è filtrata in base a AIMM (gestore del metodo di input attivo).
ms.assetid: 1f5e98f1-3626-4aa5-b2da-b6bc48d02184
keywords:
- Framework servizi di testo funzione MsimtfIsWindowFiltered
topic_type:
- apiref
api_name:
- MsimtfIsWindowFiltered
api_location:
- msimtf.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70ad9bd9fb61c546ec3e2f1d96d5fc9cf932613a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120915"
---
# <a name="msimtfiswindowfiltered-function"></a><span data-ttu-id="f7995-104">MsimtfIsWindowFiltered (funzione)</span><span class="sxs-lookup"><span data-stu-id="f7995-104">MsimtfIsWindowFiltered function</span></span>

<span data-ttu-id="f7995-105">La funzione **MsimtfIsWindowFiltered** verifica se la finestra specificata è filtrata in base a AIMM (gestore del metodo di input attivo).</span><span class="sxs-lookup"><span data-stu-id="f7995-105">The **MsimtfIsWindowFiltered** function tests if the given window is filtered by AIMM (Active Input Method Manager).</span></span>

## <a name="syntax"></a><span data-ttu-id="f7995-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f7995-106">Syntax</span></span>


```C++
BOOL CALLBACK MsimtfIsWindowFiltered(
  _In_ HWND hwnd
);
```



## <a name="parameters"></a><span data-ttu-id="f7995-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="f7995-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7995-108">*HWND* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f7995-108">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7995-109">Handle di finestra da verificare.</span><span class="sxs-lookup"><span data-stu-id="f7995-109">A window handle to be tested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7995-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f7995-110">Return value</span></span>



| <span data-ttu-id="f7995-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="f7995-111">Return code</span></span>                                                                          | <span data-ttu-id="f7995-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f7995-112">Description</span></span>                                                               |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f7995-113"><dt>**TRUE**</dt></span><span class="sxs-lookup"><span data-stu-id="f7995-113"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="f7995-114">Se questa finestra è filtrata in base al gestore del metodo di input attivo.</span><span class="sxs-lookup"><span data-stu-id="f7995-114">If this window is filtered by Active Input Method Manager.</span></span><br/>     |
| <dl> <span data-ttu-id="f7995-115"><dt>**FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="f7995-115"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="f7995-116">Se questa finestra non viene filtrata in base al gestore del metodo di input attivo.</span><span class="sxs-lookup"><span data-stu-id="f7995-116">If this window is not filtered by Active Input Method Manager.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f7995-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="f7995-117">Remarks</span></span>

<span data-ttu-id="f7995-118">Una finestra può essere filtrata in base a IActiveIMMApp:: FilterClientWindows.</span><span class="sxs-lookup"><span data-stu-id="f7995-118">A window can be filtered by IActiveIMMApp::FilterClientWindows.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7995-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f7995-119">Requirements</span></span>



| <span data-ttu-id="f7995-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7995-120">Requirement</span></span> | <span data-ttu-id="f7995-121">Valore</span><span class="sxs-lookup"><span data-stu-id="f7995-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f7995-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f7995-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f7995-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f7995-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f7995-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f7995-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f7995-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f7995-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f7995-126">DLL</span><span class="sxs-lookup"><span data-stu-id="f7995-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7995-127"><dt>Msimtf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7995-127"><dt>Msimtf.dll</dt></span></span> </dl> |



 

 





