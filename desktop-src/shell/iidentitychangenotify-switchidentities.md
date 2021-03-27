---
description: Chiamato quando le identità utente sono cambiate.
ms.assetid: e88383fc-e58e-4987-be4b-8ce2ab1368db
title: 'Metodo IIdentityChangeNotify:: SwitchIdentities (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IIdentityChangeNotify.SwitchIdentities
api_type:
- COM
api_location:
- Msoe.dll
ms.openlocfilehash: 925b52a4470c768501dd928784d85a89d05a90c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994597"
---
# <a name="iidentitychangenotifyswitchidentities-method"></a><span data-ttu-id="07b64-103">Metodo IIdentityChangeNotify:: SwitchIdentities</span><span class="sxs-lookup"><span data-stu-id="07b64-103">IIdentityChangeNotify::SwitchIdentities method</span></span>

<span data-ttu-id="07b64-104">\[**SwitchIdentities** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="07b64-104">\[**SwitchIdentities** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="07b64-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.\]</span><span class="sxs-lookup"><span data-stu-id="07b64-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="07b64-106">Chiamato quando le identità utente sono cambiate.</span><span class="sxs-lookup"><span data-stu-id="07b64-106">Called when user identities are switched.</span></span>

## <a name="syntax"></a><span data-ttu-id="07b64-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="07b64-107">Syntax</span></span>


```C++
HRESULT SwitchIdentities();
```



## <a name="parameters"></a><span data-ttu-id="07b64-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="07b64-108">Parameters</span></span>

<span data-ttu-id="07b64-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="07b64-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="07b64-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="07b64-110">Return value</span></span>

<span data-ttu-id="07b64-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="07b64-111">Type: **HRESULT**</span></span>

<span data-ttu-id="07b64-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="07b64-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="07b64-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="07b64-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="07b64-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="07b64-114">Remarks</span></span>

<span data-ttu-id="07b64-115">È possibile implementare questo metodo per fornire un comportamento personalizzato per l'applicazione quando un utente ha cambiato correttamente le identità.</span><span class="sxs-lookup"><span data-stu-id="07b64-115">You may implement this method to provide custom behavior for your application when a user has successfully switched identities.</span></span> <span data-ttu-id="07b64-116">Per fornire un comportamento personalizzato prima che si verifichi un cambio di identità utente, implementare il metodo [**IIdentityChangeNotify:: QuerySwitchIdentities**](iidentitychangenotify-queryswitchidentities.md) .</span><span class="sxs-lookup"><span data-stu-id="07b64-116">To provide custom behavior before a user identity switch occurs, implement the [**IIdentityChangeNotify::QuerySwitchIdentities**](iidentitychangenotify-queryswitchidentities.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="07b64-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="07b64-117">Requirements</span></span>



| <span data-ttu-id="07b64-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="07b64-118">Requirement</span></span> | <span data-ttu-id="07b64-119">Valore</span><span class="sxs-lookup"><span data-stu-id="07b64-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="07b64-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07b64-120">Minimum supported client</span></span><br/> | <span data-ttu-id="07b64-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="07b64-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="07b64-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07b64-122">Minimum supported server</span></span><br/> | <span data-ttu-id="07b64-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="07b64-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="07b64-124">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="07b64-124">End of client support</span></span><br/>    | <span data-ttu-id="07b64-125">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="07b64-125">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="07b64-126">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="07b64-126">End of server support</span></span><br/>    | <span data-ttu-id="07b64-127">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="07b64-127">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="07b64-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="07b64-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="07b64-129"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="07b64-129"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="07b64-130">IDL</span><span class="sxs-lookup"><span data-stu-id="07b64-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="07b64-131"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="07b64-131"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="07b64-132">DLL</span><span class="sxs-lookup"><span data-stu-id="07b64-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07b64-133"><dt>Msoe.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07b64-133"><dt>Msoe.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="07b64-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="07b64-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07b64-135">**IIdentityChangeNotify**</span><span class="sxs-lookup"><span data-stu-id="07b64-135">**IIdentityChangeNotify**</span></span>](iidentitychangenotify.md)
</dt> <dt>

[<span data-ttu-id="07b64-136">**IIdentityChangeNotify::QuerySwitchIdentities**</span><span class="sxs-lookup"><span data-stu-id="07b64-136">**IIdentityChangeNotify::QuerySwitchIdentities**</span></span>](iidentitychangenotify-queryswitchidentities.md)
</dt> </dl>

 

 




