---
description: Elimina un oggetto dispositivo Microsoft DirectDraw in modalità kernel creato in precedenza.
ms.assetid: 0b2e1bae-8291-4fe4-9528-980680906e0a
title: Funzione NtGdiDdDeleteDirectDrawObject (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdDeleteDirectDrawObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 9ac10798f83fe7e1a07a0803dd29cfa9cd8b1c98
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125937"
---
# <a name="ntgdidddeletedirectdrawobject-function"></a><span data-ttu-id="7c1f3-103">NtGdiDdDeleteDirectDrawObject (funzione)</span><span class="sxs-lookup"><span data-stu-id="7c1f3-103">NtGdiDdDeleteDirectDrawObject function</span></span>

<span data-ttu-id="7c1f3-104">\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="7c1f3-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="7c1f3-105">Usare invece il DirectDraw e Microsoft Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]</span><span class="sxs-lookup"><span data-stu-id="7c1f3-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="7c1f3-106">Elimina un oggetto dispositivo Microsoft DirectDraw in modalità kernel creato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="7c1f3-106">Destroys a previously created kernel-mode Microsoft DirectDraw device object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c1f3-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7c1f3-107">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiDdDeleteDirectDrawObject(
   HANDLE hDirectDrawLocal
);
```



## <a name="parameters"></a><span data-ttu-id="7c1f3-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7c1f3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c1f3-109">*hDirectDrawLocal*</span><span class="sxs-lookup"><span data-stu-id="7c1f3-109">*hDirectDrawLocal*</span></span> 
</dt> <dd>

<span data-ttu-id="7c1f3-110">Handle per l'oggetto dispositivo DirectDraw in modalità kernel.</span><span class="sxs-lookup"><span data-stu-id="7c1f3-110">Handle to the kernel-mode DirectDraw device object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c1f3-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7c1f3-111">Return value</span></span>

<span data-ttu-id="7c1f3-112">Se l'esito è positivo, la funzione restituisce **true**. in caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="7c1f3-112">If successful, this function returns **TRUE**; otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c1f3-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="7c1f3-113">Remarks</span></span>

<span data-ttu-id="7c1f3-114">Per creare e gestire oggetti dispositivo di grafica, è consigliabile usare le API DirectDraw e [Direct3D](../direct3d10/d3d10-graphics-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="7c1f3-114">Applications are advised to use the DirectDraw and [Direct3D](../direct3d10/d3d10-graphics-reference.md) APIs to create and manage graphics device objects.</span></span> <span data-ttu-id="7c1f3-115">Questi costrutti astraggono il processo di creazione del dispositivo in modo semplificato e indipendente dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="7c1f3-115">These constructs abstract the device creation process in a simplified and operating-system-independent way.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c1f3-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7c1f3-116">Requirements</span></span>



| <span data-ttu-id="7c1f3-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c1f3-117">Requirement</span></span> | <span data-ttu-id="7c1f3-118">Valore</span><span class="sxs-lookup"><span data-stu-id="7c1f3-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7c1f3-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c1f3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7c1f3-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7c1f3-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="7c1f3-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c1f3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7c1f3-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7c1f3-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7c1f3-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7c1f3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c1f3-124"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c1f3-124"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c1f3-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7c1f3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c1f3-126">Supporto client di livello inferiore grafica</span><span class="sxs-lookup"><span data-stu-id="7c1f3-126">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="7c1f3-127">**NtGdiDdCreateDirectDrawObject**</span><span class="sxs-lookup"><span data-stu-id="7c1f3-127">**NtGdiDdCreateDirectDrawObject**</span></span>](-dxgkernel-ntgdiddcreatedirectdrawobject.md)
</dt> <dt>

[<span data-ttu-id="7c1f3-128">**DdDeleteDirectDrawObject**</span><span class="sxs-lookup"><span data-stu-id="7c1f3-128">**DdDeleteDirectDrawObject**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-dddeletedirectdrawobject)
</dt> </dl>

 

 
