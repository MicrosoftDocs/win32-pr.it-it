---
description: IdentityInformationChanged non è supportato e può essere modificato o non disponibile in futuro. Usare invece gli account utente con cambio rapido utente e Desktop remoto.
ms.assetid: 3aca8a98-3d12-482d-9991-d6b53adde522
title: 'Metodo IIdentityChangeNotify:: IdentityInformationChanged (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IIdentityChangeNotify.IdentityInformationChanged
api_type:
- COM
api_location:
- Msoe.dll
ms.openlocfilehash: c33f67a4def3312564ed943e2a3a917fe2843980
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881546"
---
# <a name="iidentitychangenotifyidentityinformationchanged-method"></a><span data-ttu-id="95794-104">Metodo IIdentityChangeNotify:: IdentityInformationChanged</span><span class="sxs-lookup"><span data-stu-id="95794-104">IIdentityChangeNotify::IdentityInformationChanged method</span></span>

<span data-ttu-id="95794-105">\[**IdentityInformationChanged** non è supportato e può essere modificato o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="95794-105">\[**IdentityInformationChanged** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="95794-106">Usare invece gli [account utente con cambio rapido utente e desktop remoto](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="95794-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="95794-107">Chiamato quando le informazioni relative a un'identità utente sono state modificate o quando un'identità utente è stata aggiunta o eliminata.</span><span class="sxs-lookup"><span data-stu-id="95794-107">Called when information about a user identity has changed, or when a user identity has been added or deleted.</span></span>

## <a name="syntax"></a><span data-ttu-id="95794-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="95794-108">Syntax</span></span>


```C++
HRESULT IdentityInformationChanged(
   DWORD dwType
);
```



## <a name="parameters"></a><span data-ttu-id="95794-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="95794-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95794-110">*dwType*</span><span class="sxs-lookup"><span data-stu-id="95794-110">*dwType*</span></span> 
</dt> <dd>

<span data-ttu-id="95794-111">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="95794-111">Type: **DWORD**</span></span>

<span data-ttu-id="95794-112">Valore che specifica il tipo di informazioni modificate o l'operazione eseguita su un'identità.</span><span class="sxs-lookup"><span data-stu-id="95794-112">A value that specifies the type of information changed, or the operation performed on an identity.</span></span> <span data-ttu-id="95794-113">Può essere una combinazione dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="95794-113">Can be a combination of the following values.</span></span>

<dt>



 <span data-ttu-id="95794-114">(IIC \_ \_identità corrente \_ modificata)</span><span class="sxs-lookup"><span data-stu-id="95794-114">(IIC\_CURRENT\_IDENTITY\_CHANGED)</span></span>


</dt> <dd>

<span data-ttu-id="95794-115">L'identità corrente è stata modificata.</span><span class="sxs-lookup"><span data-stu-id="95794-115">The current identity has been modified.</span></span>

</dd> <dt>



 <span data-ttu-id="95794-116">(IIC \_ IDENTITÀ \_ modificata)</span><span class="sxs-lookup"><span data-stu-id="95794-116">(IIC\_IDENTITY\_CHANGED)</span></span>


</dt> <dd>

<span data-ttu-id="95794-117">Un'identità è stata modificata.</span><span class="sxs-lookup"><span data-stu-id="95794-117">An identity has been modified.</span></span>

</dd> <dt>



 <span data-ttu-id="95794-118">(IIC \_ IDENTITÀ \_ eliminata)</span><span class="sxs-lookup"><span data-stu-id="95794-118">(IIC\_IDENTITY\_DELETED)</span></span>


</dt> <dd>

<span data-ttu-id="95794-119">Un'identità è stata eliminata.</span><span class="sxs-lookup"><span data-stu-id="95794-119">An identity has been deleted.</span></span>

</dd> <dt>



 <span data-ttu-id="95794-120">(IIC \_ IDENTITÀ \_ aggiunta)</span><span class="sxs-lookup"><span data-stu-id="95794-120">(IIC\_IDENTITY\_ADDED)</span></span>


</dt> <dd>

<span data-ttu-id="95794-121">È stata aggiunta una nuova identità.</span><span class="sxs-lookup"><span data-stu-id="95794-121">A new identity has been added.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95794-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="95794-122">Return value</span></span>

<span data-ttu-id="95794-123">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="95794-123">Type: **HRESULT**</span></span>

<span data-ttu-id="95794-124">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="95794-124">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="95794-125">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="95794-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="95794-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="95794-126">Remarks</span></span>

<span data-ttu-id="95794-127">È possibile implementare questo metodo per fornire un comportamento personalizzato per l'applicazione quando l'elenco di identità utente nel sistema è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="95794-127">You may implement this method to provide custom behavior for your application when the list of user identities on the system has been modified.</span></span>

## <a name="requirements"></a><span data-ttu-id="95794-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="95794-128">Requirements</span></span>



| <span data-ttu-id="95794-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="95794-129">Requirement</span></span> | <span data-ttu-id="95794-130">Valore</span><span class="sxs-lookup"><span data-stu-id="95794-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="95794-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="95794-131">Minimum supported client</span></span><br/> | <span data-ttu-id="95794-132">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="95794-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="95794-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="95794-133">Minimum supported server</span></span><br/> | <span data-ttu-id="95794-134">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="95794-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="95794-135">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="95794-135">End of client support</span></span><br/>    | <span data-ttu-id="95794-136">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="95794-136">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="95794-137">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="95794-137">End of server support</span></span><br/>    | <span data-ttu-id="95794-138">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="95794-138">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="95794-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="95794-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="95794-140"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="95794-140"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="95794-141">IDL</span><span class="sxs-lookup"><span data-stu-id="95794-141">IDL</span></span><br/>                      | <dl> <span data-ttu-id="95794-142"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="95794-142"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="95794-143">DLL</span><span class="sxs-lookup"><span data-stu-id="95794-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95794-144"><dt>Msoe.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95794-144"><dt>Msoe.dll</dt></span></span> </dl>    |



 

 




