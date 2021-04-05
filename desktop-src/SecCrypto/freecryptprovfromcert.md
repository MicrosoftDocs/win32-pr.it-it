---
description: Rilascia l'handle a un provider del servizio di crittografia (CSP) ed eventualmente elimina il contenitore temporaneo creato dalla funzione GetCryptProvFromCert.
ms.assetid: 4462eef2-7056-4e48-aa96-c46f29b701d6
title: FreeCryptProvFromCert (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreeCryptProvFromCert
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 8201de475a4224aea58267405ccde244e56d59f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884066"
---
# <a name="freecryptprovfromcert-function"></a><span data-ttu-id="c1e51-103">FreeCryptProvFromCert (funzione)</span><span class="sxs-lookup"><span data-stu-id="c1e51-103">FreeCryptProvFromCert function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c1e51-104">Questa API è deprecata.</span><span class="sxs-lookup"><span data-stu-id="c1e51-104">This API is deprecated.</span></span> <span data-ttu-id="c1e51-105">Microsoft può rimuovere questa API nelle versioni future.</span><span class="sxs-lookup"><span data-stu-id="c1e51-105">Microsoft may remove this API in future releases.</span></span>

 

<span data-ttu-id="c1e51-106">La funzione **FreeCryptProvFromCert** rilascia l'handle a un [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) ed eventualmente elimina il contenitore temporaneo creato dalla funzione [**GetCryptProvFromCert**](getcryptprovfromcert.md) .</span><span class="sxs-lookup"><span data-stu-id="c1e51-106">The **FreeCryptProvFromCert** function releases the handle to a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and optionally deletes the temporary container created by the [**GetCryptProvFromCert**](getcryptprovfromcert.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="c1e51-107">A questa funzione non è associato alcun file di intestazione o libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="c1e51-107">This function has no associated header file or import library.</span></span> <span data-ttu-id="c1e51-108">Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e utilizzare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="c1e51-108">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="c1e51-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c1e51-109">Syntax</span></span>


```C++
void WINAPI FreeCryptProvFromCert(
  _In_     BOOL       fAcquired,
  _In_     HCRYPTPROV hProv,
  _In_opt_ LPWSTR     pwszCapiProvider,
  _In_     DWORD      dwProviderType,
  _In_opt_ LPWSTR     pwszTmpContainer
);
```



## <a name="parameters"></a><span data-ttu-id="c1e51-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="c1e51-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1e51-111">*fAcquired* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c1e51-111">*fAcquired* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1e51-112">Valore che specifica se l'handle del provider è stato acquisito dal [*certificato*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="c1e51-112">A value that specifies whether the provider handle was acquired from the [*certificate*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1e51-113">*hProv* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c1e51-113">*hProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1e51-114">Puntatore a una struttura [**HCRYPTPROV**](hcryptprov.md) per il CSP.</span><span class="sxs-lookup"><span data-stu-id="c1e51-114">A pointer to an [**HCRYPTPROV**](hcryptprov.md) structure for the CSP.</span></span>

</dd> <dt>

<span data-ttu-id="c1e51-115">*pwszCapiProvider* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="c1e51-115">*pwszCapiProvider* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c1e51-116">Puntatore a una stringa con terminazione null per il nome del provider.</span><span class="sxs-lookup"><span data-stu-id="c1e51-116">A pointer to a null-terminated string for the provider name.</span></span>

</dd> <dt>

<span data-ttu-id="c1e51-117">*dwProviderType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c1e51-117">*dwProviderType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1e51-118">Specifica il tipo CSP.</span><span class="sxs-lookup"><span data-stu-id="c1e51-118">Specifies the CSP type.</span></span> <span data-ttu-id="c1e51-119">Può essere zero o uno dei tipi di [provider di crittografia](cryptographic-provider-types.md).</span><span class="sxs-lookup"><span data-stu-id="c1e51-119">This can be zero or one of the [Cryptographic Provider Types](cryptographic-provider-types.md).</span></span> <span data-ttu-id="c1e51-120">Se questo membro è zero, il contenitore di chiavi è uno dei provider di archiviazione delle chiavi CNG.</span><span class="sxs-lookup"><span data-stu-id="c1e51-120">If this member is zero, the key container is one of the CNG key storage providers.</span></span>

</dd> <dt>

<span data-ttu-id="c1e51-121">*pwszTmpContainer* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="c1e51-121">*pwszTmpContainer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c1e51-122">Puntatore a una stringa con terminazione null per il nome del contenitore di chiavi temporaneo.</span><span class="sxs-lookup"><span data-stu-id="c1e51-122">A pointer to a null-terminated string for the name of the temporary key container.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1e51-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c1e51-123">Return value</span></span>

<span data-ttu-id="c1e51-124">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="c1e51-124">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1e51-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c1e51-125">Requirements</span></span>



| <span data-ttu-id="c1e51-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1e51-126">Requirement</span></span> | <span data-ttu-id="c1e51-127">Valore</span><span class="sxs-lookup"><span data-stu-id="c1e51-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1e51-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1e51-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c1e51-129">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c1e51-129">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c1e51-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1e51-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c1e51-131">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c1e51-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c1e51-132">DLL</span><span class="sxs-lookup"><span data-stu-id="c1e51-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1e51-133"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1e51-133"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
