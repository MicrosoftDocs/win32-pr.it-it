---
description: Callback che notifica all'host le informazioni instructrion restituite dalla richiesta associata.
MS-HAID: vspixengine.IDebugShaderCallback\_ResultInstructions\_DWORD\_BYTE\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IDebugShaderCallback:: ResultInstructions'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 52440CE4-561C-4808-BE6A-B25A84BA5729
api_name:
- IDebugShaderCallback.ResultInstructions
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 63dfd0e3b2b4ec7bd765e5fc0c85835f2a3ce102
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481949"
---
# <a name="span-idvspixengineidebugshadercallback_resultinstructions_dword_byte_arrspanidebugshadercallbackresultinstructions-method"></a><span data-ttu-id="40aa9-103"><span id="vspixengine.idebugshadercallback_resultinstructions_dword_byte_arr"></span>Metodo IDebugShaderCallback:: ResultInstructions</span><span class="sxs-lookup"><span data-stu-id="40aa9-103"><span id="vspixengine.idebugshadercallback_resultinstructions_dword_byte_arr"></span>IDebugShaderCallback::ResultInstructions method</span></span>

<span data-ttu-id="40aa9-104">Callback che notifica all'host le informazioni instructrion restituite dalla richiesta associata.</span><span class="sxs-lookup"><span data-stu-id="40aa9-104">A callback that notifies the host of instructrion information returned by the associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="40aa9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="40aa9-105">Syntax</span></span>


```C++
HRESULT ResultInstructions(
   DWORD   instructionStreamSize,
   BYTE [] count0_instructionStream
);
```

## <a name="parameters"></a><span data-ttu-id="40aa9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="40aa9-106">Parameters</span></span>

<span data-ttu-id="40aa9-107">*instructionStreamSize* </span><span class="sxs-lookup"><span data-stu-id="40aa9-107">*instructionStreamSize* </span></span>  
<span data-ttu-id="40aa9-108">Numero di istruzioni.</span><span class="sxs-lookup"><span data-stu-id="40aa9-108">The number of instructions.</span></span>

<span data-ttu-id="40aa9-109">*\_instructionStream count0* </span><span class="sxs-lookup"><span data-stu-id="40aa9-109">*count0\_instructionStream* </span></span>  
<span data-ttu-id="40aa9-110">Istruzioni.</span><span class="sxs-lookup"><span data-stu-id="40aa9-110">The instructions.</span></span>

## <a name="return-value"></a><span data-ttu-id="40aa9-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="40aa9-111">Return value</span></span>

<span data-ttu-id="40aa9-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="40aa9-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="40aa9-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="40aa9-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="40aa9-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="40aa9-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="40aa9-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="40aa9-115">Header</span></span></p></td><td><span data-ttu-id="40aa9-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="40aa9-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="40aa9-117"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="40aa9-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="40aa9-118">**IDebugShaderCallback**</span><span class="sxs-lookup"><span data-stu-id="40aa9-118">**IDebugShaderCallback**</span></span>](/windows/desktop/direct3dtools/idebugshadercallback)

 

 
