---
description: Determina se il driver è in grado di creare un comando a livello di driver o un buffer vertex della descrizione specificata.
ms.assetid: c67492d9-c4ba-4206-8beb-3d67235192f9
title: Funzione NtGdiDdCanCreateD3DBuffer (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCanCreateD3DBuffer
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 849eb2ba9c1349c54c20703217989b0b92ee78e9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304464"
---
# <a name="ntgdiddcancreated3dbuffer-function"></a><span data-ttu-id="1dd1f-103">NtGdiDdCanCreateD3DBuffer (funzione)</span><span class="sxs-lookup"><span data-stu-id="1dd1f-103">NtGdiDdCanCreateD3DBuffer function</span></span>

<span data-ttu-id="1dd1f-104">\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="1dd1f-105">Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]</span><span class="sxs-lookup"><span data-stu-id="1dd1f-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="1dd1f-106">Determina se il driver è in grado di creare un comando a livello di driver o un buffer vertex della descrizione specificata.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-106">Determines whether the driver can create a driver-level command or vertex buffer of the specified description.</span></span>

## <a name="syntax"></a><span data-ttu-id="1dd1f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1dd1f-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdCanCreateD3DBuffer(
  _In_    HANDLE                   hDirectDraw,
  _Inout_ PDD_CANCREATESURFACEDATA puCanCreateSurfaceData
);
```



## <a name="parameters"></a><span data-ttu-id="1dd1f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1dd1f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1dd1f-109">*hDirectDraw* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1dd1f-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1dd1f-110">Handle per la [**struttura \_ \_ globale di DirectDraw DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) che rappresenta l'oggetto DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-110">Handle to the [**DD\_DIRECTDRAW\_GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) structure representing the DirectDraw object.</span></span>

</dd> <dt>

<span data-ttu-id="1dd1f-111">*puCanCreateSurfaceData* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="1dd1f-111">*puCanCreateSurfaceData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1dd1f-112">Puntatore a una [**struttura \_ CANCREATESURFACEDATA DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_cancreatesurfacedata) .</span><span class="sxs-lookup"><span data-stu-id="1dd1f-112">Pointer to a [**DD\_CANCREATESURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_cancreatesurfacedata) structure.</span></span> <span data-ttu-id="1dd1f-113">Questa struttura contiene le informazioni necessarie affinché il driver determini se è possibile creare un buffer del comando o del vertice.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-113">This structure contains the information required for the driver to determine whether a command or vertex buffer can be created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1dd1f-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1dd1f-114">Return value</span></span>

<span data-ttu-id="1dd1f-115">**NtGdiDdCanCreateD3DBuffer** restituisce uno dei codici di callback seguenti.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-115">**NtGdiDdCanCreateD3DBuffer** returns one of the following callback codes.</span></span>



| <span data-ttu-id="1dd1f-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="1dd1f-116">Return code</span></span>                                                                                              | <span data-ttu-id="1dd1f-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1dd1f-117">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1dd1f-118"><dt>**\_driver DDHAL \_ gestito**</dt></span><span class="sxs-lookup"><span data-stu-id="1dd1f-118"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="1dd1f-119">Il driver ha eseguito l'operazione e ha restituito un codice restituito valido per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-119">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="1dd1f-120">Se il codice è DD \_ OK, DirectDraw o Direct3D procede con la funzione.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-120">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="1dd1f-121">In caso contrario, DirectDraw o Direct3D restituisce il codice di errore fornito dal driver e interrompe la funzione.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-121">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="1dd1f-122"><dt>**\_NOTHANDLED driver \_ DDHAL**</dt></span><span class="sxs-lookup"><span data-stu-id="1dd1f-122"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="1dd1f-123">Il driver non ha commenti sull'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-123">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="1dd1f-124">Se è necessario che il driver implementi un particolare callback, DirectDraw o Direct3D segnala una condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-124">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="1dd1f-125">In caso contrario, DirectDraw o Direct3D gestisce l'operazione come se il callback del driver non fosse stato definito eseguendo l'implementazione di DirectDraw o Direct3D indipendente dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-125">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1dd1f-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1dd1f-126">Requirements</span></span>



| <span data-ttu-id="1dd1f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="1dd1f-127">Requirement</span></span> | <span data-ttu-id="1dd1f-128">Valore</span><span class="sxs-lookup"><span data-stu-id="1dd1f-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1dd1f-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1dd1f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="1dd1f-130">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1dd1f-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="1dd1f-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1dd1f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="1dd1f-132">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1dd1f-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1dd1f-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1dd1f-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="1dd1f-134"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1dd1f-134"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1dd1f-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1dd1f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dd1f-136">Supporto client di livello inferiore grafica</span><span class="sxs-lookup"><span data-stu-id="1dd1f-136">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
