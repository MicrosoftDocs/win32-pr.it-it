---
description: L'interfaccia IAMErrorLog fornisce un metodo di callback per la registrazione degli errori in DirectShow editing Services (DES). DES non implementa questa interfaccia.
ms.assetid: d5366072-2de7-437c-b198-cbc4d8623c45
title: Interfaccia IAMErrorLog (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMErrorLog
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 48a1515ebf3e7c829a3e23772f1f84ee76c36ae0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326821"
---
# <a name="iamerrorlog-interface"></a><span data-ttu-id="16e6d-103">Interfaccia IAMErrorLog</span><span class="sxs-lookup"><span data-stu-id="16e6d-103">IAMErrorLog interface</span></span>

> [!Note]  
> <span data-ttu-id="16e6d-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="16e6d-104">\[Deprecated.</span></span> <span data-ttu-id="16e6d-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="16e6d-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="16e6d-106">L' `IAMErrorLog` interfaccia fornisce un metodo di callback per la registrazione degli errori in [DirectShow editing Services](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="16e6d-106">The `IAMErrorLog` interface provides a callback method for error logging in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span>

<span data-ttu-id="16e6d-107">DES non implementa questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="16e6d-107">DES does not implement this interface.</span></span> <span data-ttu-id="16e6d-108">Per eseguire la registrazione degli errori, implementare questa interfaccia nell'applicazione e chiamare [**IAMSetErrorLog::p \_ log**](iamseterrorlog-put-errorlog.md) degli errori UT nella sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="16e6d-108">To perform error logging, implement this interface in your application and call [**IAMSetErrorLog::put\_ErrorLog**](iamseterrorlog-put-errorlog.md) on the timeline.</span></span> <span data-ttu-id="16e6d-109">Se si verifica un errore quando si esegue il rendering del progetto, DES chiamerà il metodo [**IAMErrorLog:: LogError**](iamerrorlog-logerror.md) implementato dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="16e6d-109">If an error occurs when you render the project, DES will call the [**IAMErrorLog::LogError**](iamerrorlog-logerror.md) method implemented by your application.</span></span>

<span data-ttu-id="16e6d-110">DES registra gli errori solo quando si esegue il rendering di un progetto usando l'interfaccia [**IRenderEngine**](irenderengine.md) .</span><span class="sxs-lookup"><span data-stu-id="16e6d-110">DES logs errors only when you render a project using the [**IRenderEngine**](irenderengine.md) interface.</span></span> <span data-ttu-id="16e6d-111">Se, ad esempio, si salva un progetto come un grafico del filtro DirectShow (formato. GRF) e si riproduce il file del grafo, non viene eseguita alcuna registrazione degli errori.</span><span class="sxs-lookup"><span data-stu-id="16e6d-111">For example, if you save a project as a DirectShow filter graph (.grf format) and play the graph file, there is no error logging.</span></span> <span data-ttu-id="16e6d-112">Per ulteriori informazioni sull'utilizzo di questa interfaccia, vedere [registrazione degli errori](logging-errors.md).</span><span class="sxs-lookup"><span data-stu-id="16e6d-112">For more information on using this interface, see [Logging Errors](logging-errors.md).</span></span>

## <a name="members"></a><span data-ttu-id="16e6d-113">Membri</span><span class="sxs-lookup"><span data-stu-id="16e6d-113">Members</span></span>

<span data-ttu-id="16e6d-114">L'interfaccia **IAMErrorLog** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="16e6d-114">The **IAMErrorLog** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="16e6d-115">**IAMErrorLog** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="16e6d-115">**IAMErrorLog** also has these types of members:</span></span>

-   [<span data-ttu-id="16e6d-116">Metodi</span><span class="sxs-lookup"><span data-stu-id="16e6d-116">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="16e6d-117">Metodi</span><span class="sxs-lookup"><span data-stu-id="16e6d-117">Methods</span></span>

<span data-ttu-id="16e6d-118">L'interfaccia **IAMErrorLog** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="16e6d-118">The **IAMErrorLog** interface has these methods.</span></span>



| <span data-ttu-id="16e6d-119">Metodo</span><span class="sxs-lookup"><span data-stu-id="16e6d-119">Method</span></span>                                   | <span data-ttu-id="16e6d-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16e6d-120">Description</span></span>               |
|:-----------------------------------------|:--------------------------|
| [<span data-ttu-id="16e6d-121">**LogError**</span><span class="sxs-lookup"><span data-stu-id="16e6d-121">**LogError**</span></span>](iamerrorlog-logerror.md) | <span data-ttu-id="16e6d-122">Registra un errore.</span><span class="sxs-lookup"><span data-stu-id="16e6d-122">Logs an error.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="16e6d-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="16e6d-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="16e6d-124">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="16e6d-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="16e6d-125">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="16e6d-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="16e6d-126">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="16e6d-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="16e6d-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="16e6d-127">Requirements</span></span>



| <span data-ttu-id="16e6d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="16e6d-128">Requirement</span></span> | <span data-ttu-id="16e6d-129">Valore</span><span class="sxs-lookup"><span data-stu-id="16e6d-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="16e6d-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="16e6d-130">Header</span></span><br/>  | <dl> <span data-ttu-id="16e6d-131"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="16e6d-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="16e6d-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="16e6d-132">Library</span></span><br/> | <dl> <span data-ttu-id="16e6d-133"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="16e6d-133"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
