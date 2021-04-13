---
description: Ottiene un handle per un provider del servizio di crittografia (CSP) e una specifica della chiave per un contesto del certificato.
ms.assetid: ff72231f-e10f-49d2-b0e0-0008923803cc
title: GetCryptProvFromCert (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCryptProvFromCert
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: bcd396c45333dee42bae4cb8bdfdd52792f1bdd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350126"
---
# <a name="getcryptprovfromcert-function"></a><span data-ttu-id="b5ef4-103">GetCryptProvFromCert (funzione)</span><span class="sxs-lookup"><span data-stu-id="b5ef4-103">GetCryptProvFromCert function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b5ef4-104">Questa API è deprecata.</span><span class="sxs-lookup"><span data-stu-id="b5ef4-104">This API is deprecated.</span></span> <span data-ttu-id="b5ef4-105">Microsoft può rimuovere questa API nelle versioni future.</span><span class="sxs-lookup"><span data-stu-id="b5ef4-105">Microsoft may remove this API in future releases.</span></span>

 

<span data-ttu-id="b5ef4-106">La funzione **GetCryptProvFromCert** ottiene un handle per un [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) e una specifica della chiave per un contesto del [*certificato*](../secgloss/c-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="b5ef4-106">The **GetCryptProvFromCert** function gets a handle to a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and a key specification for a [*certificate*](../secgloss/c-gly.md) context.</span></span> <span data-ttu-id="b5ef4-107">Usare questa funzione per ottenere l'accesso alla [*chiave privata*](../secgloss/p-gly.md) dell'autorità emittente del certificato.</span><span class="sxs-lookup"><span data-stu-id="b5ef4-107">Use this function to get access to the [*private key*](../secgloss/p-gly.md) of the certificate issuer.</span></span>

> [!Note]  
> <span data-ttu-id="b5ef4-108">A questa funzione non è associato alcun file di intestazione o libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="b5ef4-108">This function has no associated header file or import library.</span></span> <span data-ttu-id="b5ef4-109">Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e utilizzare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="b5ef4-109">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="b5ef4-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b5ef4-110">Syntax</span></span>


```C++
BOOL WINAPI GetCryptProvFromCert(
  _In_      HWND           hwnd,
  _In_      PCCERT_CONTEXT pCert,
  _Out_     HCRYPTPROV     *phCryptProv,
  _Out_     DWORD          *pdwKeySpec,
  _In_      BOOL           *pfDidCryptAcquire,
  _Out_opt_ LPWSTR         *ppwszTmpContainer,
  _Out_opt_ LPWSTR         *ppwszProviderName,
  _Out_     DWORD          *pdwProviderType
);
```



## <a name="parameters"></a><span data-ttu-id="b5ef4-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="b5ef4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5ef4-112">*HWND* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5ef4-112">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5ef4-113">Handle della finestra da utilizzare come proprietario di tutte le finestre di dialogo visualizzate.</span><span class="sxs-lookup"><span data-stu-id="b5ef4-113">The handle of the window to use as the owner of any dialog boxes that are displayed.</span></span> <span data-ttu-id="b5ef4-114">Questo membro non è attualmente in uso e viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="b5ef4-114">This member is not currently used and is ignored.</span></span> <span data-ttu-id="b5ef4-115">È possibile passare il **valore null** per questo parametro.</span><span class="sxs-lookup"><span data-stu-id="b5ef4-115">It is safe to pass **NULL** for this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="b5ef4-116">*pCert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5ef4-116">*pCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5ef4-117">Puntatore a una struttura [**del \_ contesto**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) del certificato per il certificato.</span><span class="sxs-lookup"><span data-stu-id="b5ef4-117">A pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) structure for the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="b5ef4-118">*phCryptProv* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b5ef4-118">*phCryptProv* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5ef4-119">Puntatore a una struttura [**HCRYPTPROV**](hcryptprov.md) che rappresenta un handle per il CSP.</span><span class="sxs-lookup"><span data-stu-id="b5ef4-119">A pointer to an [**HCRYPTPROV**](hcryptprov.md) structure that is a handle to the CSP.</span></span>

</dd> <dt>

<span data-ttu-id="b5ef4-120">*pdwKeySpec* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b5ef4-120">*pdwKeySpec* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5ef4-121">Specifica della chiave privata da recuperare.</span><span class="sxs-lookup"><span data-stu-id="b5ef4-121">The specification of the private key to retrieve.</span></span> <span data-ttu-id="b5ef4-122">I valori possibili sono **in fase di \_ scambio** o **di \_ firma**.</span><span class="sxs-lookup"><span data-stu-id="b5ef4-122">Possible values include **AT\_KEYEXCHANGE** or **AT\_SIGNATURE**.</span></span>

</dd> <dt>

<span data-ttu-id="b5ef4-123">*pfDidCryptAcquire* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5ef4-123">*pfDidCryptAcquire* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5ef4-124">Valore che specifica se la funzione ha acquisito l'handle del provider in base al certificato.</span><span class="sxs-lookup"><span data-stu-id="b5ef4-124">A value that specifies whether the function acquired the provider handle based on the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="b5ef4-125">*ppwszTmpContainer* \[ out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="b5ef4-125">*ppwszTmpContainer* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b5ef4-126">Indirizzo di un puntatore a una stringa con terminazione null per il nome del contenitore di chiavi temporaneo.</span><span class="sxs-lookup"><span data-stu-id="b5ef4-126">The address of a pointer to a null-terminated string for the temporary key container name.</span></span> <span data-ttu-id="b5ef4-127">La funzione **GetCryptProvFromCert** fornisce e inizializza il contenitore temporaneo.</span><span class="sxs-lookup"><span data-stu-id="b5ef4-127">The **GetCryptProvFromCert** function provides and initializes the temporary container.</span></span> <span data-ttu-id="b5ef4-128">Quando si chiama **GetCryptProvFromCert**, l'indirizzo deve puntare a un valore **null** .</span><span class="sxs-lookup"><span data-stu-id="b5ef4-128">When calling **GetCryptProvFromCert**, the address should point to a **NULL** value.</span></span>

</dd> <dt>

<span data-ttu-id="b5ef4-129">*ppwszProviderName* \[ out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="b5ef4-129">*ppwszProviderName* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b5ef4-130">Indirizzo di un puntatore a una stringa con terminazione null per il nome del provider.</span><span class="sxs-lookup"><span data-stu-id="b5ef4-130">The address of a pointer to a null-terminated string for the provider name.</span></span> <span data-ttu-id="b5ef4-131">La funzione **GetCryptProvFromCert** restituisce il nome del provider.</span><span class="sxs-lookup"><span data-stu-id="b5ef4-131">The **GetCryptProvFromCert** function returns the provider name.</span></span> <span data-ttu-id="b5ef4-132">Quando si chiama **GetCryptProvFromCert**, l'indirizzo deve puntare a un valore **null** .</span><span class="sxs-lookup"><span data-stu-id="b5ef4-132">When calling **GetCryptProvFromCert**, the address should point to a **NULL** value.</span></span>

</dd> <dt>

<span data-ttu-id="b5ef4-133">*pdwProviderType* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b5ef4-133">*pdwProviderType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5ef4-134">Specifica il tipo CSP.</span><span class="sxs-lookup"><span data-stu-id="b5ef4-134">Specifies the CSP type.</span></span> <span data-ttu-id="b5ef4-135">Può essere zero o uno dei tipi di [provider di crittografia](cryptographic-provider-types.md).</span><span class="sxs-lookup"><span data-stu-id="b5ef4-135">This can be zero or one of the [Cryptographic Provider Types](cryptographic-provider-types.md).</span></span> <span data-ttu-id="b5ef4-136">Se questo membro è zero, il contenitore di chiavi è uno dei provider di archiviazione delle chiavi CNG.</span><span class="sxs-lookup"><span data-stu-id="b5ef4-136">If this member is zero, the key container is one of the CNG key storage providers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5ef4-137">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b5ef4-137">Return value</span></span>

<span data-ttu-id="b5ef4-138">Al termine dell'operazione, la funzione restituisce **true**.</span><span class="sxs-lookup"><span data-stu-id="b5ef4-138">Upon success, this function returns **TRUE**.</span></span> <span data-ttu-id="b5ef4-139">Se l'operazione ha esito negativo, la funzione **GetCryptProvFromCert** restituisce **false** .</span><span class="sxs-lookup"><span data-stu-id="b5ef4-139">The **GetCryptProvFromCert** function returns **FALSE** if it fails.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5ef4-140">Commenti</span><span class="sxs-lookup"><span data-stu-id="b5ef4-140">Remarks</span></span>

<span data-ttu-id="b5ef4-141">Lo strumento [Makecert](makecert.md) chiama **GetCryptProvFromCert** quando viene richiamato usando l'opzione della riga di comando **-is** .</span><span class="sxs-lookup"><span data-stu-id="b5ef4-141">The [MakeCert](makecert.md) tool calls **GetCryptProvFromCert** when you invoke it by using the **-is** command line option.</span></span>

<span data-ttu-id="b5ef4-142">Se il parametro *pfDidCryptAcquire* è impostato su **true**, la funzione imposta i parametri *phCryptProv*, *pdwKeySpec* e *pdwProviderType* sui valori del provider.</span><span class="sxs-lookup"><span data-stu-id="b5ef4-142">If the *pfDidCryptAcquire* parameter is set to **TRUE**, the function sets *phCryptProv*, *pdwKeySpec*, and *pdwProviderType* parameters to the provider values.</span></span>

<span data-ttu-id="b5ef4-143">Al termine dell'utilizzo del CSP, liberarlo chiamando la funzione [**FreeCryptProvFromCert**](freecryptprovfromcert.md) .</span><span class="sxs-lookup"><span data-stu-id="b5ef4-143">When you have finished using the CSP, free it by calling the [**FreeCryptProvFromCert**](freecryptprovfromcert.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5ef4-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b5ef4-144">Requirements</span></span>



| <span data-ttu-id="b5ef4-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5ef4-145">Requirement</span></span> | <span data-ttu-id="b5ef4-146">Valore</span><span class="sxs-lookup"><span data-stu-id="b5ef4-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5ef4-147">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b5ef4-147">Minimum supported client</span></span><br/> | <span data-ttu-id="b5ef4-148">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b5ef4-148">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b5ef4-149">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b5ef4-149">Minimum supported server</span></span><br/> | <span data-ttu-id="b5ef4-150">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b5ef4-150">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b5ef4-151">DLL</span><span class="sxs-lookup"><span data-stu-id="b5ef4-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5ef4-152"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5ef4-152"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
