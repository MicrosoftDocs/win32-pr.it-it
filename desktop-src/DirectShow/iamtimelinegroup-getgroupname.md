---
description: Il metodo GetGroupName Recupera il nome definito dall'applicazione del gruppo.
ms.assetid: 402e97d9-abb5-4d8e-8735-1b06d60ab225
title: 'Metodo IAMTimelineGroup:: GetGroupName (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetGroupName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 78e3fc736ece3f4a8ebea1c688ce2bc5099f497c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333691"
---
# <a name="iamtimelinegroupgetgroupname-method"></a><span data-ttu-id="49623-103">Metodo IAMTimelineGroup:: GetGroupName</span><span class="sxs-lookup"><span data-stu-id="49623-103">IAMTimelineGroup::GetGroupName method</span></span>

> [!Note]  
> <span data-ttu-id="49623-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="49623-104">\[Deprecated.</span></span> <span data-ttu-id="49623-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="49623-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="49623-106">Il `GetGroupName` metodo recupera il nome definito dall'applicazione del gruppo.</span><span class="sxs-lookup"><span data-stu-id="49623-106">The `GetGroupName` method retrieves the application-defined name of the group.</span></span>

## <a name="syntax"></a><span data-ttu-id="49623-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="49623-107">Syntax</span></span>


```C++
HRESULT GetGroupName(
  [out, retval] BSTR *pGroupName
);
```



## <a name="parameters"></a><span data-ttu-id="49623-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="49623-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49623-109">*pGroupName* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="49623-109">*pGroupName* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="49623-110">Riceve il nome del gruppo.</span><span class="sxs-lookup"><span data-stu-id="49623-110">Receives the name of the group.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49623-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="49623-111">Return value</span></span>

<span data-ttu-id="49623-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="49623-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="49623-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="49623-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="49623-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="49623-114">Remarks</span></span>

<span data-ttu-id="49623-115">Il metodo alloca memoria per la stringa.</span><span class="sxs-lookup"><span data-stu-id="49623-115">The method allocates memory for the string.</span></span> <span data-ttu-id="49623-116">Per liberare la memoria, l'applicazione deve chiamare **SysFreeString** .</span><span class="sxs-lookup"><span data-stu-id="49623-116">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="49623-117">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="49623-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="49623-118">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="49623-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="49623-119">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="49623-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="49623-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="49623-120">Requirements</span></span>



| <span data-ttu-id="49623-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="49623-121">Requirement</span></span> | <span data-ttu-id="49623-122">Valore</span><span class="sxs-lookup"><span data-stu-id="49623-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="49623-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="49623-123">Header</span></span><br/>  | <dl> <span data-ttu-id="49623-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="49623-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="49623-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="49623-125">Library</span></span><br/> | <dl> <span data-ttu-id="49623-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="49623-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49623-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="49623-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49623-128">**Interfaccia IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="49623-128">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="49623-129">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="49623-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




