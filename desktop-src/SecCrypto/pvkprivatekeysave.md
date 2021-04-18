---
description: Salva una chiave privata e la relativa chiave pubblica corrispondente in un file specificato.
ms.assetid: 491a128a-b4aa-4cca-a835-d0e8d7df6720
title: PvkPrivateKeySave (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PvkPrivateKeySave
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: ef60c3f615a704248fbcb8630322fa6b598141ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315368"
---
# <a name="pvkprivatekeysave-function"></a><span data-ttu-id="db408-103">PvkPrivateKeySave (funzione)</span><span class="sxs-lookup"><span data-stu-id="db408-103">PvkPrivateKeySave function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="db408-104">Questa API è deprecata.</span><span class="sxs-lookup"><span data-stu-id="db408-104">This API is deprecated.</span></span> <span data-ttu-id="db408-105">Microsoft può rimuovere questa API nelle versioni future.</span><span class="sxs-lookup"><span data-stu-id="db408-105">Microsoft may remove this API in future releases.</span></span>

 

<span data-ttu-id="db408-106">La funzione **PvkPrivateKeySave** salva una [*chiave privata*](../secgloss/p-gly.md) e la [*chiave pubblica*](../secgloss/p-gly.md) corrispondente in un file specificato.</span><span class="sxs-lookup"><span data-stu-id="db408-106">The **PvkPrivateKeySave** function saves a [*private key*](../secgloss/p-gly.md) and its corresponding [*public key*](../secgloss/p-gly.md) to a specified file.</span></span>

> [!Note]  
> <span data-ttu-id="db408-107">A questa funzione non è associato alcun file di intestazione o libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="db408-107">This function has no associated header file or import library.</span></span> <span data-ttu-id="db408-108">Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e utilizzare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="db408-108">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="db408-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="db408-109">Syntax</span></span>


```C++
BOOL WINAPI PvkPrivateKeySave(
  _In_ HCRYPTPROV hCryptProv,
  _In_ HANDLE     hFile,
  _In_ DWORD      dwKeySpec,
  _In_ HWND       hwndOwner,
  _In_ LPCWSTR    pwszKeyName,
  _In_ DWORD      dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="db408-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="db408-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db408-111">*hCryptProv* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="db408-111">*hCryptProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db408-112">Handle per un [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP).</span><span class="sxs-lookup"><span data-stu-id="db408-112">A handle to a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

</dd> <dt>

<span data-ttu-id="db408-113">*hFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="db408-113">*hFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db408-114">Handle per un file creato con l'autorizzazione di lettura/scrittura iniziale e l'autorizzazione di sola lettura successiva.</span><span class="sxs-lookup"><span data-stu-id="db408-114">A handle to a file created with initial read/write permission and subsequent read-only permission.</span></span>

</dd> <dt>

<span data-ttu-id="db408-115">*dwKeySpec* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="db408-115">*dwKeySpec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db408-116">Valore long integer per il tipo di chiave.</span><span class="sxs-lookup"><span data-stu-id="db408-116">A long integer for the type of key.</span></span> <span data-ttu-id="db408-117">I valori possibili sono **in fase di \_ scambio** o **di \_ firma**.</span><span class="sxs-lookup"><span data-stu-id="db408-117">Possible values include **AT\_KEYEXCHANGE** or **AT\_SIGNATURE**.</span></span>

</dd> <dt>

<span data-ttu-id="db408-118">*hwndOwner* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="db408-118">*hwndOwner* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db408-119">Se è necessaria una password per crittografare la chiave privata, questo parametro è un handle per l'elemento padre della finestra di dialogo; in caso contrario, è **null**.</span><span class="sxs-lookup"><span data-stu-id="db408-119">If a password is required to encrypt the private key, this parameter is a handle to the parent of the dialog box; otherwise, it is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="db408-120">*pwszKeyName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="db408-120">*pwszKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db408-121">Puntatore a una stringa con terminazione null per il nome della chiave da salvare.</span><span class="sxs-lookup"><span data-stu-id="db408-121">A pointer to a null-terminated string for the name of the key to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="db408-122">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="db408-122">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db408-123">Valore **DWORD** che specifica opzioni aggiuntive per la funzione.</span><span class="sxs-lookup"><span data-stu-id="db408-123">A **DWORD** value that specifies additional options for the function.</span></span> <span data-ttu-id="db408-124">Per ulteriori informazioni, vedere il parametro *dwFlags* in [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey).</span><span class="sxs-lookup"><span data-stu-id="db408-124">For more information, see the *dwFlags* parameter in [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db408-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="db408-125">Return value</span></span>

<span data-ttu-id="db408-126">Al termine dell'operazione, la funzione restituisce **true**.</span><span class="sxs-lookup"><span data-stu-id="db408-126">Upon success, this function returns **TRUE**.</span></span> <span data-ttu-id="db408-127">Se l'operazione ha esito negativo, la funzione **PvkPrivateKeySave** restituisce **false** .</span><span class="sxs-lookup"><span data-stu-id="db408-127">The **PvkPrivateKeySave** function returns **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="db408-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="db408-128">Requirements</span></span>



| <span data-ttu-id="db408-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="db408-129">Requirement</span></span> | <span data-ttu-id="db408-130">Valore</span><span class="sxs-lookup"><span data-stu-id="db408-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="db408-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="db408-131">Minimum supported client</span></span><br/> | <span data-ttu-id="db408-132">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="db408-132">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="db408-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="db408-133">Minimum supported server</span></span><br/> | <span data-ttu-id="db408-134">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="db408-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="db408-135">DLL</span><span class="sxs-lookup"><span data-stu-id="db408-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db408-136"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db408-136"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
