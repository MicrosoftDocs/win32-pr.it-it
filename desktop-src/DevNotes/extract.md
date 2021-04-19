---
description: La funzione extract estrae i file da un file CAB.
ms.assetid: c6a79d81-7adf-4b8e-a1ef-fec868f7fdbf
title: Estrarre la funzione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extract
api_type:
- DllExport
api_location:
- Cabinet.dll
ms.openlocfilehash: 2e1096cdb7909f49fbcac7c32891210b25637c90
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330094"
---
# <a name="extract-function"></a><span data-ttu-id="dfe88-103">Estrarre la funzione</span><span class="sxs-lookup"><span data-stu-id="dfe88-103">Extract function</span></span>

<span data-ttu-id="dfe88-104">\[Questa funzione non è più supportata, pertanto non è possibile garantirne il comportamento.\]</span><span class="sxs-lookup"><span data-stu-id="dfe88-104">\[This function is no longer supported, so its behavior cannot be guaranteed.\]</span></span>

<span data-ttu-id="dfe88-105">La funzione **Extract** estrae i file da un file CAB.</span><span class="sxs-lookup"><span data-stu-id="dfe88-105">The **Extract** function extracts files from a cabinet.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfe88-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dfe88-106">Syntax</span></span>


```C++
HRESULT Extract(
   PSESSION ps,
   LPCSTR   lpCabName
);
```



## <a name="parameters"></a><span data-ttu-id="dfe88-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="dfe88-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfe88-108">*ps*</span><span class="sxs-lookup"><span data-stu-id="dfe88-108">*ps*</span></span> 
</dt> <dd>

<span data-ttu-id="dfe88-109">Puntatore a una struttura di [**sessione**](session.md) che contiene informazioni sulla sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="dfe88-109">Pointer to a [**SESSION**](session.md) structure that contains information about the current session.</span></span>

</dd> <dt>

<span data-ttu-id="dfe88-110">*lpCabName*</span><span class="sxs-lookup"><span data-stu-id="dfe88-110">*lpCabName*</span></span> 
</dt> <dd>

<span data-ttu-id="dfe88-111">Puntatore al nome del file CAB da cui estrarre i file.</span><span class="sxs-lookup"><span data-stu-id="dfe88-111">Pointer to the name of the cabinet from which files are to be extracted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfe88-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dfe88-112">Return value</span></span>

<span data-ttu-id="dfe88-113">Se la funzione ha esito positivo, restituisce **S \_ OK**. in caso contrario, restituisce un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="dfe88-113">If the function succeeds, it returns **S\_OK**; otherwise, it returns an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="dfe88-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="dfe88-114">Remarks</span></span>

<span data-ttu-id="dfe88-115">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="dfe88-115">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfe88-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dfe88-116">Requirements</span></span>



| <span data-ttu-id="dfe88-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfe88-117">Requirement</span></span> | <span data-ttu-id="dfe88-118">Valore</span><span class="sxs-lookup"><span data-stu-id="dfe88-118">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dfe88-119">DLL</span><span class="sxs-lookup"><span data-stu-id="dfe88-119">DLL</span></span><br/> | <dl> <span data-ttu-id="dfe88-120"><dt>Cabinet.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dfe88-120"><dt>Cabinet.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfe88-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dfe88-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfe88-122">**DeleteExtractedFiles**</span><span class="sxs-lookup"><span data-stu-id="dfe88-122">**DeleteExtractedFiles**</span></span>](deleteextractedfiles.md)
</dt> <dt>

[<span data-ttu-id="dfe88-123">**ERF**</span><span class="sxs-lookup"><span data-stu-id="dfe88-123">**ERF**</span></span>](/windows/win32/api/fdi_fci_types/ns-fdi_fci_types-erf)
</dt> <dt>

[<span data-ttu-id="dfe88-124">**SESSIONE**</span><span class="sxs-lookup"><span data-stu-id="dfe88-124">**SESSION**</span></span>](session.md)
</dt> </dl>

 

 
