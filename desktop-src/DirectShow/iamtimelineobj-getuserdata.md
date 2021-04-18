---
description: Il metodo GetUserData recupera i dati persistenti definiti dall'applicazione.
ms.assetid: dd2cdb37-9c4f-4356-a35f-2d42b7588da6
title: 'Metodo IAMTimelineObj:: GetUserData (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetUserData
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9dda74980dcdae9cd73e749d9cb4324b4c6357f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331516"
---
# <a name="iamtimelineobjgetuserdata-method"></a><span data-ttu-id="6c078-103">Metodo IAMTimelineObj:: GetUserData</span><span class="sxs-lookup"><span data-stu-id="6c078-103">IAMTimelineObj::GetUserData method</span></span>

> [!Note]  
> <span data-ttu-id="6c078-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="6c078-104">\[Deprecated.</span></span> <span data-ttu-id="6c078-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6c078-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6c078-106">Il `GetUserData` metodo recupera i dati persistenti definiti dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6c078-106">The `GetUserData` method retrieves the application-defined persistent data.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c078-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6c078-107">Syntax</span></span>


```C++
HRESULT GetUserData(
   BYTE *pData,
   long *pSize
);
```



## <a name="parameters"></a><span data-ttu-id="6c078-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6c078-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c078-109">*pData*</span><span class="sxs-lookup"><span data-stu-id="6c078-109">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="6c078-110">Puntatore a un buffer che riceve i dati.</span><span class="sxs-lookup"><span data-stu-id="6c078-110">Pointer to a buffer that receives the data.</span></span> <span data-ttu-id="6c078-111">Per determinare le dimensioni del buffer da allocare, impostare questo parametro su **null**.</span><span class="sxs-lookup"><span data-stu-id="6c078-111">To determine the size of buffer to allocate, set this parameter to **NULL**.</span></span> <span data-ttu-id="6c078-112">La dimensione richiesta viene restituita in *psize*.</span><span class="sxs-lookup"><span data-stu-id="6c078-112">The required size is returned in *pSize*.</span></span>

</dd> <dt>

<span data-ttu-id="6c078-113">*pSize*</span><span class="sxs-lookup"><span data-stu-id="6c078-113">*pSize*</span></span> 
</dt> <dd>

<span data-ttu-id="6c078-114">Riceve le dimensioni dei dati in byte.</span><span class="sxs-lookup"><span data-stu-id="6c078-114">Receives the size of the data, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c078-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6c078-115">Return value</span></span>

<span data-ttu-id="6c078-116">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6c078-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6c078-117">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6c078-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c078-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="6c078-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6c078-119">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="6c078-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="6c078-120">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="6c078-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="6c078-121">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="6c078-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6c078-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6c078-122">Requirements</span></span>



| <span data-ttu-id="6c078-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c078-123">Requirement</span></span> | <span data-ttu-id="6c078-124">Valore</span><span class="sxs-lookup"><span data-stu-id="6c078-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c078-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6c078-125">Header</span></span><br/>  | <dl> <span data-ttu-id="6c078-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c078-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="6c078-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="6c078-127">Library</span></span><br/> | <dl> <span data-ttu-id="6c078-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6c078-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c078-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6c078-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c078-130">**Interfaccia IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="6c078-130">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="6c078-131">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="6c078-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




