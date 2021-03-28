---
description: ChangePassword non è supportato e può essere modificato o non disponibile in futuro. Usare invece gli account utente con cambio rapido utente e Desktop remoto.
ms.assetid: bc8813a0-9b40-481f-9ab3-cf6a9a0796d2
title: 'Metodo IUserIdentity2:: ChangePassword (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity2.ChangePassword
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: dd4b858924e4b042b3d7a0636d90eb582e9506df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977890"
---
# <a name="iuseridentity2changepassword-method"></a><span data-ttu-id="613ce-104">Metodo IUserIdentity2:: ChangePassword</span><span class="sxs-lookup"><span data-stu-id="613ce-104">IUserIdentity2::ChangePassword method</span></span>

<span data-ttu-id="613ce-105">\[**ChangePassword** non è supportato e può essere modificato o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="613ce-105">\[**ChangePassword** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="613ce-106">Usare invece gli [account utente con cambio rapido utente e desktop remoto](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="613ce-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="613ce-107">Imposta una nuova password per l'identità.</span><span class="sxs-lookup"><span data-stu-id="613ce-107">Sets a new password for the identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="613ce-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="613ce-108">Syntax</span></span>


```C++
HRESULT ChangePassword(
  [in] WCHAR *szOldPass,
  [in] WCHAR *szNewPass
);
```



## <a name="parameters"></a><span data-ttu-id="613ce-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="613ce-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="613ce-110">*szOldPass* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="613ce-110">*szOldPass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="613ce-111">Tipo: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="613ce-111">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="613ce-112">Stringa di caratteri wide che contiene la password attualmente associata all'identità.</span><span class="sxs-lookup"><span data-stu-id="613ce-112">The wide-character string that contains the password currently associated with the identity.</span></span>

</dd> <dt>

<span data-ttu-id="613ce-113">_szNewPass \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="613ce-113">_szNewPass\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="613ce-114">Tipo: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="613ce-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="613ce-115">Stringa di caratteri wide che contiene la nuova password da associare all'identità.</span><span class="sxs-lookup"><span data-stu-id="613ce-115">The wide-character string that contains the new password to be associated with the identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="613ce-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="613ce-116">Return value</span></span>

<span data-ttu-id="613ce-117">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="613ce-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="613ce-118">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="613ce-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="613ce-119">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="613ce-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="613ce-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="613ce-120">Remarks</span></span>

<span data-ttu-id="613ce-121">Il valore di *szOldPass* deve corrispondere alla password corrente dell'identità per l'applicazione di *szNewPass* .</span><span class="sxs-lookup"><span data-stu-id="613ce-121">The value of *szOldPass* must match the current password of the identity for *szNewPass* to be applied.</span></span> <span data-ttu-id="613ce-122">Un valore non corretto di *szOldPass* comporterà un valore restituito di E avrà \_ esito negativo.</span><span class="sxs-lookup"><span data-stu-id="613ce-122">An incorrect value of *szOldPass* will result in a return value of E\_FAIL.</span></span>

## <a name="requirements"></a><span data-ttu-id="613ce-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="613ce-123">Requirements</span></span>



| <span data-ttu-id="613ce-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="613ce-124">Requirement</span></span> | <span data-ttu-id="613ce-125">Valore</span><span class="sxs-lookup"><span data-stu-id="613ce-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="613ce-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="613ce-126">Minimum supported client</span></span><br/> | <span data-ttu-id="613ce-127">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="613ce-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="613ce-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="613ce-128">Minimum supported server</span></span><br/> | <span data-ttu-id="613ce-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="613ce-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="613ce-130">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="613ce-130">End of client support</span></span><br/>    | <span data-ttu-id="613ce-131">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="613ce-131">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="613ce-132">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="613ce-132">End of server support</span></span><br/>    | <span data-ttu-id="613ce-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="613ce-133">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="613ce-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="613ce-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="613ce-135"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="613ce-135"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="613ce-136">IDL</span><span class="sxs-lookup"><span data-stu-id="613ce-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="613ce-137"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="613ce-137"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="613ce-138">DLL</span><span class="sxs-lookup"><span data-stu-id="613ce-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="613ce-139"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="613ce-139"><dt>Msident.dll</dt></span></span> </dl> |



 

 




