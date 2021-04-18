---
title: Proprietà Session.BatchItems (WSManDisp. h)
description: Imposta e ottiene il numero di elementi in ogni batch di enumerazione.
ms.assetid: 1675ba12-a0c7-4e59-a013-2109780e8afe
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows proprietà BatchItems
- Gestione remota Windows proprietà BatchItems, oggetto Session
- Gestione remota Windows oggetto sessione, proprietà BatchItems
topic_type:
- apiref
api_name:
- Session.BatchItems
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb668b80a2fea8ec5c8683a7a85a20cfbb217a7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302329"
---
# <a name="sessionbatchitems-property"></a><span data-ttu-id="5c69a-106">Session.Batproprietà chItems</span><span class="sxs-lookup"><span data-stu-id="5c69a-106">Session.BatchItems property</span></span>

<span data-ttu-id="5c69a-107">Imposta e ottiene il numero di elementi in ogni batch di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="5c69a-107">Sets and gets the number of items in each enumeration batch.</span></span> <span data-ttu-id="5c69a-108">Questo valore non può essere modificato durante un'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="5c69a-108">This value cannot be changed during an enumeration.</span></span> <span data-ttu-id="5c69a-109">Il provider di risorse può impostare un limite.</span><span class="sxs-lookup"><span data-stu-id="5c69a-109">The resource provider may set a limit.</span></span>

<span data-ttu-id="5c69a-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="5c69a-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c69a-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5c69a-111">Syntax</span></span>


```VB
Session.BatchItems As long
```



## <a name="property-value"></a><span data-ttu-id="5c69a-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="5c69a-112">Property value</span></span>

<span data-ttu-id="5c69a-113">Specifica il numero massimo di elementi restituiti per ogni chiamata di rete sottostante al servizio.</span><span class="sxs-lookup"><span data-stu-id="5c69a-113">Specifies the maximum number of elements returned for each underlying network call to the service.</span></span> <span data-ttu-id="5c69a-114">Il valore predefinito è 20.</span><span class="sxs-lookup"><span data-stu-id="5c69a-114">The default is 20.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c69a-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="5c69a-115">Remarks</span></span>

<span data-ttu-id="5c69a-116">Si tratta di una funzionalità di ottimizzazione che controlla la frequenza con cui vengono effettuate chiamate di rete tra il client e il server.</span><span class="sxs-lookup"><span data-stu-id="5c69a-116">This is an optimization feature that controls how often network calls are made between the client and the server.</span></span> <span data-ttu-id="5c69a-117">Attualmente, viene usato solo per le enumerazioni.</span><span class="sxs-lookup"><span data-stu-id="5c69a-117">Currently, it is used only for enumerations.</span></span> <span data-ttu-id="5c69a-118">Per ulteriori informazioni sull'enumerazione delle risorse [**, vedere Enumerazione**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="5c69a-118">For more information about enumerating resources, see [**Enumerate**](session-enumerate.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5c69a-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5c69a-119">Requirements</span></span>



| <span data-ttu-id="5c69a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c69a-120">Requirement</span></span> | <span data-ttu-id="5c69a-121">Valore</span><span class="sxs-lookup"><span data-stu-id="5c69a-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c69a-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c69a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5c69a-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5c69a-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="5c69a-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c69a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5c69a-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5c69a-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="5c69a-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5c69a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c69a-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c69a-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5c69a-128">IDL</span><span class="sxs-lookup"><span data-stu-id="5c69a-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5c69a-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5c69a-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="5c69a-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="5c69a-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="5c69a-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5c69a-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5c69a-132">DLL</span><span class="sxs-lookup"><span data-stu-id="5c69a-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c69a-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c69a-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5c69a-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5c69a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c69a-135">**Sessione**</span><span class="sxs-lookup"><span data-stu-id="5c69a-135">**Session**</span></span>](session.md)
</dt> <dt>

[<span data-ttu-id="5c69a-136">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="5c69a-136">**Enumerate**</span></span>](session-enumerate.md)
</dt> <dt>

[<span data-ttu-id="5c69a-137">**Enumeratore. ReadItem**</span><span class="sxs-lookup"><span data-stu-id="5c69a-137">**Enumerator.ReadItem**</span></span>](enumerator-readitem.md)
</dt> </dl>

 

 





