---
description: Consente di creare un contenitore temporaneo nel provider del servizio di crittografia (CSP) e di caricare una chiave privata dalla memoria nel contenitore.
ms.assetid: 9388b49b-fad4-4499-a391-fe58ed672552
title: PvkPrivateKeyAcquireContextFromMemory (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PvkPrivateKeyAcquireContextFromMemory
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 1552d1e35845ffb7407d11d6e520b914ab805d50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348486"
---
# <a name="pvkprivatekeyacquirecontextfrommemory-function"></a><span data-ttu-id="dd9dc-103">PvkPrivateKeyAcquireContextFromMemory (funzione)</span><span class="sxs-lookup"><span data-stu-id="dd9dc-103">PvkPrivateKeyAcquireContextFromMemory function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dd9dc-104">Questa API è deprecata.</span><span class="sxs-lookup"><span data-stu-id="dd9dc-104">This API is deprecated.</span></span> <span data-ttu-id="dd9dc-105">Microsoft può rimuovere questa API nelle versioni future.</span><span class="sxs-lookup"><span data-stu-id="dd9dc-105">Microsoft may remove this API in future releases.</span></span>

 

<span data-ttu-id="dd9dc-106">La funzione **PvkPrivateKeyAcquireContextFromMemory** crea un contenitore temporaneo nel [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) e carica una [*chiave privata*](../secgloss/p-gly.md) dalla memoria nel contenitore.</span><span class="sxs-lookup"><span data-stu-id="dd9dc-106">The **PvkPrivateKeyAcquireContextFromMemory** function creates a temporary container in the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and loads a [*private key*](../secgloss/p-gly.md) from memory into the container.</span></span>

> [!Note]  
> <span data-ttu-id="dd9dc-107">A questa funzione non è associato alcun file di intestazione o libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="dd9dc-107">This function has no associated header file or import library.</span></span> <span data-ttu-id="dd9dc-108">Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e utilizzare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="dd9dc-108">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="dd9dc-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dd9dc-109">Syntax</span></span>


```C++
BOOL WINAPI PvkPrivateKeyAcquireContextFromMemory(
  _In_        LPCWSTR    pwszProvName,
  _In_        DWORD      dwProvType,
  _In_        BYTE       *pbData,
  _In_        DWORD      cbData,
  _In_        HWND       hwndOwner,
  _In_        LPCWSTR    pwszKeyName,
  _Inout_opt_ DWORD      *pdwKeySpec,
  _Out_       HCRYPTPROV *phCryptProv,
  _Out_       LPTSTR     *ppwszTmpContainer
);
```



## <a name="parameters"></a><span data-ttu-id="dd9dc-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="dd9dc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd9dc-111">*pwszProvName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dd9dc-111">*pwszProvName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd9dc-112">Puntatore a una stringa con terminazione null che contiene il nome del CSP il cui tipo è richiesto in *dwProvType*.</span><span class="sxs-lookup"><span data-stu-id="dd9dc-112">A pointer to a null-terminated string that contains the name of the CSP whose type is requested in *dwProvType*.</span></span>

</dd> <dt>

<span data-ttu-id="dd9dc-113">*dwProvType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dd9dc-113">*dwProvType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd9dc-114">Valore **DWORD** per il tipo CSP.</span><span class="sxs-lookup"><span data-stu-id="dd9dc-114">A **DWORD** value for the CSP type.</span></span> <span data-ttu-id="dd9dc-115">Per ulteriori informazioni sui tipi CSP, vedere [tipi di provider di crittografia](cryptographic-provider-types.md).</span><span class="sxs-lookup"><span data-stu-id="dd9dc-115">For more information about CSP types, see [Cryptographic Provider Types](cryptographic-provider-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd9dc-116">*pbData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dd9dc-116">*pbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd9dc-117">Puntatore a un buffer per ricevere i dati di contesto.</span><span class="sxs-lookup"><span data-stu-id="dd9dc-117">A pointer to a buffer to receive the context data.</span></span> <span data-ttu-id="dd9dc-118">Il chiamante deve fornire questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="dd9dc-118">The caller must provide this resource.</span></span>

</dd> <dt>

<span data-ttu-id="dd9dc-119">*cbData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dd9dc-119">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd9dc-120">Valore **DWORD** che specifica la dimensione, in byte, del buffer *pbData* .</span><span class="sxs-lookup"><span data-stu-id="dd9dc-120">A **DWORD** value that specifies the size, in bytes, of the *pbData* buffer.</span></span> <span data-ttu-id="dd9dc-121">Il chiamante deve fornire questo valore.</span><span class="sxs-lookup"><span data-stu-id="dd9dc-121">The caller must provide this value.</span></span>

</dd> <dt>

<span data-ttu-id="dd9dc-122">*hwndOwner* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dd9dc-122">*hwndOwner* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd9dc-123">Se è necessaria una password per decrittografare i dati di contesto a cui punta il parametro *pbData* , questo parametro è un handle per l'elemento padre della finestra di dialogo. in caso contrario, è **null**.</span><span class="sxs-lookup"><span data-stu-id="dd9dc-123">If a password is required to decrypt the context data pointed to by the *pbData* parameter, this parameter is a handle to the parent of the dialog box; otherwise, it is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="dd9dc-124">*pwszKeyName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dd9dc-124">*pwszKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd9dc-125">Puntatore a una stringa con terminazione null che contiene il nome della chiave da recuperare.</span><span class="sxs-lookup"><span data-stu-id="dd9dc-125">A pointer to a null-terminated string that contains the name of the key to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="dd9dc-126">*pdwKeySpec* \[ in, out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="dd9dc-126">*pdwKeySpec* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dd9dc-127">Puntatore a un valore **DWORD** che specifica il tipo di chiave.</span><span class="sxs-lookup"><span data-stu-id="dd9dc-127">A pointer to a **DWORD** value that specifies the type of key.</span></span> <span data-ttu-id="dd9dc-128">I valori possibili sono **in fase di \_ scambio** o **di \_ firma**.</span><span class="sxs-lookup"><span data-stu-id="dd9dc-128">Possible values include **AT\_KEYEXCHANGE** or **AT\_SIGNATURE**.</span></span>

</dd> <dt>

<span data-ttu-id="dd9dc-129">*phCryptProv* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="dd9dc-129">*phCryptProv* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dd9dc-130">Puntatore a un handle per il CSP.</span><span class="sxs-lookup"><span data-stu-id="dd9dc-130">A pointer to a handle for the CSP.</span></span>

</dd> <dt>

<span data-ttu-id="dd9dc-131">*ppwszTmpContainer* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="dd9dc-131">*ppwszTmpContainer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dd9dc-132">Indirizzo di un puntatore a una stringa con terminazione null per il nome del contenitore temporaneo.</span><span class="sxs-lookup"><span data-stu-id="dd9dc-132">The address of a pointer to a null-terminated string for the temporary container name.</span></span> <span data-ttu-id="dd9dc-133">La funzione **PvkPrivateKeyAcquireContextFromMemory** fornisce il buffer per questa stringa e lo inizializza.</span><span class="sxs-lookup"><span data-stu-id="dd9dc-133">The **PvkPrivateKeyAcquireContextFromMemory** function provides the buffer for this string and initializes it.</span></span> <span data-ttu-id="dd9dc-134">Quando si chiama **PvkPrivateKeyAcquireContextFromMemory**, l'indirizzo deve puntare a un valore **null** .</span><span class="sxs-lookup"><span data-stu-id="dd9dc-134">When calling **PvkPrivateKeyAcquireContextFromMemory**, the address should point to a **NULL** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd9dc-135">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dd9dc-135">Return value</span></span>

<span data-ttu-id="dd9dc-136">Al termine dell'operazione, la funzione restituisce **true**.</span><span class="sxs-lookup"><span data-stu-id="dd9dc-136">Upon success, this function returns **TRUE**.</span></span> <span data-ttu-id="dd9dc-137">Se l'operazione ha esito negativo, la funzione **PvkPrivateKeyAcquireContextFromMemory** restituisce **false** .</span><span class="sxs-lookup"><span data-stu-id="dd9dc-137">The **PvkPrivateKeyAcquireContextFromMemory** function returns **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd9dc-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dd9dc-138">Requirements</span></span>



| <span data-ttu-id="dd9dc-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd9dc-139">Requirement</span></span> | <span data-ttu-id="dd9dc-140">Valore</span><span class="sxs-lookup"><span data-stu-id="dd9dc-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd9dc-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dd9dc-141">Minimum supported client</span></span><br/> | <span data-ttu-id="dd9dc-142">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="dd9dc-142">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="dd9dc-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dd9dc-143">Minimum supported server</span></span><br/> | <span data-ttu-id="dd9dc-144">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="dd9dc-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="dd9dc-145">DLL</span><span class="sxs-lookup"><span data-stu-id="dd9dc-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd9dc-146"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd9dc-146"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
