---
description: "Il metodo GetSubObjectGUIDB Recupera il GUID dell'oggetto SubObject associato a questo oggetto sequenza temporale. Questo metodo è equivalente a IAMTimelineObj:: GetSubObjectGUID, ma riceve un valore BSTR."
ms.assetid: 693cafda-78c8-4ba4-90d7-23fedcd1fc52
title: 'Metodo IAMTimelineObj:: GetSubObjectGUIDB (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetSubObjectGUIDB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 903c6638eececd635af2facd964adabe26f0c106
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326555"
---
# <a name="iamtimelineobjgetsubobjectguidb-method"></a><span data-ttu-id="b2049-104">Metodo IAMTimelineObj:: GetSubObjectGUIDB</span><span class="sxs-lookup"><span data-stu-id="b2049-104">IAMTimelineObj::GetSubObjectGUIDB method</span></span>

> [!Note]  
> <span data-ttu-id="b2049-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="b2049-105">\[Deprecated.</span></span> <span data-ttu-id="b2049-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b2049-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b2049-107">Il `GetSubObjectGUIDB` metodo recupera il GUID dell'oggetto SubObject associato a questo oggetto sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="b2049-107">The `GetSubObjectGUIDB` method retrieves the GUID of the subobject associated with this timeline object.</span></span> <span data-ttu-id="b2049-108">Questo metodo è equivalente a [**IAMTimelineObj:: GetSubObjectGUID**](iamtimelineobj-getsubobjectguid.md), ma riceve un valore **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="b2049-108">This method is equivalent to [**IAMTimelineObj::GetSubObjectGUID**](iamtimelineobj-getsubobjectguid.md), but receives a **BSTR** value.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2049-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b2049-109">Syntax</span></span>


```C++
HRESULT GetSubObjectGUIDB(
  [out, retval] BSTR *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="b2049-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="b2049-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2049-111">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="b2049-111">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="b2049-112">Riceve una stringa che rappresenta il GUID dell'oggetto SubObject.</span><span class="sxs-lookup"><span data-stu-id="b2049-112">Receives a string representing the subobject GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2049-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b2049-113">Return value</span></span>

<span data-ttu-id="b2049-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b2049-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b2049-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b2049-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2049-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="b2049-116">Remarks</span></span>

<span data-ttu-id="b2049-117">Il metodo alloca memoria per la stringa.</span><span class="sxs-lookup"><span data-stu-id="b2049-117">The method allocates memory for the string.</span></span> <span data-ttu-id="b2049-118">Per liberare la memoria, l'applicazione deve chiamare **SysFreeString** .</span><span class="sxs-lookup"><span data-stu-id="b2049-118">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="b2049-119">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="b2049-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b2049-120">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="b2049-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b2049-121">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="b2049-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b2049-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b2049-122">Requirements</span></span>



| <span data-ttu-id="b2049-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2049-123">Requirement</span></span> | <span data-ttu-id="b2049-124">Valore</span><span class="sxs-lookup"><span data-stu-id="b2049-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2049-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b2049-125">Header</span></span><br/>  | <dl> <span data-ttu-id="b2049-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2049-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b2049-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="b2049-127">Library</span></span><br/> | <dl> <span data-ttu-id="b2049-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b2049-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2049-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b2049-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2049-130">**Interfaccia IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="b2049-130">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="b2049-131">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="b2049-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




