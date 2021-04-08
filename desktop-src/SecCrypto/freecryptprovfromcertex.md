---
description: "Rilascia l'handle a un provider del servizio di crittografia (CSP) o a una chiave Cryptography API: Next Generation (CNG)."
ms.assetid: 76cbf8ae-c4ab-43d9-b06d-ea0b2a66368a
title: FreeCryptProvFromCertEx (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreeCryptProvFromCertEx
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 1be6270ebf9320a9c7527736b9fc4894cd50de9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884065"
---
# <a name="freecryptprovfromcertex-function"></a><span data-ttu-id="964ac-103">FreeCryptProvFromCertEx (funzione)</span><span class="sxs-lookup"><span data-stu-id="964ac-103">FreeCryptProvFromCertEx function</span></span>

<span data-ttu-id="964ac-104">La funzione **FreeCryptProvFromCertEx** rilascia l'handle a un [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) o a una chiave Cryptography API: Next Generation (CNG).</span><span class="sxs-lookup"><span data-stu-id="964ac-104">The **FreeCryptProvFromCertEx** function releases the handle either to a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) or to a Cryptography API: Next Generation (CNG) key.</span></span>

> [!Note]  
> <span data-ttu-id="964ac-105">A questa funzione non è associato alcun file di intestazione o libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="964ac-105">This function has no associated header file or import library.</span></span> <span data-ttu-id="964ac-106">Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e utilizzare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="964ac-106">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="964ac-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="964ac-107">Syntax</span></span>


```C++
void WINAPI FreeCryptProvFromCertEx(
  _In_     BOOL                            fAcquired,
  _In_     HCRYPTPROV_OR_NCRYPT_KEY_HANDLE hProv,
           DWORD                           dwKeySpec,
  _In_opt_ LPWSTR                          pwszCapiProvider,
  _In_     DWORD                           dwProviderType,
  _In_opt_ LPWSTR                          pwszTmpContainer
);
```



## <a name="parameters"></a><span data-ttu-id="964ac-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="964ac-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="964ac-109">*fAcquired* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="964ac-109">*fAcquired* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="964ac-110">Valore che specifica se l'handle del provider è stato acquisito dal [*certificato*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="964ac-110">A value that specifies whether the provider handle was acquired from the [*certificate*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="964ac-111">*hProv* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="964ac-111">*hProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="964ac-112">Handle per un CSP di CAPICOM o un handle per una chiave CNG.</span><span class="sxs-lookup"><span data-stu-id="964ac-112">A handle to a CAPICOM CSP or a handle to a CNG key.</span></span>

</dd> <dt>

<span data-ttu-id="964ac-113">*dwKeySpec*</span><span class="sxs-lookup"><span data-stu-id="964ac-113">*dwKeySpec*</span></span> 
</dt> <dd>

<span data-ttu-id="964ac-114">Indirizzo di una variabile **DWORD** che riceve informazioni aggiuntive sulla chiave.</span><span class="sxs-lookup"><span data-stu-id="964ac-114">The address of a **DWORD** variable that receives additional information about the key.</span></span> <span data-ttu-id="964ac-115">Può corrispondere a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="964ac-115">This can be one of the following values.</span></span>



| <span data-ttu-id="964ac-116">Valore</span><span class="sxs-lookup"><span data-stu-id="964ac-116">Value</span></span>                                                                                                                                                                                | <span data-ttu-id="964ac-117">Significato</span><span class="sxs-lookup"><span data-stu-id="964ac-117">Meaning</span></span>                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| <span id="AT_KEYEXCHANGE"></span><span id="at_keyexchange"></span><dl> <span data-ttu-id="964ac-118"><dt>**in \_ scambio di valute**</dt></span><span class="sxs-lookup"><span data-stu-id="964ac-118"><dt>**AT\_KEYEXCHANGE**</dt></span></span> </dl>                     | <span data-ttu-id="964ac-119">La coppia di chiavi è una coppia di scambio di chiavi.</span><span class="sxs-lookup"><span data-stu-id="964ac-119">The key pair is a key exchange pair.</span></span><br/>                                                                  |
| <span id="AT_SIGNATURE"></span><span id="at_signature"></span><dl> <span data-ttu-id="964ac-120"><dt>**ALLA \_ firma**</dt></span><span class="sxs-lookup"><span data-stu-id="964ac-120"><dt>**AT\_SIGNATURE**</dt></span></span> </dl>                           | <span data-ttu-id="964ac-121">La coppia di chiavi è una coppia di firme.</span><span class="sxs-lookup"><span data-stu-id="964ac-121">The key pair is a signature pair.</span></span><br/>                                                                     |
| <span id="CERT_NCRYPT_KEY_SPEC"></span><span id="cert_ncrypt_key_spec"></span><dl> <span data-ttu-id="964ac-122"><dt>**\_specifica della \_ chiave CERT NCRYPT \_**</dt></span><span class="sxs-lookup"><span data-stu-id="964ac-122"><dt>**CERT\_NCRYPT\_KEY\_SPEC**</dt></span></span> </dl> | <span data-ttu-id="964ac-123">La chiave è una chiave CNG.</span><span class="sxs-lookup"><span data-stu-id="964ac-123">The key is a CNG key.</span></span><br/> <span data-ttu-id="964ac-124">**Windows Server 2003 e Windows XP:** Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="964ac-124">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="964ac-125">*pwszCapiProvider* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="964ac-125">*pwszCapiProvider* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="964ac-126">Puntatore a una stringa con terminazione null per il nome del provider.</span><span class="sxs-lookup"><span data-stu-id="964ac-126">A pointer to a null-terminated string for the provider name.</span></span>

</dd> <dt>

<span data-ttu-id="964ac-127">*dwProviderType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="964ac-127">*dwProviderType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="964ac-128">Specifica il tipo CSP.</span><span class="sxs-lookup"><span data-stu-id="964ac-128">Specifies the CSP type.</span></span> <span data-ttu-id="964ac-129">Può essere zero o uno dei tipi di [provider di crittografia](cryptographic-provider-types.md).</span><span class="sxs-lookup"><span data-stu-id="964ac-129">This can be zero or one of the [Cryptographic Provider Types](cryptographic-provider-types.md).</span></span> <span data-ttu-id="964ac-130">Se questo membro è zero, il contenitore di chiavi è uno dei provider di archiviazione delle chiavi CNG.</span><span class="sxs-lookup"><span data-stu-id="964ac-130">If this member is zero, the key container is one of the CNG key storage providers.</span></span>

</dd> <dt>

<span data-ttu-id="964ac-131">*pwszTmpContainer* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="964ac-131">*pwszTmpContainer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="964ac-132">Puntatore a una stringa con terminazione null per il nome del contenitore di chiavi temporaneo.</span><span class="sxs-lookup"><span data-stu-id="964ac-132">A pointer to a null-terminated string for the name of the temporary key container.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="964ac-133">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="964ac-133">Return value</span></span>

<span data-ttu-id="964ac-134">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="964ac-134">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="964ac-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="964ac-135">Requirements</span></span>



| <span data-ttu-id="964ac-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="964ac-136">Requirement</span></span> | <span data-ttu-id="964ac-137">Valore</span><span class="sxs-lookup"><span data-stu-id="964ac-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="964ac-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="964ac-138">Minimum supported client</span></span><br/> | <span data-ttu-id="964ac-139">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="964ac-139">Windows 7 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="964ac-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="964ac-140">Minimum supported server</span></span><br/> | <span data-ttu-id="964ac-141">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="964ac-141">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="964ac-142">DLL</span><span class="sxs-lookup"><span data-stu-id="964ac-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="964ac-143"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="964ac-143"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
