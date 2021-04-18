---
description: Il metodo GetSubObject recupera l'oggetto SubObject associato a questo oggetto.
ms.assetid: 478597d6-ae13-4fa9-a928-19893f378f1a
title: 'Metodo IAMTimelineObj:: GetSubObject (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetSubObject
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 74f14658db5ffbaf100925f26573a08b592f6510
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328154"
---
# <a name="iamtimelineobjgetsubobject-method"></a><span data-ttu-id="6d77b-103">Metodo IAMTimelineObj:: GetSubObject</span><span class="sxs-lookup"><span data-stu-id="6d77b-103">IAMTimelineObj::GetSubObject method</span></span>

> [!Note]  
> <span data-ttu-id="6d77b-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="6d77b-104">\[Deprecated.</span></span> <span data-ttu-id="6d77b-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6d77b-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6d77b-106">Il `GetSubObject` metodo recupera l'oggetto SubObject associato a questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="6d77b-106">The `GetSubObject` method retrieves the subobject associated with this object.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d77b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6d77b-107">Syntax</span></span>


```C++
HRESULT GetSubObject(
  [out, retval] IUnknown **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="6d77b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6d77b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d77b-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="6d77b-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="6d77b-110">Riceve un puntatore all'interfaccia **IUnknown** dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6d77b-110">Receives a pointer to the subobject's **IUnknown** interface.</span></span> <span data-ttu-id="6d77b-111">Se l'oggetto non dispone di un oggetto SubObject, il valore viene impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="6d77b-111">If the object does not have a subobject, the value is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d77b-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6d77b-112">Return value</span></span>

<span data-ttu-id="6d77b-113">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6d77b-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6d77b-114">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6d77b-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d77b-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="6d77b-115">Remarks</span></span>

<span data-ttu-id="6d77b-116">Ogni oggetto sequenza temporale può avere un puntatore a un oggetto SubObject associato.</span><span class="sxs-lookup"><span data-stu-id="6d77b-116">Every timeline object can hold a pointer to an associated subobject.</span></span>

<span data-ttu-id="6d77b-117">Se il valore restituito in *pval* non è **null**, l'interfaccia **IUnknown** presenta un conteggio dei riferimenti in attesa.</span><span class="sxs-lookup"><span data-stu-id="6d77b-117">If the value returned in *pVal* is not **NULL**, the **IUnknown** interface has an outstanding reference count.</span></span> <span data-ttu-id="6d77b-118">Assicurarsi di rilasciare l'interfaccia al termine dell'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="6d77b-118">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="6d77b-119">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="6d77b-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="6d77b-120">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="6d77b-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="6d77b-121">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="6d77b-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6d77b-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6d77b-122">Requirements</span></span>



| <span data-ttu-id="6d77b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d77b-123">Requirement</span></span> | <span data-ttu-id="6d77b-124">Valore</span><span class="sxs-lookup"><span data-stu-id="6d77b-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d77b-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6d77b-125">Header</span></span><br/>  | <dl> <span data-ttu-id="6d77b-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d77b-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="6d77b-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="6d77b-127">Library</span></span><br/> | <dl> <span data-ttu-id="6d77b-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6d77b-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d77b-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6d77b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d77b-130">**Interfaccia IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="6d77b-130">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="6d77b-131">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="6d77b-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




