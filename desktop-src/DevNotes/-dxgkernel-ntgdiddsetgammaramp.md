---
description: Imposta la rampa gamma per il dispositivo.
ms.assetid: 92ea0247-6eec-4c5f-9ea7-65f6b97dde1e
title: Funzione NtGdiDdSetGammaRamp (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdSetGammaRamp
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 0c5efba67eedbd6e70f1e0682f42c1855948cecd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125931"
---
# <a name="ntgdiddsetgammaramp-function"></a><span data-ttu-id="b6ead-103">NtGdiDdSetGammaRamp (funzione)</span><span class="sxs-lookup"><span data-stu-id="b6ead-103">NtGdiDdSetGammaRamp function</span></span>

<span data-ttu-id="b6ead-104">\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b6ead-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="b6ead-105">Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]</span><span class="sxs-lookup"><span data-stu-id="b6ead-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="b6ead-106">Imposta la rampa gamma per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b6ead-106">Sets the gamma ramp for the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6ead-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b6ead-107">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiDdSetGammaRamp(
  _In_ HANDLE hDirectDraw,
  _In_ HDC    hdc,
  _In_ LPVOID lpGammaRamp
);
```



## <a name="parameters"></a><span data-ttu-id="b6ead-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b6ead-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6ead-109">*hDirectDraw* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b6ead-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6ead-110">Handle per l'oggetto driver in modalità kernel per il quale è necessario impostare la rampa.</span><span class="sxs-lookup"><span data-stu-id="b6ead-110">Handle to the kernel-mode driver object for which the ramp is to be set.</span></span>

</dd> <dt>

<span data-ttu-id="b6ead-111">*HDC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b6ead-111">*hdc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6ead-112">Riservato.</span><span class="sxs-lookup"><span data-stu-id="b6ead-112">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="b6ead-113">*lpGammaRamp* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b6ead-113">*lpGammaRamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6ead-114">Puntatore a una matrice di strutture **DDGAMMARAMP** .</span><span class="sxs-lookup"><span data-stu-id="b6ead-114">Pointer to an array of **DDGAMMARAMP** structures.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6ead-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b6ead-115">Return value</span></span>

<span data-ttu-id="b6ead-116">Il valore restituito è **true** se la funzione ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="b6ead-116">The return value is **TRUE** if the function is successful.</span></span> <span data-ttu-id="b6ead-117">In caso contrario, è **null**.</span><span class="sxs-lookup"><span data-stu-id="b6ead-117">Otherwise, it is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6ead-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="b6ead-118">Remarks</span></span>

<span data-ttu-id="b6ead-119">È consigliabile che le applicazioni usino invece i metodi **IDirectDrawGammaControl:: SetGammaRamp** o [**IDirect3DDevice9:: SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp) , perché questi metodi offrono la stessa funzionalità indipendentemente dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b6ead-119">It is recommended that applications use the **IDirectDrawGammaControl::SetGammaRamp** or [**IDirect3DDevice9::SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp) methods instead because these methods offer the same functionality independent of the operating system.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6ead-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b6ead-120">Requirements</span></span>



| <span data-ttu-id="b6ead-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6ead-121">Requirement</span></span> | <span data-ttu-id="b6ead-122">Valore</span><span class="sxs-lookup"><span data-stu-id="b6ead-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b6ead-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b6ead-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b6ead-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b6ead-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="b6ead-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b6ead-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b6ead-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b6ead-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b6ead-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b6ead-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6ead-128"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6ead-128"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6ead-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b6ead-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6ead-130">Supporto client di livello inferiore grafica</span><span class="sxs-lookup"><span data-stu-id="b6ead-130">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
