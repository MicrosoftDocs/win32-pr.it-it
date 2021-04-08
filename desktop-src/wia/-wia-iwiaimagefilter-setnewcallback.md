---
description: Imposta un nuovo callback dell'applicazione per il filtro di elaborazione dell'immagine da utilizzare per l'invio delle chiamate.
ms.assetid: 25b86f1d-96c8-4150-9147-13be9b1dd50c
title: 'Metodo IWiaImageFilter:: SetNewCallback (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter.SetNewCallback
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 16325d854f7b17c62e6fb8254819078de64977f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752831"
---
# <a name="iwiaimagefiltersetnewcallback-method"></a><span data-ttu-id="0d460-103">Metodo IWiaImageFilter:: SetNewCallback</span><span class="sxs-lookup"><span data-stu-id="0d460-103">IWiaImageFilter::SetNewCallback method</span></span>

<span data-ttu-id="0d460-104">Imposta un nuovo callback dell'applicazione per il filtro di elaborazione dell'immagine da utilizzare per l'invio delle chiamate.</span><span class="sxs-lookup"><span data-stu-id="0d460-104">Sets a new application callback for the image processing filter to use for forwarding calls.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d460-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0d460-105">Syntax</span></span>


```C++
HRESULT SetNewCallback(
  [in] IWiaTransferCallback pWiaTransferCallback
);
```



## <a name="parameters"></a><span data-ttu-id="0d460-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0d460-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d460-107">*pWiaTransferCallback* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0d460-107">*pWiaTransferCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d460-108">Tipo: **[ **IWiaTransferCallback**](-wia-iwiatransfercallback.md)**</span><span class="sxs-lookup"><span data-stu-id="0d460-108">Type: **[**IWiaTransferCallback**](-wia-iwiatransfercallback.md)**</span></span>

<span data-ttu-id="0d460-109">Specifica un puntatore all'interfaccia [**IWiaTransferCallback**](-wia-iwiatransfercallback.md) dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0d460-109">Specifies a pointer to the application's [**IWiaTransferCallback**](-wia-iwiatransfercallback.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d460-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0d460-110">Return value</span></span>

<span data-ttu-id="0d460-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="0d460-111">Type: **HRESULT**</span></span>

<span data-ttu-id="0d460-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0d460-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0d460-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0d460-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d460-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="0d460-114">Remarks</span></span>

<span data-ttu-id="0d460-115">Non chiamare questo metodo direttamente dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0d460-115">Do not call this method directly from your application.</span></span>

<span data-ttu-id="0d460-116">Il filtro di elaborazione delle immagini è necessario per rilasciare l'interfaccia di callback dell'applicazione precedentemente archiviata prima di impostare il nuovo callback.</span><span class="sxs-lookup"><span data-stu-id="0d460-116">The image processing filter is required to release the previously stored application callback interface before setting the new callback.</span></span>

<span data-ttu-id="0d460-117">Se *pWiaTransferCallback* è **null**, il filtro di elaborazione dell'immagine deve semplicemente rilasciare il callback precedente dell'applicazione e restituire S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0d460-117">If *pWiaTransferCallback* is **NULL**, the image processing filter should simply release the old application callback and return S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d460-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0d460-118">Requirements</span></span>



| <span data-ttu-id="0d460-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d460-119">Requirement</span></span> | <span data-ttu-id="0d460-120">Valore</span><span class="sxs-lookup"><span data-stu-id="0d460-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0d460-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d460-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0d460-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0d460-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0d460-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d460-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0d460-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0d460-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0d460-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0d460-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d460-126"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d460-126"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="0d460-127">IDL</span><span class="sxs-lookup"><span data-stu-id="0d460-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0d460-128"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0d460-128"><dt>Wia.idl</dt></span></span> </dl> |



 

 




