---
description: Consente di abilitare la modalità utente per ottenere una conoscenza valida dell'area di visualizzazione per Windows sul desktop. Questo ritaglio può variare in modo asincrono dal punto di vista dei thread in modalità utente.
ms.assetid: 286f1c06-c27b-42bd-aecc-3a6923e3df29
title: Funzione NtGdiDdResetVisrgn (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdResetVisrgn
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: dd83bcfd6c1f3dec31fb80cf78750bfdfef5e7a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877257"
---
# <a name="ntgdiddresetvisrgn-function"></a><span data-ttu-id="47eb3-104">NtGdiDdResetVisrgn (funzione)</span><span class="sxs-lookup"><span data-stu-id="47eb3-104">NtGdiDdResetVisrgn function</span></span>

<span data-ttu-id="47eb3-105">\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="47eb3-105">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="47eb3-106">Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]</span><span class="sxs-lookup"><span data-stu-id="47eb3-106">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="47eb3-107">Consente di abilitare la modalità utente per ottenere una conoscenza valida dell'area di visualizzazione per Windows sul desktop.</span><span class="sxs-lookup"><span data-stu-id="47eb3-107">Used to enable the user mode to gain a valid understanding of the clipping region for windows on the desktop.</span></span> <span data-ttu-id="47eb3-108">Questo ritaglio può variare in modo asincrono dal punto di vista dei thread in modalità utente.</span><span class="sxs-lookup"><span data-stu-id="47eb3-108">This clipping can change asynchronously from the point of view of user-mode threads.</span></span>

