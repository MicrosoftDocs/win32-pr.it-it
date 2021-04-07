---
title: Metodo Session. Delete (WSManDisp. h)
description: Elimina la risorsa specificata nell'URI della risorsa.
ms.assetid: 8803d35d-674c-483d-866b-37129102c7ce
ms.tgt_platform: multiple
keywords:
- Elimina Gestione remota Windows del metodo
- Elimina Gestione remota Windows metodo, oggetto sessione
- Gestione remota Windows oggetto sessione, metodo Delete
topic_type:
- apiref
api_name:
- Session.Delete
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaf4b46997a7e3cf50dbf50c2828de78a814a513
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963951"
---
# <a name="sessiondelete-method"></a><span data-ttu-id="461b0-106">Metodo Session. Delete</span><span class="sxs-lookup"><span data-stu-id="461b0-106">Session.Delete method</span></span>

<span data-ttu-id="461b0-107">Elimina la risorsa specificata nell'URI della risorsa.</span><span class="sxs-lookup"><span data-stu-id="461b0-107">Deletes the resource specified in the resource URI.</span></span>

## <a name="syntax"></a><span data-ttu-id="461b0-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="461b0-108">Syntax</span></span>


```VB
Session.Delete( _
  ByVal resourceUri, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="461b0-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="461b0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="461b0-110">*resourceUri* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="461b0-110">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="461b0-111">URI della risorsa da eliminare.</span><span class="sxs-lookup"><span data-stu-id="461b0-111">The URI of the resource to be deleted.</span></span> <span data-ttu-id="461b0-112">È anche possibile usare un oggetto [**resourceLocator**](resourcelocator.md) per specificare la risorsa.</span><span class="sxs-lookup"><span data-stu-id="461b0-112">You can also use a [**ResourceLocator**](resourcelocator.md) object to specify the resource.</span></span>

</dd> <dt>

<span data-ttu-id="461b0-113">*flag* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="461b0-113">*flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="461b0-114">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="461b0-114">Reserved for future use.</span></span> <span data-ttu-id="461b0-115">Deve essere 0.</span><span class="sxs-lookup"><span data-stu-id="461b0-115">Must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="461b0-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="461b0-116">Return value</span></span>

<span data-ttu-id="461b0-117">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="461b0-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="461b0-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="461b0-118">Remarks</span></span>

<span data-ttu-id="461b0-119">Per chiamare questo metodo, viene usata la sintassi seguente.</span><span class="sxs-lookup"><span data-stu-id="461b0-119">The following syntax is used to call this method.</span></span>


```VB
session.Delete("<resourceUri>")
```



## <a name="examples"></a><span data-ttu-id="461b0-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="461b0-120">Examples</span></span>

<span data-ttu-id="461b0-121">Nell'esempio di codice VBScript seguente vengono eliminati i listener configurati per il trasporto HTTP.</span><span class="sxs-lookup"><span data-stu-id="461b0-121">The following VBScript code example deletes the listeners configured for HTTP transport.</span></span>


```VB
Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
  "config/Listener?Address=*+Transport=HTTP"
objSession.Delete(strResource)
```



## <a name="requirements"></a><span data-ttu-id="461b0-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="461b0-122">Requirements</span></span>



| <span data-ttu-id="461b0-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="461b0-123">Requirement</span></span> | <span data-ttu-id="461b0-124">Valore</span><span class="sxs-lookup"><span data-stu-id="461b0-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="461b0-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="461b0-125">Minimum supported client</span></span><br/> | <span data-ttu-id="461b0-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="461b0-126">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="461b0-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="461b0-127">Minimum supported server</span></span><br/> | <span data-ttu-id="461b0-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="461b0-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="461b0-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="461b0-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="461b0-130"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="461b0-130"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="461b0-131">IDL</span><span class="sxs-lookup"><span data-stu-id="461b0-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="461b0-132"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="461b0-132"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="461b0-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="461b0-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="461b0-134"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="461b0-134"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="461b0-135">DLL</span><span class="sxs-lookup"><span data-stu-id="461b0-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="461b0-136"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="461b0-136"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="461b0-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="461b0-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="461b0-138">**Sessione**</span><span class="sxs-lookup"><span data-stu-id="461b0-138">**Session**</span></span>](session.md)
</dt> </dl>

 

 





