---
description: Ottiene il livello di una regola di identificazione hash che corrisponde all'hash specificato.
ms.assetid: 1592c8da-31c0-45fb-b832-d439dd53c277
title: SaferiSearchMatchingHashRules (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SaferiSearchMatchingHashRules
api_type:
- DllExport
api_location:
- Advapi32.dll
- Ext-MS-Win-AdvAPI32-safer-l1-1-0.dll
ms.openlocfilehash: 2d1b7a2b2ce3f0f0e45d87a46219f3ee4d999bc8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483645"
---
# <a name="saferisearchmatchinghashrules-function"></a><span data-ttu-id="9d5db-103">SaferiSearchMatchingHashRules (funzione)</span><span class="sxs-lookup"><span data-stu-id="9d5db-103">SaferiSearchMatchingHashRules function</span></span>

<span data-ttu-id="9d5db-104">Ottiene il livello di una regola di identificazione hash che corrisponde all'hash specificato.</span><span class="sxs-lookup"><span data-stu-id="9d5db-104">Gets the level of a hash identification rule that matches the specified hash.</span></span>

<span data-ttu-id="9d5db-105">Questa funzione non dispone di librerie di importazione associate e non è dichiarata in un'intestazione pubblica.</span><span class="sxs-lookup"><span data-stu-id="9d5db-105">This function has no associated import library and is not declared in a public header.</span></span> <span data-ttu-id="9d5db-106">È necessario definire un puntatore a funzione con la firma di questa funzione ed è necessario utilizzare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Advapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="9d5db-106">You must define a function pointer with the signature of this function, and you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Advapi32.dll.</span></span>

<span data-ttu-id="9d5db-107">È consigliabile usare la funzione [**SaferIdentifyLevel**](/windows/win32/api/winsafer/nf-winsafer-saferidentifylevel) per valutare i criteri di restrizione software.</span><span class="sxs-lookup"><span data-stu-id="9d5db-107">We recommend using the [**SaferIdentifyLevel**](/windows/win32/api/winsafer/nf-winsafer-saferidentifylevel) function to evaluate software restriction policies.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d5db-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9d5db-108">Syntax</span></span>


```C++
BOOL WINAPI SaferiSearchMatchingHashRules(
  _In_opt_ ALG_ID HashAlgorithm,
  _In_     PBYTE  pHashBytes,
  _In_     DWORD  dwHashSize,
  _In_opt_ DWORD  dwOriginalImageSize,
  _Out_    PDWORD pdwFoundLevel,
           PDWORD pdwSaferFlags
);
```



## <a name="parameters"></a><span data-ttu-id="9d5db-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="9d5db-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d5db-110">*HashAlgorithm* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="9d5db-110">*HashAlgorithm* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9d5db-111">Identificatore dell'algoritmo utilizzato per creare l'hash.</span><span class="sxs-lookup"><span data-stu-id="9d5db-111">The identifier of the algorithm used to create the hash.</span></span>

</dd> <dt>

<span data-ttu-id="9d5db-112">*pHashBytes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9d5db-112">*pHashBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d5db-113">Puntatore a una matrice di byte che contiene l'hash.</span><span class="sxs-lookup"><span data-stu-id="9d5db-113">A pointer to an array of bytes that contains the hash.</span></span>

</dd> <dt>

<span data-ttu-id="9d5db-114">*dwHashSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9d5db-114">*dwHashSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d5db-115">Dimensione, in byte, della matrice *pHashBytes* .</span><span class="sxs-lookup"><span data-stu-id="9d5db-115">The size, in bytes, of the *pHashBytes* array.</span></span>

</dd> <dt>

<span data-ttu-id="9d5db-116">*dwOriginalImageSize* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="9d5db-116">*dwOriginalImageSize* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9d5db-117">Dimensione, in byte, dell'immagine originale da cui è stato calcolato l'hash.</span><span class="sxs-lookup"><span data-stu-id="9d5db-117">The size, in bytes, of the original image from which the hash was computed.</span></span>

</dd> <dt>

<span data-ttu-id="9d5db-118">*pdwFoundLevel* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9d5db-118">*pdwFoundLevel* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9d5db-119">Puntatore all'identificatore di livello per la regola di identificazione hash corrispondente.</span><span class="sxs-lookup"><span data-stu-id="9d5db-119">A pointer to the level identifier for the matching hash identification rule.</span></span>

</dd> <dt>

<span data-ttu-id="9d5db-120">*pdwSaferFlags*</span><span class="sxs-lookup"><span data-stu-id="9d5db-120">*pdwSaferFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="9d5db-121">Riservato.</span><span class="sxs-lookup"><span data-stu-id="9d5db-121">Reserved.</span></span> <span data-ttu-id="9d5db-122">Impostare questo valore su zero.</span><span class="sxs-lookup"><span data-stu-id="9d5db-122">Set this value to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d5db-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9d5db-123">Return value</span></span>

<span data-ttu-id="9d5db-124">**True** se la funzione ha esito positivo; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="9d5db-124">**TRUE** if the function is successful; otherwise, **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d5db-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9d5db-125">Requirements</span></span>



| <span data-ttu-id="9d5db-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d5db-126">Requirement</span></span> | <span data-ttu-id="9d5db-127">Valore</span><span class="sxs-lookup"><span data-stu-id="9d5db-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d5db-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9d5db-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9d5db-129">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9d5db-129">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="9d5db-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9d5db-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9d5db-131">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9d5db-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9d5db-132">DLL</span><span class="sxs-lookup"><span data-stu-id="9d5db-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d5db-133"><dt>Advapi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d5db-133"><dt>Advapi32.dll</dt></span></span> </dl> |



 

 
