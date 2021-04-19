---
description: Il \_ metodo get log degli errori Recupera il log degli errori corrente per questo oggetto.
ms.assetid: 580b8a06-6bf2-49ef-a5fb-5e6df2f09793
title: 'Metodo IAMSetErrorLog:: get_ErrorLog (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMSetErrorLog.get_ErrorLog
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 508a73d6475698dca628de7e3bb96001fe13bcd0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326813"
---
# <a name="iamseterrorlogget_errorlog-method"></a><span data-ttu-id="d94f3-103">Metodo IAMSetErrorLog:: Get \_ log</span><span class="sxs-lookup"><span data-stu-id="d94f3-103">IAMSetErrorLog::get\_ErrorLog method</span></span>

> [!Note]  
> <span data-ttu-id="d94f3-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="d94f3-104">\[Deprecated.</span></span> <span data-ttu-id="d94f3-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d94f3-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d94f3-106">Il `get_ErrorLog` metodo recupera il log degli errori corrente per questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="d94f3-106">The `get_ErrorLog` method retrieves the current error log for this object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d94f3-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d94f3-107">Syntax</span></span>


```C++
HRESULT get_ErrorLog(
  [out, retval] IAMErrorLog **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="d94f3-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d94f3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d94f3-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="d94f3-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="d94f3-110">Riceve un puntatore all'interfaccia [**IAMErrorLog**](iamerrorlog.md) del log degli errori.</span><span class="sxs-lookup"><span data-stu-id="d94f3-110">Receives a pointer to the error log's [**IAMErrorLog**](iamerrorlog.md) interface.</span></span> <span data-ttu-id="d94f3-111">Se per la sequenza temporale non è presente un log degli errori, il valore viene impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="d94f3-111">If the timeline does not have an error log, the value is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d94f3-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d94f3-112">Return value</span></span>

<span data-ttu-id="d94f3-113">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d94f3-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d94f3-114">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d94f3-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d94f3-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="d94f3-115">Remarks</span></span>

<span data-ttu-id="d94f3-116">Se il valore restituito in *pval* non è **null**, l'interfaccia [**IAMErrorLog**](iamerrorlog.md) include un conteggio dei riferimenti in attesa.</span><span class="sxs-lookup"><span data-stu-id="d94f3-116">If the value returned in *pVal* is not **NULL**, the [**IAMErrorLog**](iamerrorlog.md) interface has an outstanding reference count.</span></span> <span data-ttu-id="d94f3-117">Assicurarsi di rilasciare l'interfaccia al termine dell'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="d94f3-117">Be sure to release the interface when you are done using it.</span></span>

> [!Note]  
> <span data-ttu-id="d94f3-118">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="d94f3-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d94f3-119">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d94f3-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d94f3-120">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="d94f3-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d94f3-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d94f3-121">Requirements</span></span>



| <span data-ttu-id="d94f3-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d94f3-122">Requirement</span></span> | <span data-ttu-id="d94f3-123">Valore</span><span class="sxs-lookup"><span data-stu-id="d94f3-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d94f3-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d94f3-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d94f3-125"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d94f3-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d94f3-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="d94f3-126">Library</span></span><br/> | <dl> <span data-ttu-id="d94f3-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d94f3-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d94f3-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d94f3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d94f3-129">**Interfaccia IAMSetErrorLog**</span><span class="sxs-lookup"><span data-stu-id="d94f3-129">**IAMSetErrorLog Interface**</span></span>](iamseterrorlog.md)
</dt> <dt>

[<span data-ttu-id="d94f3-130">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="d94f3-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




