---
description: Ottiene il certificato dalle credenziali dell'utente.
ms.assetid: 3C79D049-89DC-4AF5-8C0A-5B7EBBBD69D3
title: Funzione GetCertificateFromCred (Lsaidprov. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCertificateFromCred
api_type:
- HeaderDef
api_location:
- Lsaidprov.h
ms.openlocfilehash: 1120e7859080657e2a04202e01a01464694a3450
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310475"
---
# <a name="getcertificatefromcred-function"></a><span data-ttu-id="2a8fd-103">GetCertificateFromCred (funzione)</span><span class="sxs-lookup"><span data-stu-id="2a8fd-103">GetCertificateFromCred function</span></span>

<span data-ttu-id="2a8fd-104">Ottiene il certificato dalle credenziali dell'utente.</span><span class="sxs-lookup"><span data-stu-id="2a8fd-104">Gets the certificate from the user credential.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a8fd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2a8fd-105">Syntax</span></span>


```C++
NTSTATUS GetCertificateFromCred(
  _In_  PVOID  ProviderHandle,
  _In_  HANDLE ClientToken,
  _In_  PVOID  SuppliedCred,
  _In_  ULONG  SuppliedCredSize,
  _Out_ PVOID  *CertContext
);
```



## <a name="parameters"></a><span data-ttu-id="2a8fd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2a8fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a8fd-107">*ProviderHandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2a8fd-107">*ProviderHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a8fd-108">Handle del provider di identità.</span><span class="sxs-lookup"><span data-stu-id="2a8fd-108">Identity provider handle.</span></span>

</dd> <dt>

<span data-ttu-id="2a8fd-109">*ClientToken* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2a8fd-109">*ClientToken* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a8fd-110">Token del chiamante che sta recuperando il certificato.</span><span class="sxs-lookup"><span data-stu-id="2a8fd-110">Token of the caller who is retrieving the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="2a8fd-111">*SuppliedCred* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2a8fd-111">*SuppliedCred* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a8fd-112">Puntatore a una struttura [**di \_ \_ credenziali fornita da SECPKG**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_supplied_credential) che contiene le credenziali di un ID online di cui è richiesto il certificato.</span><span class="sxs-lookup"><span data-stu-id="2a8fd-112">A pointer to a [**SECPKG\_SUPPLIED\_CREDENTIAL**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_supplied_credential) structure that contains the credential of an online ID whose certificate is requested.</span></span> <span data-ttu-id="2a8fd-113">Il provider di identità deve convalidare i dati di input come se provenisse da un'origine non attendibile.</span><span class="sxs-lookup"><span data-stu-id="2a8fd-113">The identity provider must validate the input data as if it is coming from an untrusted source.</span></span>

</dd> <dt>

<span data-ttu-id="2a8fd-114">*SuppliedCredSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2a8fd-114">*SuppliedCredSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a8fd-115">Dimensione, in byte, del buffer *SuppliedCred* .</span><span class="sxs-lookup"><span data-stu-id="2a8fd-115">The size, in bytes, of the *SuppliedCred* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="2a8fd-116">*CertContext* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2a8fd-116">*CertContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2a8fd-117">Se la funzione ha esito positivo, questo parametro è un puntatore al puntatore di contesto CCERT restituito \_ .</span><span class="sxs-lookup"><span data-stu-id="2a8fd-117">If the function succeeds, this parameter is a pointer to the returned CCERT\_CONTEXT pointer.</span></span> <span data-ttu-id="2a8fd-118">Al termine dell'utilizzo del contesto del certificato, rilasciarlo chiamando la funzione [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) .</span><span class="sxs-lookup"><span data-stu-id="2a8fd-118">When you have finished using the certificate context, release it by calling the [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a8fd-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2a8fd-119">Return value</span></span>

<span data-ttu-id="2a8fd-120">Se la funzione ha esito positivo, la funzione restituisce lo stato \_ Success.</span><span class="sxs-lookup"><span data-stu-id="2a8fd-120">If the function succeeds, the function returns STATUS\_SUCCESS.</span></span>

<span data-ttu-id="2a8fd-121">Se la funzione ha esito negativo, la funzione può restituire uno dei codici di errore NTSTATUS seguenti.</span><span class="sxs-lookup"><span data-stu-id="2a8fd-121">If the function fails, the function may return one of the following NTSTATUS error codes.</span></span>



| <span data-ttu-id="2a8fd-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2a8fd-122">Return value</span></span>                                                                                            | <span data-ttu-id="2a8fd-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2a8fd-123">Description</span></span>                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2a8fd-124"><dt>STATO \_ non \_ supportato</dt></span><span class="sxs-lookup"><span data-stu-id="2a8fd-124"><dt>STATUS\_NOT\_SUPPORTED</dt></span></span> </dl>       | <span data-ttu-id="2a8fd-125">Il provider di identità non riconosce il tipo di credenziale delle credenziali fornite.</span><span class="sxs-lookup"><span data-stu-id="2a8fd-125">The identity provider does not recognize the credential type of the supplied credential.</span></span> <span data-ttu-id="2a8fd-126">LSA tenterà il provider di identità successivo.</span><span class="sxs-lookup"><span data-stu-id="2a8fd-126">LSA will try the next identity provider.</span></span><br/>                                           |
| <dl> <span data-ttu-id="2a8fd-127"><dt>\_errore di accesso stato \_</dt></span><span class="sxs-lookup"><span data-stu-id="2a8fd-127"><dt>STATUS\_LOGON\_FAILURE</dt></span></span> </dl>       | <span data-ttu-id="2a8fd-128">Le credenziali non sono corrette.</span><span class="sxs-lookup"><span data-stu-id="2a8fd-128">The credential is incorrect.</span></span><br/>                                                                                                                                                |
| <dl> <span data-ttu-id="2a8fd-129"><dt>STATO \_ parametro non valido \_</dt></span><span class="sxs-lookup"><span data-stu-id="2a8fd-129"><dt>STATUS\_INVALID\_PARAMETER</dt></span></span> </dl>   | <span data-ttu-id="2a8fd-130">Un parametro non è valido.</span><span class="sxs-lookup"><span data-stu-id="2a8fd-130">A parameter is not valid.</span></span> <span data-ttu-id="2a8fd-131">La credenziale potrebbe essere in un formato non corretto e non nella struttura di [**\_ \_ credenziali specificata SECPKG**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_supplied_credential) .</span><span class="sxs-lookup"><span data-stu-id="2a8fd-131">The credential may be in an incorrect format and not in the defined [**SECPKG\_SUPPLIED\_CREDENTIAL**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_supplied_credential) structure.</span></span><br/> |
| <dl> <span data-ttu-id="2a8fd-132"><dt>rete di stato \_ \_ irraggiungibile</dt></span><span class="sxs-lookup"><span data-stu-id="2a8fd-132"><dt>STATUS\_NETWORK\_UNREACHABLE</dt></span></span> </dl> | <span data-ttu-id="2a8fd-133">Il provider di identità non può contattare il cloud per ottenere il certificato.</span><span class="sxs-lookup"><span data-stu-id="2a8fd-133">The identity provider cannot contact the cloud to obtain the certificate.</span></span><br/>                                                                                                   |
| <dl> <span data-ttu-id="2a8fd-134"><dt>PASSWORD di stato \_ \_ scaduta</dt></span><span class="sxs-lookup"><span data-stu-id="2a8fd-134"><dt>STATUS\_PASSWORD\_EXPIRED</dt></span></span> </dl>    | <span data-ttu-id="2a8fd-135">La password dell'account è scaduta.</span><span class="sxs-lookup"><span data-stu-id="2a8fd-135">The account password has expired.</span></span><br/>                                                                                                                                           |
| <dl> <span data-ttu-id="2a8fd-136"><dt>\_account stato \_ bloccato \_</dt></span><span class="sxs-lookup"><span data-stu-id="2a8fd-136"><dt>STATUS\_ACCOUNT\_LOCKED\_OUT</dt></span></span> </dl> | <span data-ttu-id="2a8fd-137">L'account è stato bloccato.</span><span class="sxs-lookup"><span data-stu-id="2a8fd-137">The account has been locked out.</span></span> <br/>                                                                                                                                           |
| <dl> <span data-ttu-id="2a8fd-138"><dt>Altro</dt></span><span class="sxs-lookup"><span data-stu-id="2a8fd-138"><dt>Others</dt></span></span> </dl>                       | <span data-ttu-id="2a8fd-139">Altri codici di errore specifici del provider.</span><span class="sxs-lookup"><span data-stu-id="2a8fd-139">Other provider-specific error codes.</span></span> <br/>                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="2a8fd-140">Commenti</span><span class="sxs-lookup"><span data-stu-id="2a8fd-140">Remarks</span></span>

<span data-ttu-id="2a8fd-141">Prima di recuperare il certificato dal cloud, il provider di identità deve verificare la presenza di un certificato valido per l'utente nell'archivio certificati "MY" dell'utente.</span><span class="sxs-lookup"><span data-stu-id="2a8fd-141">Before fetching the certificate from the cloud, the identity provider should check that there is a valid certificate for this user in the user's "MY" certificate store.</span></span> <span data-ttu-id="2a8fd-142">Se esiste un certificato valido, il provider deve restituire questo certificato per evitare il traffico di rete superfluo.</span><span class="sxs-lookup"><span data-stu-id="2a8fd-142">If a valid certificate exists, the provider should return this certificate to avoid unnecessary network traffic.</span></span>

<span data-ttu-id="2a8fd-143">Il provider di identità può inoltre memorizzare nella cache il certificato localmente, purché sia protetto dall'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="2a8fd-143">The identity provider can also cache the certificate locally as long as it is protected from the current user.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a8fd-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2a8fd-144">Requirements</span></span>



| <span data-ttu-id="2a8fd-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a8fd-145">Requirement</span></span> | <span data-ttu-id="2a8fd-146">Valore</span><span class="sxs-lookup"><span data-stu-id="2a8fd-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2a8fd-147">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a8fd-147">Minimum supported client</span></span><br/> | <span data-ttu-id="2a8fd-148">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="2a8fd-148">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2a8fd-149">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a8fd-149">Minimum supported server</span></span><br/> | <span data-ttu-id="2a8fd-150">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="2a8fd-150">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="2a8fd-151">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2a8fd-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a8fd-152"><dt>Lsaidprov. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a8fd-152"><dt>Lsaidprov.h</dt></span></span> </dl> |



 

