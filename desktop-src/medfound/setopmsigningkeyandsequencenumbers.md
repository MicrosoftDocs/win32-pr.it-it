---
description: Imposta la chiave di firma e due numeri di sequenza su un oggetto di output protetto.
ms.assetid: 278a80f5-198d-4311-aa43-10b6dc33b3a4
title: SetOPMSigningKeyAndSequenceNumbers (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetOPMSigningKeyAndSequenceNumbers
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: cbd088b83acd4e93cc186e6c7b5635ad1e3d8346
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226502"
---
# <a name="setopmsigningkeyandsequencenumbers-function"></a><span data-ttu-id="be910-103">SetOPMSigningKeyAndSequenceNumbers (funzione)</span><span class="sxs-lookup"><span data-stu-id="be910-103">SetOPMSigningKeyAndSequenceNumbers function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="be910-104">Questa funzione viene utilizzata da [Output Protection Manager](output-protection-manager.md) (OPM) per accedere alla funzionalità nel driver di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="be910-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="be910-105">Le applicazioni non devono chiamare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="be910-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="be910-106">Imposta la chiave di firma e due numeri di sequenza su un oggetto di output protetto.</span><span class="sxs-lookup"><span data-stu-id="be910-106">Sets the signing key and two sequence numbers on a protected output object.</span></span>

## <a name="syntax"></a><span data-ttu-id="be910-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="be910-107">Syntax</span></span>


```C++
NTSTATUS WINAPI SetOPMSigningKeyAndSequenceNumbers(
  _In_        OPM_PROTECTED_OUTPUT_HANDLE      opoOPMProtectedOutput,
  _Out_ const DXGKMDT_OPM_ENCRYPTED_PARAMETERS *pParameters
);
```



## <a name="parameters"></a><span data-ttu-id="be910-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="be910-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be910-109">*opoOPMProtectedOutput* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="be910-109">*opoOPMProtectedOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be910-110">Handle per l'oggetto di output protetto.</span><span class="sxs-lookup"><span data-stu-id="be910-110">A handle to the protected output object.</span></span> <span data-ttu-id="be910-111">Questo handle viene ottenuto chiamando [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span><span class="sxs-lookup"><span data-stu-id="be910-111">This handle is obtained by calling [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span></span>

</dd> <dt>

<span data-ttu-id="be910-112">*pParameters* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="be910-112">*pParameters* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="be910-113">Puntatore a una struttura [**di \_ \_ \_ parametri crittografati di DXGKMDT OPM**](/windows-hardware/drivers/ddi/d3dkmdt/ns-d3dkmdt-_dxgkmdt_opm_encrypted_parameters) che contiene una matrice di 256 byte.</span><span class="sxs-lookup"><span data-stu-id="be910-113">A pointer to a [**DXGKMDT\_OPM\_ENCRYPTED\_PARAMETERS**](/windows-hardware/drivers/ddi/d3dkmdt/ns-d3dkmdt-_dxgkmdt_opm_encrypted_parameters) structure that contains a 256-byte array.</span></span> <span data-ttu-id="be910-114">Per ulteriori informazioni su come inizializzare questa matrice, vedere [DxgkDdiOPMSetSigningKeyAndSequenceNumbers](https://msdn.microsoft.com/library/aa906703.aspx).</span><span class="sxs-lookup"><span data-stu-id="be910-114">For more information about how to initialize this array, see [DxgkDdiOPMSetSigningKeyAndSequenceNumbers](https://msdn.microsoft.com/library/aa906703.aspx).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be910-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="be910-115">Return value</span></span>

<span data-ttu-id="be910-116">Se il metodo ha esito positivo, viene restituito **lo stato \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="be910-116">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="be910-117">In caso contrario, restituisce un codice di errore **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="be910-117">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="be910-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="be910-118">Remarks</span></span>

<span data-ttu-id="be910-119">Le applicazioni devono chiamare [**IOPMVideoOutput:: FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) anziché chiamare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="be910-119">Applications should call [**IOPMVideoOutput::FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) instead of calling this function.</span></span>

<span data-ttu-id="be910-120">A questa funzione non è associata alcuna libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="be910-120">This function has no associated import library.</span></span> <span data-ttu-id="be910-121">Per chiamare questa funzione, è necessario usare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per eseguire il collegamento dinamico a Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="be910-121">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="be910-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="be910-122">Requirements</span></span>



| <span data-ttu-id="be910-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="be910-123">Requirement</span></span> | <span data-ttu-id="be910-124">Valore</span><span class="sxs-lookup"><span data-stu-id="be910-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="be910-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="be910-125">Minimum supported client</span></span><br/> | <span data-ttu-id="be910-126">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="be910-126">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="be910-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="be910-127">Minimum supported server</span></span><br/> | <span data-ttu-id="be910-128">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="be910-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="be910-129">DLL</span><span class="sxs-lookup"><span data-stu-id="be910-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be910-130"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be910-130"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be910-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="be910-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be910-132">Funzioni di OPM</span><span class="sxs-lookup"><span data-stu-id="be910-132">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="be910-133">Gestione protezione output</span><span class="sxs-lookup"><span data-stu-id="be910-133">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
