---
description: Il metodo getmedianame Recupera il nome del file di origine rappresentato da questo oggetto di origine.
ms.assetid: 6f468628-10e1-4746-9c3a-6dae9aa3f6ad
title: 'Metodo IAMTimelineSrc:: getmedianame (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetMediaName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3727d57371e5c7bab4f9d693a247b6b62a3ada17
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324259"
---
# <a name="iamtimelinesrcgetmedianame-method"></a><span data-ttu-id="bac0a-103">Metodo IAMTimelineSrc:: getmedianame</span><span class="sxs-lookup"><span data-stu-id="bac0a-103">IAMTimelineSrc::GetMediaName method</span></span>

> [!Note]  
> <span data-ttu-id="bac0a-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="bac0a-104">\[Deprecated.</span></span> <span data-ttu-id="bac0a-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="bac0a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="bac0a-106">Il `GetMediaName` metodo recupera il nome del file di origine rappresentato da questo oggetto di origine.</span><span class="sxs-lookup"><span data-stu-id="bac0a-106">The `GetMediaName` method retrieves the name of the source file represented by this source object.</span></span>

## <a name="syntax"></a><span data-ttu-id="bac0a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bac0a-107">Syntax</span></span>


```C++
HRESULT GetMediaName(
  [out, retval] BSTR *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="bac0a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="bac0a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bac0a-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="bac0a-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="bac0a-110">Riceve il nome del file.</span><span class="sxs-lookup"><span data-stu-id="bac0a-110">Receives the name of the file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bac0a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bac0a-111">Return value</span></span>

<span data-ttu-id="bac0a-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="bac0a-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bac0a-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bac0a-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bac0a-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="bac0a-114">Remarks</span></span>

<span data-ttu-id="bac0a-115">Il metodo alloca memoria per la stringa.</span><span class="sxs-lookup"><span data-stu-id="bac0a-115">The method allocates memory for the string.</span></span> <span data-ttu-id="bac0a-116">Per liberare la memoria, l'applicazione deve chiamare **SysFreeString** .</span><span class="sxs-lookup"><span data-stu-id="bac0a-116">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="bac0a-117">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="bac0a-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="bac0a-118">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="bac0a-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="bac0a-119">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="bac0a-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bac0a-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bac0a-120">Requirements</span></span>



| <span data-ttu-id="bac0a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="bac0a-121">Requirement</span></span> | <span data-ttu-id="bac0a-122">Valore</span><span class="sxs-lookup"><span data-stu-id="bac0a-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bac0a-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bac0a-123">Header</span></span><br/>  | <dl> <span data-ttu-id="bac0a-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="bac0a-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="bac0a-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="bac0a-125">Library</span></span><br/> | <dl> <span data-ttu-id="bac0a-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bac0a-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bac0a-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bac0a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bac0a-128">**Interfaccia IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="bac0a-128">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="bac0a-129">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="bac0a-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




