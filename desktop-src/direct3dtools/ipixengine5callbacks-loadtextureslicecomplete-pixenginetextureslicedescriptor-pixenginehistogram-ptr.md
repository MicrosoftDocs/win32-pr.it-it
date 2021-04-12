---
description: Funzione di callback utilizzata per notificare all'host quando è stato completato il caricamento di una sezione di trama.
MS-HAID: vspixengine.IPixEngine5Callbacks\_LoadTextureSliceComplete\_PixEngineTextureSliceDescriptor\_PixEngineHistogram\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IPixEngine5Callbacks:: LoadTextureSliceComplete'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CEEAB77F-0856-4DEC-991A-7CEB921C84BB
api_name:
- IPixEngine5Callbacks.LoadTextureSliceComplete
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 674288841ea08ad38c519e88abac4c64a1f1ca7d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482396"
---
# <a name="span-idvspixengineipixengine5callbacks_loadtextureslicecomplete_pixenginetextureslicedescriptor_pixenginehistogram_ptrspanipixengine5callbacksloadtextureslicecomplete-method"></a><span data-ttu-id="5a386-103"><span id="vspixengine.ipixengine5callbacks_loadtextureslicecomplete_pixenginetextureslicedescriptor_pixenginehistogram_ptr"></span>Metodo IPixEngine5Callbacks:: LoadTextureSliceComplete</span><span class="sxs-lookup"><span data-stu-id="5a386-103"><span id="vspixengine.ipixengine5callbacks_loadtextureslicecomplete_pixenginetextureslicedescriptor_pixenginehistogram_ptr"></span>IPixEngine5Callbacks::LoadTextureSliceComplete method</span></span>

<span data-ttu-id="5a386-104">Funzione di callback utilizzata per notificare all'host quando è stato completato il caricamento di una sezione di trama.</span><span class="sxs-lookup"><span data-stu-id="5a386-104">A callback function used to notify the host when a texture slice load has been completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a386-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5a386-105">Syntax</span></span>


```C++
HRESULT LoadTextureSliceComplete(
   PixEngineTextureSliceDescriptor sliceDesc,
   PixEngineHistogram*             histogram
);
```

## <a name="parameters"></a><span data-ttu-id="5a386-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5a386-106">Parameters</span></span>

<span data-ttu-id="5a386-107">*sliceDesc* </span><span class="sxs-lookup"><span data-stu-id="5a386-107">*sliceDesc* </span></span>  
<span data-ttu-id="5a386-108">Descrittore della sezione caricata.</span><span class="sxs-lookup"><span data-stu-id="5a386-108">A descriptor of the loaded slice.</span></span>

<span data-ttu-id="5a386-109">*istogramma* </span><span class="sxs-lookup"><span data-stu-id="5a386-109">*histogram* </span></span>  
<span data-ttu-id="5a386-110">Indirizzo dei dati dell'istogramma per la sezione caricata.</span><span class="sxs-lookup"><span data-stu-id="5a386-110">The address of histogram data for the loaded slice.</span></span>

## <a name="return-value"></a><span data-ttu-id="5a386-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5a386-111">Return value</span></span>

<span data-ttu-id="5a386-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5a386-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5a386-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5a386-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a386-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5a386-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="5a386-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5a386-115">Header</span></span></p></td><td><span data-ttu-id="5a386-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="5a386-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="5a386-117"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="5a386-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="5a386-118">**IPixEngine5Callbacks**</span><span class="sxs-lookup"><span data-stu-id="5a386-118">**IPixEngine5Callbacks**</span></span>](/windows/desktop/direct3dtools/ipixengine5callbacks)

 

 
