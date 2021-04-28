---
description: 'Metodo IXml2Dex::CreateGraphFromFile: non implementato.'
ms.assetid: b476e0c9-1432-4644-8002-154797a2a594
title: Metodo IXml2Dex::CreateGraphFromFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.CreateGraphFromFile
api_type:
- COM
api_location: ''
ms.openlocfilehash: a79b4115dddb0e15adb4284bbefd245aba088d5f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084419"
---
# <a name="ixml2dexcreategraphfromfile-method"></a><span data-ttu-id="7b5bc-103">Metodo IXml2Dex::CreateGraphFromFile</span><span class="sxs-lookup"><span data-stu-id="7b5bc-103">IXml2Dex::CreateGraphFromFile method</span></span>

> [!Note]  
> <span data-ttu-id="7b5bc-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="7b5bc-104">\[Deprecated.</span></span> <span data-ttu-id="7b5bc-105">Questa API potrebbe essere rimossa dalle versioni future di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7b5bc-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7b5bc-106">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="7b5bc-106">Not implemented.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b5bc-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7b5bc-107">Syntax</span></span>


```C++
HRESULT CreateGraphFromFile(
   IUnknown **ppGraph,
   IUnknown *pTimeline,
   BSTR     FileName
);
```



## <a name="parameters"></a><span data-ttu-id="7b5bc-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7b5bc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b5bc-109">*ppGraph*</span><span class="sxs-lookup"><span data-stu-id="7b5bc-109">*ppGraph*</span></span> 
</dt> <dd>

<span data-ttu-id="7b5bc-110">Riservato.</span><span class="sxs-lookup"><span data-stu-id="7b5bc-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="7b5bc-111">*pTimeline*</span><span class="sxs-lookup"><span data-stu-id="7b5bc-111">*pTimeline*</span></span> 
</dt> <dd>

<span data-ttu-id="7b5bc-112">Riservato.</span><span class="sxs-lookup"><span data-stu-id="7b5bc-112">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="7b5bc-113">*FileName*</span><span class="sxs-lookup"><span data-stu-id="7b5bc-113">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="7b5bc-114">Riservato.</span><span class="sxs-lookup"><span data-stu-id="7b5bc-114">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b5bc-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7b5bc-115">Return value</span></span>

<span data-ttu-id="7b5bc-116">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="7b5bc-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7b5bc-117">In caso contrario, restituisce un **codice di errore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="7b5bc-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b5bc-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="7b5bc-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7b5bc-119">Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="7b5bc-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="7b5bc-120">Per ottenere Qedit.h, scaricare l'aggiornamento [Microsoft Windows SDK per Windows Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx)</span><span class="sxs-lookup"><span data-stu-id="7b5bc-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="7b5bc-121">Qedit.h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="7b5bc-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="7b5bc-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7b5bc-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b5bc-123">**Interfaccia IXml2Dex**</span><span class="sxs-lookup"><span data-stu-id="7b5bc-123">**IXml2Dex Interface**</span></span>](ixml2dex.md)
</dt> </dl>

 

 



