---
description: Restituisce il numero di passaggi in cui l'hardware può eseguire le operazioni di fusione specificate nello stato corrente.
ms.assetid: 355dae78-cd65-4fc9-8f08-8e5ae123064b
title: Funzione NtGdiD3DValidateTextureStageState (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiD3DValidateTextureStageState
api_type:
- HeaderDef
api_location:
- Ntgdi.h
ms.openlocfilehash: 37c852343c70c5d3325926c9108dcab2948fdc95
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877458"
---
# <a name="ntgdid3dvalidatetexturestagestate-function"></a><span data-ttu-id="3640f-103">NtGdiD3DValidateTextureStageState (funzione)</span><span class="sxs-lookup"><span data-stu-id="3640f-103">NtGdiD3DValidateTextureStageState function</span></span>

<span data-ttu-id="3640f-104">\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="3640f-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="3640f-105">Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]</span><span class="sxs-lookup"><span data-stu-id="3640f-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="3640f-106">Restituisce il numero di passaggi in cui l'hardware può eseguire le operazioni di fusione specificate nello stato corrente.</span><span class="sxs-lookup"><span data-stu-id="3640f-106">Returns the number of passes where the hardware can perform the blending operations specified in the current state.</span></span>

## <a name="syntax"></a><span data-ttu-id="3640f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3640f-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiD3DValidateTextureStageState(
  _Inout_ LPD3DNTHAL_VALIDATETEXTURESTAGESTATEDATA pData
);
```



## <a name="parameters"></a><span data-ttu-id="3640f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3640f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3640f-109">*pData* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="3640f-109">*pData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3640f-110">Puntatore a una struttura [**D3DNTHAL \_ VALIDATETEXTURESTAGESTATEDATA**](/windows-hardware/drivers/ddi/) che contiene le informazioni necessarie per determinare e restituire il numero di passaggi necessari per eseguire le operazioni di fusione.</span><span class="sxs-lookup"><span data-stu-id="3640f-110">Pointer to a [**D3DNTHAL\_VALIDATETEXTURESTAGESTATEDATA**](/windows-hardware/drivers/ddi/) structure that contains the information required for the driver to determine and return the number of passes required to perform the blending operations.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3640f-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3640f-111">Return value</span></span>

<span data-ttu-id="3640f-112">**NtGdiD3DValidateTextureStageState** restituisce uno dei codici di callback seguenti.</span><span class="sxs-lookup"><span data-stu-id="3640f-112">**NtGdiD3DValidateTextureStageState** returns one of the following callback codes.</span></span>



| <span data-ttu-id="3640f-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="3640f-113">Return code</span></span>                                                                                              | <span data-ttu-id="3640f-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3640f-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3640f-115"><dt>**\_driver DDHAL \_ gestito**</dt></span><span class="sxs-lookup"><span data-stu-id="3640f-115"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="3640f-116">Il driver ha eseguito l'operazione e ha restituito un codice restituito valido per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="3640f-116">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="3640f-117">Se il codice è DD \_ OK, DirectDraw o Direct3D procede con la funzione.</span><span class="sxs-lookup"><span data-stu-id="3640f-117">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="3640f-118">In caso contrario, DirectDraw o Direct3D restituisce il codice di errore fornito dal driver e interrompe la funzione.</span><span class="sxs-lookup"><span data-stu-id="3640f-118">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="3640f-119"><dt>**\_NOTHANDLED driver \_ DDHAL**</dt></span><span class="sxs-lookup"><span data-stu-id="3640f-119"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="3640f-120">Il driver non ha commenti sull'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="3640f-120">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="3640f-121">Se è necessario che il driver implementi un particolare callback, DirectDraw o Direct3D segnala una condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="3640f-121">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="3640f-122">In caso contrario, DirectDraw o Direct3D gestisce l'operazione come se il callback del driver non fosse stato definito eseguendo l'implementazione di DirectDraw o Direct3D indipendente dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3640f-122">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3640f-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3640f-123">Requirements</span></span>



| <span data-ttu-id="3640f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="3640f-124">Requirement</span></span> | <span data-ttu-id="3640f-125">Valore</span><span class="sxs-lookup"><span data-stu-id="3640f-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3640f-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3640f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3640f-127">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3640f-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="3640f-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3640f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3640f-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3640f-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3640f-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3640f-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="3640f-131"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="3640f-131"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3640f-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3640f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3640f-133">Supporto client di livello inferiore grafica</span><span class="sxs-lookup"><span data-stu-id="3640f-133">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
