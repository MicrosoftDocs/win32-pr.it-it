---
description: Crea una rappresentazione sul lato kernel dell'oggetto Microsoft DirectDraw.
ms.assetid: e380f948-35a0-4cf0-9b69-ab2bd4f9a161
title: Funzione NtGdiDdCreateDirectDrawObject (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateDirectDrawObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 16dd140c7b205c92b34cb9bd397a4b8d2d3e1a60
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125943"
---
# <a name="ntgdiddcreatedirectdrawobject-function"></a><span data-ttu-id="68462-103">NtGdiDdCreateDirectDrawObject (funzione)</span><span class="sxs-lookup"><span data-stu-id="68462-103">NtGdiDdCreateDirectDrawObject function</span></span>

<span data-ttu-id="68462-104">\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="68462-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="68462-105">Usare invece il DirectDraw e Microsoft Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]</span><span class="sxs-lookup"><span data-stu-id="68462-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="68462-106">Crea una rappresentazione sul lato kernel dell'oggetto Microsoft DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="68462-106">Creates a kernel-side representation of the Microsoft DirectDraw object.</span></span>

## <a name="syntax"></a><span data-ttu-id="68462-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="68462-107">Syntax</span></span>


```C++
HANDLE APIENTRY NtGdiDdCreateDirectDrawObject(
  _In_ HDC hdc
);
```



## <a name="parameters"></a><span data-ttu-id="68462-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="68462-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68462-109">*HDC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="68462-109">*hdc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68462-110">Qualsiasi dispositivo di visualizzazione del controller di dominio per il quale deve essere creato l'oggetto DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="68462-110">Any DC display device for which the DirectDraw object should be created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68462-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="68462-111">Return value</span></span>

<span data-ttu-id="68462-112">Se ha esito positivo, questa funzione restituisce un handle per la rappresentazione dell'oggetto in modalità kernel. in caso contrario, restituisce **null**.</span><span class="sxs-lookup"><span data-stu-id="68462-112">If successful, this function returns a handle to the kernel-mode object representation; otherwise it returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="68462-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="68462-113">Remarks</span></span>

<span data-ttu-id="68462-114">Per creare e gestire oggetti dispositivo di grafica, è consigliabile usare le API DirectDraw e [Direct3D](../direct3d10/d3d10-graphics-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="68462-114">Applications are advised to use the DirectDraw and [Direct3D](../direct3d10/d3d10-graphics-reference.md) APIs to create and manage graphics device objects.</span></span> <span data-ttu-id="68462-115">Questi costrutti astraggono il processo di creazione del dispositivo in modo semplificato e indipendente dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="68462-115">These constructs abstract the device creation process in a simplified and operating-system-independent way.</span></span>

## <a name="requirements"></a><span data-ttu-id="68462-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="68462-116">Requirements</span></span>



| <span data-ttu-id="68462-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="68462-117">Requirement</span></span> | <span data-ttu-id="68462-118">Valore</span><span class="sxs-lookup"><span data-stu-id="68462-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="68462-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="68462-119">Minimum supported client</span></span><br/> | <span data-ttu-id="68462-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="68462-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="68462-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="68462-121">Minimum supported server</span></span><br/> | <span data-ttu-id="68462-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="68462-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="68462-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="68462-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="68462-124"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="68462-124"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68462-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="68462-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68462-126">Supporto client di livello inferiore grafica</span><span class="sxs-lookup"><span data-stu-id="68462-126">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="68462-127">**DdCreateDirectDrawObject**</span><span class="sxs-lookup"><span data-stu-id="68462-127">**DdCreateDirectDrawObject**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddcreatedirectdrawobject)
</dt> </dl>

 

 
