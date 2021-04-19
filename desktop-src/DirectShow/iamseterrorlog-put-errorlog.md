---
description: Il \_ metodo Put log degli errori specifica un log degli errori per l'oggetto.
ms.assetid: 39da3fb0-57d3-452f-b2ae-6dcd84fa5c8e
title: 'IAMSetErrorLog: metodo:p ut_ErrorLog (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMSetErrorLog.put_ErrorLog
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 189f0fed57d67d7632d07839ee82dd13494eb418
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326812"
---
# <a name="iamseterrorlogput_errorlog-method"></a><span data-ttu-id="c722c-103">IAMSetErrorLog::p \_ metodo di log degli errori UT</span><span class="sxs-lookup"><span data-stu-id="c722c-103">IAMSetErrorLog::put\_ErrorLog method</span></span>

> [!Note]  
> <span data-ttu-id="c722c-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="c722c-104">\[Deprecated.</span></span> <span data-ttu-id="c722c-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c722c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c722c-106">Il `put_ErrorLog` metodo specifica un log degli errori per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c722c-106">The `put_ErrorLog` method specifies an error log for the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c722c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c722c-107">Syntax</span></span>


```C++
HRESULT put_ErrorLog(
  [in] IAMErrorLog *newVal
);
```



## <a name="parameters"></a><span data-ttu-id="c722c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c722c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c722c-109">*newVal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c722c-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c722c-110">Puntatore all'interfaccia [**IAMErrorLog**](iamerrorlog.md) del log degli errori.</span><span class="sxs-lookup"><span data-stu-id="c722c-110">Pointer to the error log's [**IAMErrorLog**](iamerrorlog.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c722c-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c722c-111">Return value</span></span>

<span data-ttu-id="c722c-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c722c-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c722c-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c722c-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c722c-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="c722c-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c722c-115">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="c722c-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c722c-116">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="c722c-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c722c-117">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="c722c-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c722c-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c722c-118">Requirements</span></span>



| <span data-ttu-id="c722c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c722c-119">Requirement</span></span> | <span data-ttu-id="c722c-120">Valore</span><span class="sxs-lookup"><span data-stu-id="c722c-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c722c-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c722c-121">Header</span></span><br/>  | <dl> <span data-ttu-id="c722c-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c722c-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c722c-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="c722c-123">Library</span></span><br/> | <dl> <span data-ttu-id="c722c-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c722c-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c722c-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c722c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c722c-126">**Interfaccia IAMSetErrorLog**</span><span class="sxs-lookup"><span data-stu-id="c722c-126">**IAMSetErrorLog Interface**</span></span>](iamseterrorlog.md)
</dt> <dt>

[<span data-ttu-id="c722c-127">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="c722c-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




