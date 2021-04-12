---
description: Imposta il valore della chiave di colore per la superficie specificata.
ms.assetid: 052dba97-c047-4ef7-a908-2a66ade3af10
title: Funzione NtGdiDdSetColorKey (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdSetColorKey
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 7d6186df13ee88ca3de4f123381c012548b1cd85
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523002"
---
# <a name="ntgdiddsetcolorkey-function"></a><span data-ttu-id="3711d-103">NtGdiDdSetColorKey (funzione)</span><span class="sxs-lookup"><span data-stu-id="3711d-103">NtGdiDdSetColorKey function</span></span>

<span data-ttu-id="3711d-104">\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="3711d-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="3711d-105">Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]</span><span class="sxs-lookup"><span data-stu-id="3711d-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="3711d-106">Imposta il valore della chiave di colore per la superficie specificata.</span><span class="sxs-lookup"><span data-stu-id="3711d-106">Sets the color key value for the specified surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="3711d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3711d-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdSetColorKey(
  _In_    HANDLE              hSurface,
  _Inout_ PDD_SETCOLORKEYDATA puSetColorKeyData
);
```



## <a name="parameters"></a><span data-ttu-id="3711d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3711d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3711d-109">*hSurface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3711d-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3711d-110">Puntatore alla struttura [**\_ \_ locale della superficie DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) che descrive la superficie a cui deve essere associata la chiave di colore.</span><span class="sxs-lookup"><span data-stu-id="3711d-110">Pointer to the [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that describes the surface with which the color key is to be associated.</span></span>

</dd> <dt>

<span data-ttu-id="3711d-111">*puSetColorKeyData* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="3711d-111">*puSetColorKeyData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3711d-112">Puntatore a una struttura [**DD \_ SETCOLORKEYDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_setcolorkeydata) che contiene le informazioni necessarie per impostare la chiave di colore per la superficie specificata.</span><span class="sxs-lookup"><span data-stu-id="3711d-112">Pointer to a [**DD\_SETCOLORKEYDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_setcolorkeydata) structure that contains the information required to set the color key for the specified surface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3711d-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3711d-113">Return value</span></span>

<span data-ttu-id="3711d-114">**NtGdiDdSetColorKey** restituisce uno dei codici di callback seguenti.</span><span class="sxs-lookup"><span data-stu-id="3711d-114">**NtGdiDdSetColorKey** returns one of the following callback codes.</span></span>



| <span data-ttu-id="3711d-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="3711d-115">Return code</span></span>                                                                                              | <span data-ttu-id="3711d-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3711d-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3711d-117"><dt>**\_driver DDHAL \_ gestito**</dt></span><span class="sxs-lookup"><span data-stu-id="3711d-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="3711d-118">Il driver ha eseguito l'operazione e ha restituito un codice restituito valido per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="3711d-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="3711d-119">Se il codice è DD \_ OK, DirectDraw o Direct3D procede con la funzione.</span><span class="sxs-lookup"><span data-stu-id="3711d-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="3711d-120">In caso contrario, DirectDraw o Direct3D restituisce il codice di errore fornito dal driver e interrompe la funzione.</span><span class="sxs-lookup"><span data-stu-id="3711d-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="3711d-121"><dt>**\_NOTHANDLED driver \_ DDHAL**</dt></span><span class="sxs-lookup"><span data-stu-id="3711d-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="3711d-122">Il driver non ha commenti sull'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="3711d-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="3711d-123">Se è necessario che il driver implementi un particolare callback, DirectDraw o Direct3D segnala una condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="3711d-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="3711d-124">In caso contrario, DirectDraw o Direct3D gestisce l'operazione come se il callback del driver non fosse stato definito eseguendo l'implementazione di DirectDraw o Direct3D indipendente dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3711d-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3711d-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3711d-125">Requirements</span></span>



| <span data-ttu-id="3711d-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="3711d-126">Requirement</span></span> | <span data-ttu-id="3711d-127">Valore</span><span class="sxs-lookup"><span data-stu-id="3711d-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3711d-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3711d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3711d-129">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3711d-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="3711d-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3711d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3711d-131">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3711d-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3711d-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3711d-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="3711d-133"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="3711d-133"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3711d-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3711d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3711d-135">Supporto client di livello inferiore grafica</span><span class="sxs-lookup"><span data-stu-id="3711d-135">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
