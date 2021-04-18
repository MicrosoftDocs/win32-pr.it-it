---
description: 'IUserIdentity:: GetName non è supportato e può essere modificato o non disponibile in futuro. Usare invece gli account utente con cambio rapido utente e Desktop remoto.'
ms.assetid: 4db24dd2-d2b8-4a58-9c16-0e721bc195da
title: 'Metodo IUserIdentity:: GetName (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity.GetName
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 88c0a3d08ff917c2cc9fd59f15e4c23fc22fc79d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979487"
---
# <a name="iuseridentitygetname-method"></a><span data-ttu-id="7adb5-104">Metodo IUserIdentity:: GetName</span><span class="sxs-lookup"><span data-stu-id="7adb5-104">IUserIdentity::GetName method</span></span>

<span data-ttu-id="7adb5-105">\[**IUserIdentity:: GetName** non è supportato e può essere modificato o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="7adb5-105">\[**IUserIdentity::GetName** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="7adb5-106">Usare invece gli [account utente con cambio rapido utente e desktop remoto](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="7adb5-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="7adb5-107">Ottiene il nome associato a questa identità utente.</span><span class="sxs-lookup"><span data-stu-id="7adb5-107">Gets the name associated with this user identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="7adb5-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7adb5-108">Syntax</span></span>


```C++
HRESULT GetName(
  [in] WCHAR *pszName,
  [in] ULONG ulBuffSize
);
```



## <a name="parameters"></a><span data-ttu-id="7adb5-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="7adb5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7adb5-110">*pszName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7adb5-110">*pszName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7adb5-111">Tipo: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="7adb5-111">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="7adb5-112">Puntatore a una stringa di caratteri wide che riceve il nome dell'identità utente.</span><span class="sxs-lookup"><span data-stu-id="7adb5-112">A pointer to a wide-character string that receives the name of this user identity.</span></span>

</dd> <dt>

<span data-ttu-id="7adb5-113">_ulBuffSize \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7adb5-113">_ulBuffSize\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7adb5-114">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="7adb5-114">Type: **ULONG**</span></span>

<span data-ttu-id="7adb5-115">Valore che specifica la dimensione di *pszName*.</span><span class="sxs-lookup"><span data-stu-id="7adb5-115">A value that specifies the size of *pszName*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7adb5-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7adb5-116">Return value</span></span>

<span data-ttu-id="7adb5-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="7adb5-117">Type: **HRESULT**</span></span>

<span data-ttu-id="7adb5-118">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="7adb5-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7adb5-119">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7adb5-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="7adb5-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7adb5-120">Requirements</span></span>



| <span data-ttu-id="7adb5-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="7adb5-121">Requirement</span></span> | <span data-ttu-id="7adb5-122">Valore</span><span class="sxs-lookup"><span data-stu-id="7adb5-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7adb5-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7adb5-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7adb5-124">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="7adb5-124">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="7adb5-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7adb5-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7adb5-126">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7adb5-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="7adb5-127">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="7adb5-127">End of client support</span></span><br/>    | <span data-ttu-id="7adb5-128">Windows XP</span><span class="sxs-lookup"><span data-stu-id="7adb5-128">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="7adb5-129">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="7adb5-129">End of server support</span></span><br/>    | <span data-ttu-id="7adb5-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7adb5-130">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="7adb5-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7adb5-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="7adb5-132"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="7adb5-132"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="7adb5-133">IDL</span><span class="sxs-lookup"><span data-stu-id="7adb5-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7adb5-134"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7adb5-134"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="7adb5-135">DLL</span><span class="sxs-lookup"><span data-stu-id="7adb5-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7adb5-136"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7adb5-136"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7adb5-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7adb5-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7adb5-138">**IUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="7adb5-138">**IUserIdentity**</span></span>](iuseridentity.md)
</dt> <dt>

[<span data-ttu-id="7adb5-139">**SetName**</span><span class="sxs-lookup"><span data-stu-id="7adb5-139">**SetName**</span></span>](iuseridentity2-setname.md)
</dt> </dl>

 

 




