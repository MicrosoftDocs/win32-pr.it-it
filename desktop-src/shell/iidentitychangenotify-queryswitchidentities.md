---
description: Viene chiamato quando l'utente corrente ha richiesto la commutazione dell'identità utente, ma prima che si verifichi l'opzione.
ms.assetid: f159b829-623c-4348-9692-7317663811a7
title: 'Metodo IIdentityChangeNotify:: QuerySwitchIdentities (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IIdentityChangeNotify.QuerySwitchIdentities
api_type:
- COM
api_location:
- Msoe.dll
ms.openlocfilehash: 42f8033c943e402d434c973f8c768ed5a951811d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881545"
---
# <a name="iidentitychangenotifyqueryswitchidentities-method"></a><span data-ttu-id="960e6-103">Metodo IIdentityChangeNotify:: QuerySwitchIdentities</span><span class="sxs-lookup"><span data-stu-id="960e6-103">IIdentityChangeNotify::QuerySwitchIdentities method</span></span>

<span data-ttu-id="960e6-104">\[**QuerySwitchIdentities** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="960e6-104">\[**QuerySwitchIdentities** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="960e6-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.\]</span><span class="sxs-lookup"><span data-stu-id="960e6-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="960e6-106">Viene chiamato quando l'utente corrente ha richiesto la commutazione dell'identità utente, ma prima che si verifichi l'opzione.</span><span class="sxs-lookup"><span data-stu-id="960e6-106">Called when the current user has requested that their user identity be switched, but before the switch occurs.</span></span>

## <a name="syntax"></a><span data-ttu-id="960e6-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="960e6-107">Syntax</span></span>


```C++
HRESULT QuerySwitchIdentities();
```



## <a name="parameters"></a><span data-ttu-id="960e6-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="960e6-108">Parameters</span></span>

<span data-ttu-id="960e6-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="960e6-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="960e6-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="960e6-110">Return value</span></span>

<span data-ttu-id="960e6-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="960e6-111">Type: **HRESULT**</span></span>

<span data-ttu-id="960e6-112">Risultato della query switch.</span><span class="sxs-lookup"><span data-stu-id="960e6-112">Result of the switch query.</span></span> <span data-ttu-id="960e6-113">Se l'opzione deve continuare, restituire S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="960e6-113">If the switch should proceed, return S\_OK.</span></span> <span data-ttu-id="960e6-114">In caso contrario, \_ restituire \_ l'opzione E processo annullato \_ per indicare che il cambio di identità utente deve essere interrotto.</span><span class="sxs-lookup"><span data-stu-id="960e6-114">Otherwise, return E\_PROCESS\_CANCELLED\_SWITCH to indicate that the user identity switch should be aborted.</span></span>

## <a name="remarks"></a><span data-ttu-id="960e6-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="960e6-115">Remarks</span></span>

<span data-ttu-id="960e6-116">È possibile implementare questo metodo per fornire un comportamento personalizzato all'applicazione quando un utente richiede la commutazione delle identità.</span><span class="sxs-lookup"><span data-stu-id="960e6-116">You may implement this method to provide custom behavior for your application when a user requests that identities be switched.</span></span> <span data-ttu-id="960e6-117">È possibile arrestare il cambio di identità in sospeso restituendo l'opzione valore E \_ processo \_ annullato \_ .</span><span class="sxs-lookup"><span data-stu-id="960e6-117">You can stop the pending identity switch by returning the value E\_PROCESS\_CANCELLED\_SWITCH.</span></span>

## <a name="requirements"></a><span data-ttu-id="960e6-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="960e6-118">Requirements</span></span>



| <span data-ttu-id="960e6-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="960e6-119">Requirement</span></span> | <span data-ttu-id="960e6-120">Valore</span><span class="sxs-lookup"><span data-stu-id="960e6-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="960e6-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="960e6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="960e6-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="960e6-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="960e6-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="960e6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="960e6-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="960e6-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="960e6-125">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="960e6-125">End of client support</span></span><br/>    | <span data-ttu-id="960e6-126">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="960e6-126">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="960e6-127">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="960e6-127">End of server support</span></span><br/>    | <span data-ttu-id="960e6-128">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="960e6-128">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="960e6-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="960e6-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="960e6-130"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="960e6-130"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="960e6-131">IDL</span><span class="sxs-lookup"><span data-stu-id="960e6-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="960e6-132"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="960e6-132"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="960e6-133">DLL</span><span class="sxs-lookup"><span data-stu-id="960e6-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="960e6-134"><dt>Msoe.dll</dt></span><span class="sxs-lookup"><span data-stu-id="960e6-134"><dt>Msoe.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="960e6-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="960e6-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="960e6-136">**IIdentityChangeNotify**</span><span class="sxs-lookup"><span data-stu-id="960e6-136">**IIdentityChangeNotify**</span></span>](iidentitychangenotify.md)
</dt> <dt>

[<span data-ttu-id="960e6-137">**IIdentityChangeNotify::SwitchIdentities**</span><span class="sxs-lookup"><span data-stu-id="960e6-137">**IIdentityChangeNotify::SwitchIdentities**</span></span>](iidentitychangenotify-switchidentities.md)
</dt> </dl>

 

 




