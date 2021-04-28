---
description: 'Metodo IXml2Dex::WriteXMLPart: non implementato.'
ms.assetid: d0fc571f-79f5-448a-8082-6e5f7f48118f
title: Metodo IXml2Dex::WriteXMLPart
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.WriteXMLPart
api_type:
- COM
api_location: ''
ms.openlocfilehash: 957fa74f09a79f94e2e0feb35c418a711c91c1b0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084359"
---
# <a name="ixml2dexwritexmlpart-method"></a><span data-ttu-id="5a0a9-103">Metodo IXml2Dex::WriteXMLPart</span><span class="sxs-lookup"><span data-stu-id="5a0a9-103">IXml2Dex::WriteXMLPart method</span></span>

> [!Note]  
> <span data-ttu-id="5a0a9-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="5a0a9-104">\[Deprecated.</span></span> <span data-ttu-id="5a0a9-105">Questa API potrebbe essere rimossa dalle versioni future di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5a0a9-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5a0a9-106">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="5a0a9-106">Not implemented.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a0a9-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5a0a9-107">Syntax</span></span>


```C++
HRESULT WriteXMLPart(
   IUnknown *pTimeline,
   double   dStart,
   double   dEnd,
   BSTR     FileName
);
```



## <a name="parameters"></a><span data-ttu-id="5a0a9-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5a0a9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a0a9-109">*pTimeline*</span><span class="sxs-lookup"><span data-stu-id="5a0a9-109">*pTimeline*</span></span> 
</dt> <dd>

<span data-ttu-id="5a0a9-110">Riservato.</span><span class="sxs-lookup"><span data-stu-id="5a0a9-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="5a0a9-111">*dStart*</span><span class="sxs-lookup"><span data-stu-id="5a0a9-111">*dStart*</span></span> 
</dt> <dd>

<span data-ttu-id="5a0a9-112">Riservato.</span><span class="sxs-lookup"><span data-stu-id="5a0a9-112">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="5a0a9-113">*dEnd*</span><span class="sxs-lookup"><span data-stu-id="5a0a9-113">*dEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="5a0a9-114">Riservato.</span><span class="sxs-lookup"><span data-stu-id="5a0a9-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="5a0a9-115">*FileName*</span><span class="sxs-lookup"><span data-stu-id="5a0a9-115">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="5a0a9-116">Riservato.</span><span class="sxs-lookup"><span data-stu-id="5a0a9-116">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a0a9-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5a0a9-117">Return value</span></span>

<span data-ttu-id="5a0a9-118">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5a0a9-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5a0a9-119">In caso contrario, restituisce un **codice di errore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="5a0a9-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a0a9-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="5a0a9-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5a0a9-121">Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="5a0a9-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5a0a9-122">Per ottenere Qedit.h, scaricare l'aggiornamento [Microsoft Windows SDK per Windows Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx)</span><span class="sxs-lookup"><span data-stu-id="5a0a9-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5a0a9-123">Qedit.h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="5a0a9-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="5a0a9-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5a0a9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a0a9-125">**Interfaccia IXml2Dex**</span><span class="sxs-lookup"><span data-stu-id="5a0a9-125">**IXml2Dex Interface**</span></span>](ixml2dex.md)
</dt> </dl>

 

 