## <a name="syntax"></a><span data-ttu-id="47eb3-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="47eb3-109">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiDdResetVisrgn(
  _In_ HANDLE hSurface,
  _In_ HWND   hwnd
);
```



## <a name="parameters"></a><span data-ttu-id="47eb3-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="47eb3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47eb3-111">*hSurface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="47eb3-111">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47eb3-112">Puntatore all'oggetto in modalità utente di qualsiasi superficie appartenente al dispositivo DirectDraw per il quale deve essere reimpostato il ritaglio.</span><span class="sxs-lookup"><span data-stu-id="47eb3-112">Pointer to the user-mode object of any surface belonging to the DirectDraw device for which clipping is to be reset.</span></span> <span data-ttu-id="47eb3-113">Per informazioni dettagliate, vedere la documentazione di DDK.</span><span class="sxs-lookup"><span data-stu-id="47eb3-113">For details, see the DDK documentation.</span></span>

</dd> <dt>

<span data-ttu-id="47eb3-114">*HWND* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="47eb3-114">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47eb3-115">Riservato.</span><span class="sxs-lookup"><span data-stu-id="47eb3-115">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47eb3-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="47eb3-116">Return value</span></span>

<span data-ttu-id="47eb3-117">Se l'esito è positivo, la funzione restituisce **true**. in caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="47eb3-117">If successful, this function returns **TRUE**; otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="47eb3-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="47eb3-118">Remarks</span></span>

<span data-ttu-id="47eb3-119">Il ritaglio può variare in modo asincrono dal punto di vista dei thread in modalità utente.</span><span class="sxs-lookup"><span data-stu-id="47eb3-119">Clipping can change asynchronously from the point of view of user-mode threads.</span></span> <span data-ttu-id="47eb3-120">Le parti in modalità kernel di DirectDraw e Windows Graphics Device Interface (GDI) mantengono un contatore incrementato ogni volta che viene modificato l'elenco di ritaglio per l'intero desktop.</span><span class="sxs-lookup"><span data-stu-id="47eb3-120">The kernel-mode parts of DirectDraw and Windows Graphics Device Interface (GDI) maintain a counter that is incremented whenever the clipping list for the entire desktop changes.</span></span> <span data-ttu-id="47eb3-121">Una chiamata a questa funzione registra questo contatore con ogni superficie primaria DirectDraw esistente nel sistema.</span><span class="sxs-lookup"><span data-stu-id="47eb3-121">A call to this function records this counter with every existing DirectDraw primary surface on the system.</span></span>

<span data-ttu-id="47eb3-122">In un secondo momento, quando una di queste superfici primarie viene modificata da un'operazione [IDirectDrawSurface7:: BLT](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-blt) o [IDirectDrawSurface7:: Lock](/previous-versions/ms858221(v=msdn.10)) (vedere la documentazione di DDK), il contatore registrato con la superficie viene confrontato con il contatore globale.</span><span class="sxs-lookup"><span data-stu-id="47eb3-122">At any later time when one of these primary surfaces is modified by a [IDirectDrawSurface7::Blt](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-blt) or [IDirectDrawSurface7::Lock](/previous-versions/ms858221(v=msdn.10)) operation (see DDK documentation), then the counter recorded with the surface is compared with the global counter.</span></span> <span data-ttu-id="47eb3-123">Se questi valori sono diversi, viene restituito un codice \_ di errore DDERR VISRGNCHANGED al codice in modalità utente.</span><span class="sxs-lookup"><span data-stu-id="47eb3-123">If these values are different, an error code DDERR\_VISRGNCHANGED is returned to the user-mode code.</span></span> <span data-ttu-id="47eb3-124">Il codice in modalità utente eseguirà nuovamente una query sul ritaglio corrente per il desktop, chiamerà **NtGdiDdResetVisrgn** e riproverà a eseguire IDirectDrawSurface7:: BLT applicato all'area primaria, rispettando il nuovo ritaglio.</span><span class="sxs-lookup"><span data-stu-id="47eb3-124">The user-mode code will then re-query the current clipping for the desktop, call **NtGdiDdResetVisrgn**, and re-try the IDirectDrawSurface7::Blt applied to the primary surface, respecting the new clipping.</span></span> <span data-ttu-id="47eb3-125">Infine, il ritaglio che è stato campionato dal codice in modalità utente sarà uguale al ritaglio corrente di proprietà della modalità kernel e IDirectDrawSurface7:: BLT potrà continuare.</span><span class="sxs-lookup"><span data-stu-id="47eb3-125">Eventually, the clipping that was sampled by the user-mode code will be the same as the current clipping owned by kernel mode, and the IDirectDrawSurface7::Blt will be allowed to continue.</span></span>

<span data-ttu-id="47eb3-126">Si consiglia di usare l'interfaccia [IDirectDrawClipper](/previous-versions/aa919448(v=msdn.10)) o [IDirect3DDevice8::P](/previous-versions/ms889707(v=msdn.10)) metodo reinviato per gestire le modifiche di ritaglio asincrono.</span><span class="sxs-lookup"><span data-stu-id="47eb3-126">Applications are advised to use the [IDirectDrawClipper](/previous-versions/aa919448(v=msdn.10)) interface or [IDirect3DDevice8::Present](/previous-versions/ms889707(v=msdn.10)) method to handle asynchronous clipping changes.</span></span> <span data-ttu-id="47eb3-127">Questi costrutti implementano il ritaglio asincrono in modo automatico e indipendente dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="47eb3-127">These constructs implement asynchronous clipping in an automated and operating-system-independent way.</span></span>

## <a name="requirements"></a><span data-ttu-id="47eb3-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="47eb3-128">Requirements</span></span>



| <span data-ttu-id="47eb3-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="47eb3-129">Requirement</span></span> | <span data-ttu-id="47eb3-130">Valore</span><span class="sxs-lookup"><span data-stu-id="47eb3-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="47eb3-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="47eb3-131">Minimum supported client</span></span><br/> | <span data-ttu-id="47eb3-132">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="47eb3-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="47eb3-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="47eb3-133">Minimum supported server</span></span><br/> | <span data-ttu-id="47eb3-134">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="47eb3-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="47eb3-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="47eb3-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="47eb3-136"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="47eb3-136"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47eb3-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="47eb3-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47eb3-138">Supporto client di livello inferiore grafica</span><span class="sxs-lookup"><span data-stu-id="47eb3-138">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="47eb3-139">**DdResetVisrgn**</span><span class="sxs-lookup"><span data-stu-id="47eb3-139">**DdResetVisrgn**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddresetvisrgn)
</dt> </dl>

 

 
