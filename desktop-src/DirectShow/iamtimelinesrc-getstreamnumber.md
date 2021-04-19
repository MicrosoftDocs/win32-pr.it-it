---
description: Il metodo GetStreamNumber Recupera il numero del flusso corrente per l'oggetto di origine.
ms.assetid: c9c0c9f7-2716-436d-902c-f2255bedaffb
title: 'Metodo IAMTimelineSrc:: GetStreamNumber (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetStreamNumber
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d6fc9387499f675dd011dbceecbaf1aecdd287ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332764"
---
# <a name="iamtimelinesrcgetstreamnumber-method"></a><span data-ttu-id="8409e-103">Metodo IAMTimelineSrc:: GetStreamNumber</span><span class="sxs-lookup"><span data-stu-id="8409e-103">IAMTimelineSrc::GetStreamNumber method</span></span>

> [!Note]  
> <span data-ttu-id="8409e-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="8409e-104">\[Deprecated.</span></span> <span data-ttu-id="8409e-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8409e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="8409e-106">Il `GetStreamNumber` metodo recupera il numero del flusso corrente per l'oggetto di origine.</span><span class="sxs-lookup"><span data-stu-id="8409e-106">The `GetStreamNumber` method retrieves the current stream number for the source object.</span></span>

## <a name="syntax"></a><span data-ttu-id="8409e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8409e-107">Syntax</span></span>


```C++
HRESULT GetStreamNumber(
   long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="8409e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8409e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8409e-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="8409e-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="8409e-110">Riceve il numero di flusso.</span><span class="sxs-lookup"><span data-stu-id="8409e-110">Receives the stream number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8409e-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8409e-111">Return value</span></span>

<span data-ttu-id="8409e-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="8409e-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8409e-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8409e-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8409e-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="8409e-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8409e-115">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="8409e-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="8409e-116">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="8409e-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="8409e-117">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="8409e-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8409e-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8409e-118">Requirements</span></span>



| <span data-ttu-id="8409e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8409e-119">Requirement</span></span> | <span data-ttu-id="8409e-120">Valore</span><span class="sxs-lookup"><span data-stu-id="8409e-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8409e-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8409e-121">Header</span></span><br/>  | <dl> <span data-ttu-id="8409e-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="8409e-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="8409e-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="8409e-123">Library</span></span><br/> | <dl> <span data-ttu-id="8409e-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8409e-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8409e-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8409e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8409e-126">**Interfaccia IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="8409e-126">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="8409e-127">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="8409e-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




