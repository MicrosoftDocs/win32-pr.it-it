---
description: Il metodo seusername imposta un nome definito dall'applicazione per l'oggetto.
ms.assetid: 6f071884-519a-465f-8273-ab1be58dda8b
title: 'Metodo IAMTimelineObj:: seusername (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetUserName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8ec39aece23d38be6fbe2e69f7ded8bc738e04c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330797"
---
# <a name="iamtimelineobjsetusername-method"></a><span data-ttu-id="658f3-103">Metodo IAMTimelineObj:: seusername</span><span class="sxs-lookup"><span data-stu-id="658f3-103">IAMTimelineObj::SetUserName method</span></span>

> [!Note]  
> <span data-ttu-id="658f3-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="658f3-104">\[Deprecated.</span></span> <span data-ttu-id="658f3-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="658f3-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="658f3-106">Il `SetUserName` metodo imposta un nome definito dall'applicazione per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="658f3-106">The `SetUserName` method sets an application-defined name for the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="658f3-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="658f3-107">Syntax</span></span>


```C++
HRESULT SetUserName(
   BSTR newVal
);
```



## <a name="parameters"></a><span data-ttu-id="658f3-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="658f3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="658f3-109">*newVal*</span><span class="sxs-lookup"><span data-stu-id="658f3-109">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="658f3-110">Stringa di caratteri wide che contiene il nome.</span><span class="sxs-lookup"><span data-stu-id="658f3-110">Wide-character string that contains the name.</span></span> <span data-ttu-id="658f3-111">Le stringhe con lunghezza superiore a 256 caratteri potrebbero essere troncate.</span><span class="sxs-lookup"><span data-stu-id="658f3-111">Strings longer than 256 characters might be truncated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="658f3-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="658f3-112">Return value</span></span>

<span data-ttu-id="658f3-113">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="658f3-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="658f3-114">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="658f3-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="658f3-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="658f3-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="658f3-116">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="658f3-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="658f3-117">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="658f3-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="658f3-118">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="658f3-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="658f3-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="658f3-119">Requirements</span></span>



| <span data-ttu-id="658f3-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="658f3-120">Requirement</span></span> | <span data-ttu-id="658f3-121">Valore</span><span class="sxs-lookup"><span data-stu-id="658f3-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="658f3-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="658f3-122">Header</span></span><br/>  | <dl> <span data-ttu-id="658f3-123"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="658f3-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="658f3-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="658f3-124">Library</span></span><br/> | <dl> <span data-ttu-id="658f3-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="658f3-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="658f3-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="658f3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="658f3-127">**Interfaccia IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="658f3-127">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="658f3-128">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="658f3-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




