---
description: Abilita nuovamente un oggetto dispositivo in modalità kernel di Microsoft DirectDraw dopo un'opzione di modalità.
ms.assetid: 26451881-cebf-4db1-aeed-365f0dae6704
title: Funzione NtGdiDdReenableDirectDrawObject (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdReenableDirectDrawObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: afd736317ecdf802cb418e81063b622db43f0651
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127283"
---
# <a name="ntgdiddreenabledirectdrawobject-function"></a><span data-ttu-id="0ef0b-103">NtGdiDdReenableDirectDrawObject (funzione)</span><span class="sxs-lookup"><span data-stu-id="0ef0b-103">NtGdiDdReenableDirectDrawObject function</span></span>

<span data-ttu-id="0ef0b-104">\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0ef0b-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="0ef0b-105">Usare invece il DirectDraw e Microsoft Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]</span><span class="sxs-lookup"><span data-stu-id="0ef0b-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="0ef0b-106">Abilita nuovamente un oggetto dispositivo in modalità kernel di Microsoft DirectDraw dopo un'opzione di modalità.</span><span class="sxs-lookup"><span data-stu-id="0ef0b-106">Re-enables a Microsoft DirectDraw kernel-mode device object after a mode switch.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ef0b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0ef0b-107">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiDdReenableDirectDrawObject(
  _In_    HANDLE hDirectDrawLocal,
  _Inout_ BOOL   *pubNewMode
);
```



## <a name="parameters"></a><span data-ttu-id="0ef0b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0ef0b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ef0b-109">*hDirectDrawLocal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0ef0b-109">*hDirectDrawLocal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ef0b-110">Oggetto DirectDraw che deve essere riabilitato.</span><span class="sxs-lookup"><span data-stu-id="0ef0b-110">DirectDraw object that needs to be re-enabled.</span></span>

</dd> <dt>

<span data-ttu-id="0ef0b-111">*pubNewMode* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="0ef0b-111">*pubNewMode* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ef0b-112">Puntatore a un BOOL che verrà riempito con un valore che indica se la modalità di visualizzazione è cambiata.</span><span class="sxs-lookup"><span data-stu-id="0ef0b-112">Pointer to a BOOL that will be filled with a value that represents whether the display mode changed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ef0b-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0ef0b-113">Return value</span></span>

<span data-ttu-id="0ef0b-114">Se ha esito positivo (il dispositivo può essere riabilitato), questa funzione restituisce **true**.</span><span class="sxs-lookup"><span data-stu-id="0ef0b-114">If successful (the device can be re-enabled), this function returns **TRUE**.</span></span> <span data-ttu-id="0ef0b-115">In caso contrario (ad esempio, il driver di visualizzazione è stato modificato), restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="0ef0b-115">Otherwise (for example, the display driver was changed), it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ef0b-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="0ef0b-116">Remarks</span></span>

<span data-ttu-id="0ef0b-117">Una volta che l'oggetto è stato riabilitato, è possibile eseguire una nuova query sulle funzionalità del dispositivo tramite una chiamata a [**NtGdiDdQueryDirectDrawObject**](-dxgkernel-ntgdiddquerydirectdrawobject.md).</span><span class="sxs-lookup"><span data-stu-id="0ef0b-117">Once the object has been re-enabled, the capabilities for the device can be re-queried via a call to [**NtGdiDdQueryDirectDrawObject**](-dxgkernel-ntgdiddquerydirectdrawobject.md).</span></span>

<span data-ttu-id="0ef0b-118">Per le applicazioni è consigliabile usare le API DirectDraw o [Direct3D](../direct3d10/d3d10-graphics-reference.md) versione 8, che automatizzano ed astraggono questo processo in modo indipendente dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0ef0b-118">Applications are advised to use the DirectDraw or [Direct3D](../direct3d10/d3d10-graphics-reference.md) version 8 APIs, which automate and abstract this process in a manner independent of the operating system.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ef0b-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0ef0b-119">Requirements</span></span>



| <span data-ttu-id="0ef0b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ef0b-120">Requirement</span></span> | <span data-ttu-id="0ef0b-121">Valore</span><span class="sxs-lookup"><span data-stu-id="0ef0b-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0ef0b-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0ef0b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0ef0b-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0ef0b-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="0ef0b-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0ef0b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0ef0b-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0ef0b-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0ef0b-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0ef0b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ef0b-127"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ef0b-127"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ef0b-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0ef0b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ef0b-129">Supporto client di livello inferiore grafica</span><span class="sxs-lookup"><span data-stu-id="0ef0b-129">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="0ef0b-130">**DdReenableDirectDrawObject**</span><span class="sxs-lookup"><span data-stu-id="0ef0b-130">**DdReenableDirectDrawObject**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddreenabledirectdrawobject)
</dt> </dl>

 

 
