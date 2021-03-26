---
description: 'IUserIdentity2:: Sename non è supportato e può essere modificato o non disponibile in futuro. Usare invece gli account utente con cambio rapido utente e Desktop remoto.'
ms.assetid: 1c9c3beb-fa1c-4b4d-9cfd-656b97949036
title: 'Metodo IUserIdentity2:: SetValue (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity2.SetName
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 0b0fd06ef4b582987e41c2343f2d4596db6b8528
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980039"
---
# <a name="iuseridentity2setname-method"></a><span data-ttu-id="b4791-104">Metodo IUserIdentity2:: SetValue</span><span class="sxs-lookup"><span data-stu-id="b4791-104">IUserIdentity2::SetName method</span></span>

<span data-ttu-id="b4791-105">\[**IUserIdentity2:: Sename** non è supportato e può essere modificato o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="b4791-105">\[**IUserIdentity2::SetName** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="b4791-106">Usare invece gli [account utente con cambio rapido utente e desktop remoto](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="b4791-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="b4791-107">Imposta il nome visualizzato dell'identità.</span><span class="sxs-lookup"><span data-stu-id="b4791-107">Sets the display name of the identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4791-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b4791-108">Syntax</span></span>


```C++
HRESULT SetName(
  [in] WCHAR *pszName
);
```



## <a name="parameters"></a><span data-ttu-id="b4791-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="b4791-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4791-110">*pszName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b4791-110">*pszName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4791-111">Tipo: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="b4791-111">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="b4791-112">Stringa di caratteri wide che contiene il nuovo nome dell'identità.</span><span class="sxs-lookup"><span data-stu-id="b4791-112">The wide-character string that contains the new name of the identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4791-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b4791-113">Return value</span></span>

<span data-ttu-id="b4791-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="b4791-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="b4791-115">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b4791-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b4791-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b4791-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4791-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b4791-117">Requirements</span></span>



| <span data-ttu-id="b4791-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4791-118">Requirement</span></span> | <span data-ttu-id="b4791-119">Valore</span><span class="sxs-lookup"><span data-stu-id="b4791-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4791-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b4791-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b4791-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b4791-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b4791-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b4791-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b4791-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b4791-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b4791-124">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="b4791-124">End of client support</span></span><br/>    | <span data-ttu-id="b4791-125">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b4791-125">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="b4791-126">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="b4791-126">End of server support</span></span><br/>    | <span data-ttu-id="b4791-127">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b4791-127">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="b4791-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b4791-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4791-129"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4791-129"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="b4791-130">IDL</span><span class="sxs-lookup"><span data-stu-id="b4791-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b4791-131"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b4791-131"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="b4791-132">DLL</span><span class="sxs-lookup"><span data-stu-id="b4791-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4791-133"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4791-133"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4791-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b4791-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4791-135">**IUserIdentity2**</span><span class="sxs-lookup"><span data-stu-id="b4791-135">**IUserIdentity2**</span></span>](iuseridentity2.md)
</dt> <dt>

[<span data-ttu-id="b4791-136">**GetName**</span><span class="sxs-lookup"><span data-stu-id="b4791-136">**GetName**</span></span>](iuseridentity-getname.md)
</dt> </dl>

 

 




