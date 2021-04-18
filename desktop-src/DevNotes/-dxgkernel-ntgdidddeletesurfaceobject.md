---
description: NtGdiDdDeleteSurfaceObject Elimina un oggetto Surface in modalità kernel creato in precedenza.
ms.assetid: 95ce6c73-7e41-4ac3-b849-9b8f53aa3ac3
title: Funzione NtGdiDdDeleteSurfaceObject (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdDeleteSurfaceObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 03988b842aacc29915287490508eb9e9d057e907
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304461"
---
# <a name="ntgdidddeletesurfaceobject-function"></a><span data-ttu-id="9a49e-103">NtGdiDdDeleteSurfaceObject (funzione)</span><span class="sxs-lookup"><span data-stu-id="9a49e-103">NtGdiDdDeleteSurfaceObject function</span></span>

<span data-ttu-id="9a49e-104">\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="9a49e-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="9a49e-105">Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]</span><span class="sxs-lookup"><span data-stu-id="9a49e-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="9a49e-106">**NtGdiDdDeleteSurfaceObject** Elimina un oggetto Surface in modalità kernel creato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="9a49e-106">**NtGdiDdDeleteSurfaceObject** deletes a previously created kernel-mode surface object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a49e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9a49e-107">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiDdDeleteSurfaceObject(
  _In_ HANDLE hSurface
);
```



## <a name="parameters"></a><span data-ttu-id="9a49e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9a49e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a49e-109">*hSurface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9a49e-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a49e-110">Handle per l'oggetto Surface in modalità kernel creato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="9a49e-110">Handle to the previously created kernel-mode surface object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a49e-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9a49e-111">Return value</span></span>

<span data-ttu-id="9a49e-112">Se l'esito è positivo, la funzione restituisce **true**. in caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="9a49e-112">If successful, this function returns **TRUE**; otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a49e-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="9a49e-113">Remarks</span></span>

<span data-ttu-id="9a49e-114">Per creare e gestire oggetti dispositivo di grafica, è consigliabile usare le API DirectDraw e [Direct3D](../direct3d10/d3d10-graphics-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="9a49e-114">Applications are advised to use the DirectDraw and [Direct3D](../direct3d10/d3d10-graphics-reference.md) APIs to create and manage graphics device objects.</span></span> <span data-ttu-id="9a49e-115">Questi costrutti astraggono il processo di creazione del dispositivo in modo semplificato e indipendente dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="9a49e-115">These constructs abstract the device creation process in a simplified and operating-system-independent way.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a49e-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9a49e-116">Requirements</span></span>



| <span data-ttu-id="9a49e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a49e-117">Requirement</span></span> | <span data-ttu-id="9a49e-118">Valore</span><span class="sxs-lookup"><span data-stu-id="9a49e-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9a49e-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9a49e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9a49e-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9a49e-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="9a49e-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9a49e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9a49e-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9a49e-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9a49e-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9a49e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a49e-124"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a49e-124"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a49e-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9a49e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a49e-126">Supporto client di livello inferiore grafica</span><span class="sxs-lookup"><span data-stu-id="9a49e-126">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="9a49e-127">**DdDeleteSurfaceObject**</span><span class="sxs-lookup"><span data-stu-id="9a49e-127">**DdDeleteSurfaceObject**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-dddeletesurfaceobject)
</dt> <dt>

[<span data-ttu-id="9a49e-128">**NtGdiDdCreateSurfaceObject**</span><span class="sxs-lookup"><span data-stu-id="9a49e-128">**NtGdiDdCreateSurfaceObject**</span></span>](-dxgkernel-ntgdiddcreatesurfaceobject.md)
</dt> </dl>

 

 
