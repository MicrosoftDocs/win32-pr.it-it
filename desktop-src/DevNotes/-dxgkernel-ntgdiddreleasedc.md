---
description: Rilascia il contesto di dispositivo creato in precedenza per l'oggetto Surface Microsoft DirectDraw in modalità kernel indicato.
ms.assetid: 98def2a1-878d-4776-a519-32cb70107338
title: Funzione NtGdiDdReleaseDC (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdReleaseDC
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: a7319b423f12d7e4415d78d995bfb1d7cd0341a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877261"
---
# <a name="ntgdiddreleasedc-function"></a><span data-ttu-id="142c6-103">NtGdiDdReleaseDC (funzione)</span><span class="sxs-lookup"><span data-stu-id="142c6-103">NtGdiDdReleaseDC function</span></span>

<span data-ttu-id="142c6-104">\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="142c6-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="142c6-105">Usare invece il DirectDraw e Microsoft Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]</span><span class="sxs-lookup"><span data-stu-id="142c6-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="142c6-106">Rilascia il contesto di dispositivo creato in precedenza per l'oggetto Surface Microsoft DirectDraw in modalità kernel indicato.</span><span class="sxs-lookup"><span data-stu-id="142c6-106">Releases the previously created device context (DC) for the indicated kernel-mode Microsoft DirectDraw surface object.</span></span>

## <a name="syntax"></a><span data-ttu-id="142c6-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="142c6-107">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiDdReleaseDC(
  _In_ HANDLE hSurface
);
```



## <a name="parameters"></a><span data-ttu-id="142c6-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="142c6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="142c6-109">*hSurface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="142c6-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="142c6-110">Handle per l'oggetto Surface DirectDraw in modalità kernel creato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="142c6-110">Handle to the previously created kernel-mode DirectDraw surface object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="142c6-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="142c6-111">Return value</span></span>

<span data-ttu-id="142c6-112">Se l'esito è positivo, la funzione restituisce **true**. in caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="142c6-112">If successful, this function returns **TRUE**; otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="142c6-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="142c6-113">Remarks</span></span>

<span data-ttu-id="142c6-114">Le applicazioni che devono ottenere un controller di dominio per una superficie DirectDraw possono utilizzare [IDirectDrawSurface7:: GetDC](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-getdc), che espone questa funzionalità in modo indipendente dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="142c6-114">Applications that need to obtain a DC for a DirectDraw surface may use [IDirectDrawSurface7::GetDC](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-getdc), which exposes this functionality in a manner independent of the operating system.</span></span>

## <a name="requirements"></a><span data-ttu-id="142c6-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="142c6-115">Requirements</span></span>



| <span data-ttu-id="142c6-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="142c6-116">Requirement</span></span> | <span data-ttu-id="142c6-117">Valore</span><span class="sxs-lookup"><span data-stu-id="142c6-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="142c6-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="142c6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="142c6-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="142c6-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="142c6-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="142c6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="142c6-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="142c6-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="142c6-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="142c6-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="142c6-123"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="142c6-123"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="142c6-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="142c6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="142c6-125">Supporto client di livello inferiore grafica</span><span class="sxs-lookup"><span data-stu-id="142c6-125">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="142c6-126">**DdReleaseDC**</span><span class="sxs-lookup"><span data-stu-id="142c6-126">**DdReleaseDC**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddreleasedc)
</dt> </dl>

 

 
