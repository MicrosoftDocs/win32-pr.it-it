---
description: Chiude un handle a un provider di ticket di stampa.
ms.assetid: ce979c89-9f9d-4e89-b142-beed414caa3f
title: UnbindPTProviderThunk (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UnbindPTProviderThunk
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: dd87f528603624e9957d8c5f3fb12cc857ec4f5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311808"
---
# <a name="unbindptproviderthunk-function"></a><span data-ttu-id="8158e-103">UnbindPTProviderThunk (funzione)</span><span class="sxs-lookup"><span data-stu-id="8158e-103">UnbindPTProviderThunk function</span></span>

<span data-ttu-id="8158e-104">\[Questa funzione non è supportata e potrebbe essere disabilitata o eliminata nelle versioni future di Windows.</span><span class="sxs-lookup"><span data-stu-id="8158e-104">\[This function is not supported and might be disabled or deleted in future versions of Windows.</span></span> <span data-ttu-id="8158e-105">[**PTCloseProvider**](/windows/desktop/api/prntvpt/nf-prntvpt-ptcloseprovider) fornisce funzionalità equivalenti e deve essere usato in alternativa.\]</span><span class="sxs-lookup"><span data-stu-id="8158e-105">[**PTCloseProvider**](/windows/desktop/api/prntvpt/nf-prntvpt-ptcloseprovider) provides equivalent functionality and should be used instead.\]</span></span>

<span data-ttu-id="8158e-106">Chiude un handle a un provider di ticket di stampa.</span><span class="sxs-lookup"><span data-stu-id="8158e-106">Closes a handle to a print ticket provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="8158e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8158e-107">Syntax</span></span>


```C++
HRESULT UnbindPTProviderThunk(
  _In_ HPTPROVIDER hProvider
);
```



## <a name="parameters"></a><span data-ttu-id="8158e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8158e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8158e-109">*hProvider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8158e-109">*hProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8158e-110">Handle per un provider di ticket di stampa aperto.</span><span class="sxs-lookup"><span data-stu-id="8158e-110">A handle to an open print ticket provider.</span></span> <span data-ttu-id="8158e-111">Questo handle viene restituito dalla funzione [**BindPTProviderThunk**](bindptproviderthunk.md) .</span><span class="sxs-lookup"><span data-stu-id="8158e-111">This handle is returned by the [**BindPTProviderThunk**](bindptproviderthunk.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8158e-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8158e-112">Return value</span></span>

<span data-ttu-id="8158e-113">Se il metodo ha esito positivo, restituisce **S \_ OK**. in caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8158e-113">If the method succeeds, it returns **S\_OK**; otherwise, it returns an **HRESULT** error code.</span></span> <span data-ttu-id="8158e-114">Per ulteriori informazioni sui codici di errore COM, vedere [gestione degli errori](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="8158e-114">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8158e-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8158e-115">Requirements</span></span>



| <span data-ttu-id="8158e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8158e-116">Requirement</span></span> | <span data-ttu-id="8158e-117">Valore</span><span class="sxs-lookup"><span data-stu-id="8158e-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8158e-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8158e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8158e-119">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8158e-119">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="8158e-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8158e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8158e-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8158e-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8158e-122">DLL</span><span class="sxs-lookup"><span data-stu-id="8158e-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8158e-123"><dt>Prntvpt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8158e-123"><dt>Prntvpt.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8158e-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8158e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8158e-125">Stampa schema</span><span class="sxs-lookup"><span data-stu-id="8158e-125">Print Schema</span></span>](./printschema.md)
</dt> <dt>

[<span data-ttu-id="8158e-126">**PTCloseProvider**</span><span class="sxs-lookup"><span data-stu-id="8158e-126">**PTCloseProvider**</span></span>](/windows/desktop/api/prntvpt/nf-prntvpt-ptcloseprovider)
</dt> <dt>

[<span data-ttu-id="8158e-127">Stampa</span><span class="sxs-lookup"><span data-stu-id="8158e-127">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="8158e-128">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="8158e-128">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

