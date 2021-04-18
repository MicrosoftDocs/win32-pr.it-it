---
description: Callback che notifica all'host le informazioni di mesh scritte dalla richiesta associata.
MS-HAID: vspixengine.IPipeLineStagesCallback3\_MeshFileReadyCallback\_BSTR
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IPipeLineStagesCallback3:: MeshFileReadyCallback'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: BD4719A5-AC07-446A-A7CA-5978F869F66E
api_name:
- IPipeLineStagesCallback3.MeshFileReadyCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7974a9f04acf8e620d792b377fa482dab6de71dd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303953"
---
# <a name="span-idvspixengineipipelinestagescallback3_meshfilereadycallback_bstrspanipipelinestagescallback3meshfilereadycallback-method"></a><span data-ttu-id="57d27-103"><span id="vspixengine.ipipelinestagescallback3_meshfilereadycallback_bstr"></span>Metodo IPipeLineStagesCallback3:: MeshFileReadyCallback</span><span class="sxs-lookup"><span data-stu-id="57d27-103"><span id="vspixengine.ipipelinestagescallback3_meshfilereadycallback_bstr"></span>IPipeLineStagesCallback3::MeshFileReadyCallback method</span></span>

<span data-ttu-id="57d27-104">Callback che notifica all'host le informazioni di mesh scritte dalla richiesta associata.</span><span class="sxs-lookup"><span data-stu-id="57d27-104">A callback that notifies the host of Mesh information written by the associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="57d27-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="57d27-105">Syntax</span></span>


```C++
HRESULT MeshFileReadyCallback(
   BSTR meshFilename
);
```

## <a name="parameters"></a><span data-ttu-id="57d27-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="57d27-106">Parameters</span></span>

<span data-ttu-id="57d27-107">*meshFilename* </span><span class="sxs-lookup"><span data-stu-id="57d27-107">*meshFilename* </span></span>  
<span data-ttu-id="57d27-108">Stringa COM contenente il percorso del file in cui vengono scritti i dati della mesh.</span><span class="sxs-lookup"><span data-stu-id="57d27-108">A COM string containing the pathname of the file where the mesh data is written.</span></span>

## <a name="return-value"></a><span data-ttu-id="57d27-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="57d27-109">Return value</span></span>

<span data-ttu-id="57d27-110">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="57d27-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="57d27-111">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="57d27-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="57d27-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="57d27-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="57d27-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="57d27-113">Header</span></span></p></td><td><span data-ttu-id="57d27-114">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="57d27-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="57d27-115"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="57d27-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="57d27-116">**IPipeLineStagesCallback3**</span><span class="sxs-lookup"><span data-stu-id="57d27-116">**IPipeLineStagesCallback3**</span></span>](/windows/desktop/direct3dtools/ipipelinestagescallback3)

 

 
