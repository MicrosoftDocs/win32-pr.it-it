---
description: Ottiene un numero casuale a 128 bit e a crittografia sicura da un oggetto di output protetto.
ms.assetid: d5adfa5c-ae61-43d5-916d-05085abea38b
title: GetOPMRandomNumber (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetOPMRandomNumber
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: f78b17dcf9ffff7a5fa26ce16e96299e5cf8386c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342451"
---
# <a name="getopmrandomnumber-function"></a><span data-ttu-id="32a8f-103">GetOPMRandomNumber (funzione)</span><span class="sxs-lookup"><span data-stu-id="32a8f-103">GetOPMRandomNumber function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="32a8f-104">Questa funzione viene utilizzata da [Output Protection Manager](output-protection-manager.md) (OPM) per accedere alla funzionalità nel driver di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="32a8f-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="32a8f-105">Le applicazioni non devono chiamare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="32a8f-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="32a8f-106">Ottiene un numero casuale a 128 bit e a crittografia sicura da un oggetto di output protetto.</span><span class="sxs-lookup"><span data-stu-id="32a8f-106">Gets a 128-bit, cryptographically secure random number from a protected output object.</span></span>

## <a name="syntax"></a><span data-ttu-id="32a8f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="32a8f-107">Syntax</span></span>


```C++
NTSTATUS WINAPI GetOPMRandomNumber(
  _In_  OPM_PROTECTED_OUTPUT_HANDLE opoOPMProtectedOutput,
  _Out_ DXGKMDT_OPM_RANDOM_NUMBER   *prnRandomNumber
);
```



## <a name="parameters"></a><span data-ttu-id="32a8f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="32a8f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32a8f-109">*opoOPMProtectedOutput* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="32a8f-109">*opoOPMProtectedOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32a8f-110">Handle per l'oggetto di output protetto.</span><span class="sxs-lookup"><span data-stu-id="32a8f-110">A handle to the protected output object.</span></span> <span data-ttu-id="32a8f-111">Questo handle viene ottenuto chiamando [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span><span class="sxs-lookup"><span data-stu-id="32a8f-111">This handle is obtained by calling [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span></span>

</dd> <dt>

<span data-ttu-id="32a8f-112">*prnRandomNumber* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="32a8f-112">*prnRandomNumber* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="32a8f-113">Puntatore a una struttura **di \_ \_ \_ numeri casuali DXGKMDT OPM** che riceve il numero casuale.</span><span class="sxs-lookup"><span data-stu-id="32a8f-113">A pointer to a **DXGKMDT\_OPM\_RANDOM\_NUMBER** structure that receives the random number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32a8f-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="32a8f-114">Return value</span></span>

<span data-ttu-id="32a8f-115">Se il metodo ha esito positivo, viene restituito **lo stato \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="32a8f-115">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="32a8f-116">In caso contrario, restituisce un codice di errore **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="32a8f-116">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="32a8f-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="32a8f-117">Remarks</span></span>

<span data-ttu-id="32a8f-118">A questa funzione non è associata alcuna libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="32a8f-118">This function has no associated import library.</span></span> <span data-ttu-id="32a8f-119">Per chiamare questa funzione, è necessario usare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per eseguire il collegamento dinamico a Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="32a8f-119">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="32a8f-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="32a8f-120">Requirements</span></span>



| <span data-ttu-id="32a8f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="32a8f-121">Requirement</span></span> | <span data-ttu-id="32a8f-122">Valore</span><span class="sxs-lookup"><span data-stu-id="32a8f-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="32a8f-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="32a8f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="32a8f-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="32a8f-124">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="32a8f-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="32a8f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="32a8f-126">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="32a8f-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="32a8f-127">DLL</span><span class="sxs-lookup"><span data-stu-id="32a8f-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32a8f-128"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32a8f-128"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32a8f-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="32a8f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32a8f-130">Funzioni di OPM</span><span class="sxs-lookup"><span data-stu-id="32a8f-130">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="32a8f-131">Gestione protezione output</span><span class="sxs-lookup"><span data-stu-id="32a8f-131">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
