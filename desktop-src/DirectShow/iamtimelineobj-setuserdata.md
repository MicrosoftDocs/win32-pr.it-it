---
description: Il Metodo SetUserData imposta i dati persistenti definiti dall'applicazione.
ms.assetid: 195d8e92-a25c-40ff-8cc7-c1f05bdd76ab
title: 'Metodo IAMTimelineObj:: SetUserData (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetUserData
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7e09aafd614234827a704d8b9997f27981eb7c45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330801"
---
# <a name="iamtimelineobjsetuserdata-method"></a><span data-ttu-id="a9c1b-103">Metodo IAMTimelineObj:: SetUserData</span><span class="sxs-lookup"><span data-stu-id="a9c1b-103">IAMTimelineObj::SetUserData method</span></span>

> [!Note]  
> <span data-ttu-id="a9c1b-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="a9c1b-104">\[Deprecated.</span></span> <span data-ttu-id="a9c1b-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a9c1b-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a9c1b-106">Il `SetUserData` metodo imposta i dati persistenti definiti dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a9c1b-106">The `SetUserData` method sets application-defined persistent data.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9c1b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a9c1b-107">Syntax</span></span>


```C++
HRESULT SetUserData(
   BYTE *pData,
   long Size
);
```



## <a name="parameters"></a><span data-ttu-id="a9c1b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a9c1b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9c1b-109">*pData*</span><span class="sxs-lookup"><span data-stu-id="a9c1b-109">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="a9c1b-110">Puntatore a un buffer contenente i dati.</span><span class="sxs-lookup"><span data-stu-id="a9c1b-110">Pointer to a buffer containing the data.</span></span>

</dd> <dt>

<span data-ttu-id="a9c1b-111">*Dimensioni*</span><span class="sxs-lookup"><span data-stu-id="a9c1b-111">*Size*</span></span> 
</dt> <dd>

<span data-ttu-id="a9c1b-112">Dimensioni dei dati in byte.</span><span class="sxs-lookup"><span data-stu-id="a9c1b-112">Size of the data, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9c1b-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a9c1b-113">Return value</span></span>

<span data-ttu-id="a9c1b-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a9c1b-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a9c1b-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a9c1b-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9c1b-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="a9c1b-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a9c1b-117">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="a9c1b-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a9c1b-118">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="a9c1b-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a9c1b-119">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="a9c1b-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a9c1b-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a9c1b-120">Requirements</span></span>



| <span data-ttu-id="a9c1b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9c1b-121">Requirement</span></span> | <span data-ttu-id="a9c1b-122">Valore</span><span class="sxs-lookup"><span data-stu-id="a9c1b-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9c1b-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a9c1b-123">Header</span></span><br/>  | <dl> <span data-ttu-id="a9c1b-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9c1b-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a9c1b-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="a9c1b-125">Library</span></span><br/> | <dl> <span data-ttu-id="a9c1b-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a9c1b-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9c1b-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a9c1b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9c1b-128">**Interfaccia IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="a9c1b-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="a9c1b-129">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="a9c1b-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




