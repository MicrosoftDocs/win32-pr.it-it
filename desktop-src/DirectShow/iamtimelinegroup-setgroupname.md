---
description: Il metodo segroupname imposta il nome definito dall'applicazione del gruppo.
ms.assetid: e1d8a91b-d5b9-42a4-9b98-582e1a57ac51
title: 'Metodo IAMTimelineGroup:: segroupname (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetGroupName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 327bf0384ce484353ac41c069ddf580c674b0b45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325488"
---
# <a name="iamtimelinegroupsetgroupname-method"></a><span data-ttu-id="62cda-103">Metodo IAMTimelineGroup:: segroupname</span><span class="sxs-lookup"><span data-stu-id="62cda-103">IAMTimelineGroup::SetGroupName method</span></span>

> [!Note]  
> <span data-ttu-id="62cda-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="62cda-104">\[Deprecated.</span></span> <span data-ttu-id="62cda-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="62cda-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="62cda-106">Il `SetGroupName` metodo imposta il nome definito dall'applicazione del gruppo.</span><span class="sxs-lookup"><span data-stu-id="62cda-106">The `SetGroupName` method sets the application-defined name of the group.</span></span>

## <a name="syntax"></a><span data-ttu-id="62cda-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="62cda-107">Syntax</span></span>


```C++
HRESULT SetGroupName(
   BSTR pGroupName
);
```



## <a name="parameters"></a><span data-ttu-id="62cda-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="62cda-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62cda-109">*pGroupName*</span><span class="sxs-lookup"><span data-stu-id="62cda-109">*pGroupName*</span></span> 
</dt> <dd>

<span data-ttu-id="62cda-110">**BSTR** che specifica il nome del gruppo.</span><span class="sxs-lookup"><span data-stu-id="62cda-110">**BSTR** that specifies the name of the group.</span></span> <span data-ttu-id="62cda-111">La lunghezza massima del nome è 256 caratteri, incuding il terminatore null.</span><span class="sxs-lookup"><span data-stu-id="62cda-111">The maximum length of the name is 256 characters, incuding the null terminator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62cda-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="62cda-112">Return value</span></span>

<span data-ttu-id="62cda-113">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="62cda-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="62cda-114">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="62cda-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="62cda-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="62cda-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="62cda-116">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="62cda-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="62cda-117">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="62cda-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="62cda-118">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="62cda-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="62cda-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="62cda-119">Requirements</span></span>



| <span data-ttu-id="62cda-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="62cda-120">Requirement</span></span> | <span data-ttu-id="62cda-121">Valore</span><span class="sxs-lookup"><span data-stu-id="62cda-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="62cda-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="62cda-122">Header</span></span><br/>  | <dl> <span data-ttu-id="62cda-123"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="62cda-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="62cda-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="62cda-124">Library</span></span><br/> | <dl> <span data-ttu-id="62cda-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="62cda-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62cda-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="62cda-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62cda-127">**Interfaccia IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="62cda-127">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="62cda-128">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="62cda-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




