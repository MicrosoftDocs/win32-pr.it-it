---
description: Il metodo ScrapIt rimuove il grafico di filtro del motore di rendering e tutti gli oggetti associati.
ms.assetid: b7470947-a661-4c08-8786-9298e5322e58
title: 'Metodo IRenderEngine:: ScrapIt (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.ScrapIt
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7f9febbe20cfd5ab9a6577a6e00989c7d6fc4145
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332746"
---
# <a name="irenderenginescrapit-method"></a><span data-ttu-id="7ad1d-103">Metodo IRenderEngine:: ScrapIt</span><span class="sxs-lookup"><span data-stu-id="7ad1d-103">IRenderEngine::ScrapIt method</span></span>

> [!Note]  
> <span data-ttu-id="7ad1d-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="7ad1d-104">\[Deprecated.</span></span> <span data-ttu-id="7ad1d-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7ad1d-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7ad1d-106">Il `ScrapIt` metodo rimuove il grafico di filtro del motore di rendering e tutti gli oggetti associati.</span><span class="sxs-lookup"><span data-stu-id="7ad1d-106">The `ScrapIt` method discards the render engine's filter graph and all associated objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ad1d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7ad1d-107">Syntax</span></span>


```C++
HRESULT ScrapIt();
```



## <a name="parameters"></a><span data-ttu-id="7ad1d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7ad1d-108">Parameters</span></span>

<span data-ttu-id="7ad1d-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="7ad1d-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7ad1d-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7ad1d-110">Return value</span></span>

<span data-ttu-id="7ad1d-111">Restituisce uno dei seguenti valori **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="7ad1d-111">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="7ad1d-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="7ad1d-112">Return code</span></span>                                                                                            | <span data-ttu-id="7ad1d-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7ad1d-113">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="7ad1d-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7ad1d-114"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="7ad1d-115">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="7ad1d-115">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="7ad1d-116"><dt>**E \_ deve \_ inizializzare il \_ RENDERER**</dt></span><span class="sxs-lookup"><span data-stu-id="7ad1d-116"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl> | <span data-ttu-id="7ad1d-117">Impossibile inizializzare il motore di rendering.</span><span class="sxs-lookup"><span data-stu-id="7ad1d-117">Render engine failed to initialize.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7ad1d-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="7ad1d-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7ad1d-119">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="7ad1d-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="7ad1d-120">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="7ad1d-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="7ad1d-121">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="7ad1d-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7ad1d-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7ad1d-122">Requirements</span></span>



| <span data-ttu-id="7ad1d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ad1d-123">Requirement</span></span> | <span data-ttu-id="7ad1d-124">Valore</span><span class="sxs-lookup"><span data-stu-id="7ad1d-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ad1d-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7ad1d-125">Header</span></span><br/>  | <dl> <span data-ttu-id="7ad1d-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ad1d-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="7ad1d-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="7ad1d-127">Library</span></span><br/> | <dl> <span data-ttu-id="7ad1d-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7ad1d-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ad1d-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7ad1d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ad1d-130">**Interfaccia IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="7ad1d-130">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="7ad1d-131">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="7ad1d-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




