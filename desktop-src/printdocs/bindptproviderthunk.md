---
description: Apre un'istanza di un provider di ticket di stampa.
ms.assetid: 815cc360-8dcd-4c58-a64d-5d77436a8623
title: BindPTProviderThunk (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BindPTProviderThunk
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: bf63fc6faf9d47993fafb97c8d3a1c18d6d6c985
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227358"
---
# <a name="bindptproviderthunk-function"></a><span data-ttu-id="73fca-103">BindPTProviderThunk (funzione)</span><span class="sxs-lookup"><span data-stu-id="73fca-103">BindPTProviderThunk function</span></span>

<span data-ttu-id="73fca-104">\[Questa funzione non è supportata e potrebbe essere disabilitata o eliminata nelle versioni future di Windows.</span><span class="sxs-lookup"><span data-stu-id="73fca-104">\[This function is not supported and might be disabled or deleted in future versions of Windows.</span></span> <span data-ttu-id="73fca-105">[**PTOpenProviderEx**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex) fornisce funzionalità equivalenti e deve essere usato in alternativa.\]</span><span class="sxs-lookup"><span data-stu-id="73fca-105">[**PTOpenProviderEx**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex) provides equivalent functionality and should be used instead.\]</span></span>

<span data-ttu-id="73fca-106">Apre un'istanza di un provider di ticket di stampa.</span><span class="sxs-lookup"><span data-stu-id="73fca-106">Opens an instance of a print ticket provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="73fca-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="73fca-107">Syntax</span></span>


```C++
HRESULT BindPTProviderThunk(
  _In_  LPTSTR      pszPrinterName,
  _In_  INT         maxVersion,
  _In_  INT         prefVersion,
  _Out_ HPTPROVIDER *phProvider,
  _Out_ INT         *usedVersion
);
```



## <a name="parameters"></a><span data-ttu-id="73fca-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="73fca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73fca-109">*pszPrinterName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="73fca-109">*pszPrinterName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73fca-110">Nome completo di una coda di stampa.</span><span class="sxs-lookup"><span data-stu-id="73fca-110">The full name of a print queue.</span></span>

</dd> <dt>

<span data-ttu-id="73fca-111">*MaxVersion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="73fca-111">*maxVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73fca-112">Versione più recente dello [schema di stampa](./printschema.md) supportato dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="73fca-112">The latest version of the [Print Schema](./printschema.md) that the caller supports.</span></span>

</dd> <dt>

<span data-ttu-id="73fca-113">*prefVersion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="73fca-113">*prefVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73fca-114">Versione dello schema di [stampa](./printschema.md) richiesta dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="73fca-114">The version of the [Print Schema](./printschema.md) requested by the caller.</span></span>

</dd> <dt>

<span data-ttu-id="73fca-115">*phProvider* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="73fca-115">*phProvider* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="73fca-116">Puntatore a un handle per il provider del ticket di stampa.</span><span class="sxs-lookup"><span data-stu-id="73fca-116">A pointer to a handle to the print ticket provider.</span></span>

</dd> <dt>

<span data-ttu-id="73fca-117">*usedVersion* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="73fca-117">*usedVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="73fca-118">Versione dello schema di [stampa](./printschema.md) che userà il provider del ticket di stampa.</span><span class="sxs-lookup"><span data-stu-id="73fca-118">The version of the [Print Schema](./printschema.md) that the print ticket provider will use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73fca-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="73fca-119">Return value</span></span>

<span data-ttu-id="73fca-120">Se il metodo ha esito positivo, restituisce **S \_ OK**. in caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="73fca-120">If the method succeeds, it returns **S\_OK**; otherwise, it returns an **HRESULT** error code.</span></span> <span data-ttu-id="73fca-121">Per ulteriori informazioni sui codici di errore COM, vedere [gestione degli errori](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="73fca-121">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="73fca-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="73fca-122">Remarks</span></span>

<span data-ttu-id="73fca-123">Prima di chiamare questa funzione, il thread chiamante deve inizializzare COM chiamando [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex).</span><span class="sxs-lookup"><span data-stu-id="73fca-123">Before calling this function, the calling thread must initialize COM by calling [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex).</span></span>

## <a name="requirements"></a><span data-ttu-id="73fca-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="73fca-124">Requirements</span></span>



| <span data-ttu-id="73fca-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="73fca-125">Requirement</span></span> | <span data-ttu-id="73fca-126">Valore</span><span class="sxs-lookup"><span data-stu-id="73fca-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="73fca-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="73fca-127">Minimum supported client</span></span><br/> | <span data-ttu-id="73fca-128">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="73fca-128">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="73fca-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="73fca-129">Minimum supported server</span></span><br/> | <span data-ttu-id="73fca-130">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="73fca-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="73fca-131">DLL</span><span class="sxs-lookup"><span data-stu-id="73fca-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73fca-132"><dt>Prntvpt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73fca-132"><dt>Prntvpt.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73fca-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="73fca-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73fca-134">Stampa schema</span><span class="sxs-lookup"><span data-stu-id="73fca-134">Print Schema</span></span>](./printschema.md)
</dt> <dt>

[<span data-ttu-id="73fca-135">**PTOpenProviderEx**</span><span class="sxs-lookup"><span data-stu-id="73fca-135">**PTOpenProviderEx**</span></span>](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex)
</dt> <dt>

[<span data-ttu-id="73fca-136">Stampa</span><span class="sxs-lookup"><span data-stu-id="73fca-136">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="73fca-137">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="73fca-137">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

