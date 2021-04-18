---
description: Il metodo GetUserName recupera il nome definito dall'applicazione dell'oggetto.
ms.assetid: 7d172ec5-9cb7-4418-a628-a109944077a6
title: 'Metodo IAMTimelineObj:: GetUserName (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetUserName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: efca014493cb5631e058927256bd1586aaca7ab7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330825"
---
# <a name="iamtimelineobjgetusername-method"></a><span data-ttu-id="46464-103">Metodo IAMTimelineObj:: GetUserName</span><span class="sxs-lookup"><span data-stu-id="46464-103">IAMTimelineObj::GetUserName method</span></span>

> [!Note]  
> <span data-ttu-id="46464-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="46464-104">\[Deprecated.</span></span> <span data-ttu-id="46464-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="46464-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="46464-106">Il `GetUserName` metodo recupera il nome definito dall'applicazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="46464-106">The `GetUserName` method retrieves the object's application-defined name.</span></span>

## <a name="syntax"></a><span data-ttu-id="46464-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="46464-107">Syntax</span></span>


```C++
HRESULT GetUserName(
  [out, retval] BSTR *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="46464-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="46464-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46464-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="46464-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="46464-110">Riceve il nome dell'oggetto come **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="46464-110">Receives the name of the object as a **BSTR**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46464-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="46464-111">Return value</span></span>

<span data-ttu-id="46464-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="46464-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="46464-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="46464-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="46464-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="46464-114">Remarks</span></span>

<span data-ttu-id="46464-115">Il metodo alloca memoria per la stringa.</span><span class="sxs-lookup"><span data-stu-id="46464-115">The method allocates memory for the string.</span></span> <span data-ttu-id="46464-116">Per liberare la memoria, l'applicazione deve chiamare **SysFreeString** .</span><span class="sxs-lookup"><span data-stu-id="46464-116">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="46464-117">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="46464-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="46464-118">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="46464-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="46464-119">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="46464-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="46464-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="46464-120">Requirements</span></span>



| <span data-ttu-id="46464-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="46464-121">Requirement</span></span> | <span data-ttu-id="46464-122">Valore</span><span class="sxs-lookup"><span data-stu-id="46464-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="46464-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="46464-123">Header</span></span><br/>  | <dl> <span data-ttu-id="46464-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="46464-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="46464-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="46464-125">Library</span></span><br/> | <dl> <span data-ttu-id="46464-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="46464-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46464-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="46464-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46464-128">**Interfaccia IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="46464-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="46464-129">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="46464-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




