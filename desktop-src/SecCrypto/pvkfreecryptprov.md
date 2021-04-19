---
description: Rilascia l'handle a un provider del servizio di crittografia (CSP) ed eventualmente elimina il contenitore temporaneo creato dalla funzione PvkGetCryptProv.
ms.assetid: e7dcb5c5-dd80-4810-bf1f-4b7b921fa22c
title: PvkFreeCryptProv (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PvkFreeCryptProv
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 70ff29c968fe8f50c813f1da71b2e73a112f25f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317709"
---
# <a name="pvkfreecryptprov-function"></a><span data-ttu-id="2f4d6-103">PvkFreeCryptProv (funzione)</span><span class="sxs-lookup"><span data-stu-id="2f4d6-103">PvkFreeCryptProv function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2f4d6-104">Questa API è deprecata.</span><span class="sxs-lookup"><span data-stu-id="2f4d6-104">This API is deprecated.</span></span> <span data-ttu-id="2f4d6-105">Microsoft può rimuovere questa API nelle versioni future.</span><span class="sxs-lookup"><span data-stu-id="2f4d6-105">Microsoft may remove this API in future releases.</span></span>

 

<span data-ttu-id="2f4d6-106">La funzione **PvkFreeCryptProv** rilascia l'handle a un [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) ed eventualmente elimina il contenitore temporaneo creato dalla funzione [**PvkGetCryptProv**](pvkgetcryptprov.md) .</span><span class="sxs-lookup"><span data-stu-id="2f4d6-106">The **PvkFreeCryptProv** function releases the handle to a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and optionally deletes the temporary container created by the [**PvkGetCryptProv**](pvkgetcryptprov.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="2f4d6-107">A questa funzione non è associato alcun file di intestazione o libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="2f4d6-107">This function has no associated header file or import library.</span></span> <span data-ttu-id="2f4d6-108">Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e utilizzare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="2f4d6-108">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="2f4d6-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2f4d6-109">Syntax</span></span>


```C++
void WINAPI PvkFreeCryptProv(
  _In_     HCRYPTPROV hProv,
  _In_     LPCWSTR    pwszCapiProvider,
  _In_     DWORD      dwProviderType,
  _In_opt_ LPWSTR     pwszTmpContainer
);
```



## <a name="parameters"></a><span data-ttu-id="2f4d6-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="2f4d6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f4d6-111">*hProv* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f4d6-111">*hProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f4d6-112">Handle per il CSP.</span><span class="sxs-lookup"><span data-stu-id="2f4d6-112">A handle to the CSP.</span></span>

</dd> <dt>

<span data-ttu-id="2f4d6-113">*pwszCapiProvider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f4d6-113">*pwszCapiProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f4d6-114">Puntatore a una stringa con terminazione null per il nome CSP.</span><span class="sxs-lookup"><span data-stu-id="2f4d6-114">A pointer to a null-terminated string for the CSP name.</span></span>

</dd> <dt>

<span data-ttu-id="2f4d6-115">*dwProviderType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f4d6-115">*dwProviderType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f4d6-116">Valore **DWORD** che rappresenta il tipo di provider di crittografia.</span><span class="sxs-lookup"><span data-stu-id="2f4d6-116">A **DWORD** value that represents the cryptographic provider type.</span></span> <span data-ttu-id="2f4d6-117">Per ulteriori informazioni, vedere [tipi di provider di crittografia](cryptographic-provider-types.md).</span><span class="sxs-lookup"><span data-stu-id="2f4d6-117">For more information, see [Cryptographic Provider Types](cryptographic-provider-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f4d6-118">*pwszTmpContainer* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="2f4d6-118">*pwszTmpContainer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2f4d6-119">Puntatore a una stringa con terminazione null per il nome del contenitore di chiavi temporaneo.</span><span class="sxs-lookup"><span data-stu-id="2f4d6-119">A pointer to a null-terminated string for the temporary key container name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f4d6-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2f4d6-120">Return value</span></span>

<span data-ttu-id="2f4d6-121">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="2f4d6-121">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f4d6-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2f4d6-122">Requirements</span></span>



| <span data-ttu-id="2f4d6-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f4d6-123">Requirement</span></span> | <span data-ttu-id="2f4d6-124">Valore</span><span class="sxs-lookup"><span data-stu-id="2f4d6-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f4d6-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f4d6-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2f4d6-126">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2f4d6-126">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2f4d6-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f4d6-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2f4d6-128">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2f4d6-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2f4d6-129">DLL</span><span class="sxs-lookup"><span data-stu-id="2f4d6-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f4d6-130"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f4d6-130"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
