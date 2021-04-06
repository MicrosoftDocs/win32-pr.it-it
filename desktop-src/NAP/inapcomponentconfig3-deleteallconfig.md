---
title: Metodo INapComponentConfig3 DeleteAllConfig (NapCommon. h)
description: Viene implementato da convalida integrità sistema (SHV) per fornire un modo per reimpostare l'archivio di convalida integrità di sistema sullo stato originale dopo l'installazione.
ms.assetid: 7f079743-1c32-430d-a250-b49a96b99f14
keywords:
- NAP metodo DeleteAllConfig
- Metodo DeleteAllConfig NAP, interfaccia INapComponentConfig3
- Interfaccia INapComponentConfig3 NAP, metodo DeleteAllConfig
topic_type:
- apiref
api_name:
- INapComponentConfig3.DeleteAllConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12a766690114db20fb9be5cccbd4508f4565f2cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873565"
---
# <a name="inapcomponentconfig3deleteallconfig-method"></a><span data-ttu-id="ed9c8-106">INapComponentConfig3::D Metodo eleteAllConfig</span><span class="sxs-lookup"><span data-stu-id="ed9c8-106">INapComponentConfig3::DeleteAllConfig method</span></span>

> [!Note]  
> <span data-ttu-id="ed9c8-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="ed9c8-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="ed9c8-108">Il metodo **DeleteAllConfig** viene implementato da convalida integrità sistema (SHV) per fornire un modo per reimpostare l'archivio di convalida integrità di sistema sullo stato originale dopo l'installazione.</span><span class="sxs-lookup"><span data-stu-id="ed9c8-108">The **DeleteAllConfig** method is implemented by system health validators (SHVs) to provide a way to reset the SHV store to its original state after setup.</span></span> <span data-ttu-id="ed9c8-109">È necessario eliminare tutti i dati di configurazione ad eccezione della configurazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="ed9c8-109">All configuration data except for the default configuration must be deleted.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed9c8-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ed9c8-110">Syntax</span></span>


```C++
HRESULT DeleteAllConfig();
```



## <a name="parameters"></a><span data-ttu-id="ed9c8-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="ed9c8-111">Parameters</span></span>

<span data-ttu-id="ed9c8-112">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="ed9c8-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ed9c8-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ed9c8-113">Return value</span></span>

<span data-ttu-id="ed9c8-114">Restituisce uno dei seguenti codici di errore in base al risultato di questa operazione.</span><span class="sxs-lookup"><span data-stu-id="ed9c8-114">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="ed9c8-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="ed9c8-115">Return code</span></span>                                                                           | <span data-ttu-id="ed9c8-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ed9c8-116">Description</span></span>                             |
|---------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="ed9c8-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ed9c8-117"><dt>**S\_OK** </dt></span></span> </dl> | <span data-ttu-id="ed9c8-118">L'operazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="ed9c8-118">The operation is successful.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ed9c8-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ed9c8-119">Requirements</span></span>



| <span data-ttu-id="ed9c8-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed9c8-120">Requirement</span></span> | <span data-ttu-id="ed9c8-121">Valore</span><span class="sxs-lookup"><span data-stu-id="ed9c8-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed9c8-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed9c8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ed9c8-123">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ed9c8-123">None supported</span></span><br/>                                                                |
| <span data-ttu-id="ed9c8-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed9c8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ed9c8-125">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="ed9c8-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ed9c8-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ed9c8-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed9c8-127"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed9c8-127"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="ed9c8-128">IDL</span><span class="sxs-lookup"><span data-stu-id="ed9c8-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ed9c8-129"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ed9c8-129"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed9c8-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ed9c8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed9c8-131">**INapComponentConfig3**</span><span class="sxs-lookup"><span data-stu-id="ed9c8-131">**INapComponentConfig3**</span></span>](inapcomponentconfig3.md)
</dt> </dl>

 

 





