---
description: Callback che notifica all'host le informazioni di buffer generico restituite dalla richiesta associata.
MS-HAID: vspixengine.IGenericBufferDataCallback\_ResultCallback\_DWORD\_BYTE\_arr\_BSTR
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IGenericBufferDataCallback:: ResultCallback'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5627A93E-8BE8-4413-BFB4-724AF2DDFEB6
api_name:
- IGenericBufferDataCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: be2d6aa7cd5e844cd5d1297c16de2ebb21c939a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747151"
---
# <a name="span-idvspixengineigenericbufferdatacallback_resultcallback_dword_byte_arr_bstrspanigenericbufferdatacallbackresultcallback-method"></a><span data-ttu-id="16ccf-103"><span id="vspixengine.igenericbufferdatacallback_resultcallback_dword_byte_arr_bstr"></span>Metodo IGenericBufferDataCallback:: ResultCallback</span><span class="sxs-lookup"><span data-stu-id="16ccf-103"><span id="vspixengine.igenericbufferdatacallback_resultcallback_dword_byte_arr_bstr"></span>IGenericBufferDataCallback::ResultCallback method</span></span>

<span data-ttu-id="16ccf-104">Callback che notifica all'host le informazioni di buffer generico restituite dalla richiesta associata.</span><span class="sxs-lookup"><span data-stu-id="16ccf-104">A callback that notifies the host of generic buffer information returned by the assocaited request.</span></span>

## <a name="syntax"></a><span data-ttu-id="16ccf-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="16ccf-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD   size,
   BYTE [] count0_buffer,
   BSTR    type
);
```

## <a name="parameters"></a><span data-ttu-id="16ccf-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="16ccf-106">Parameters</span></span>

<span data-ttu-id="16ccf-107">*dimensioni* </span><span class="sxs-lookup"><span data-stu-id="16ccf-107">*size* </span></span>  
<span data-ttu-id="16ccf-108">Dimensioni in byte del contenuto del buffer.</span><span class="sxs-lookup"><span data-stu-id="16ccf-108">The size of the buffer contents in bytes.</span></span>

<span data-ttu-id="16ccf-109">*\_buffer count0* </span><span class="sxs-lookup"><span data-stu-id="16ccf-109">*count0\_buffer* </span></span>  
<span data-ttu-id="16ccf-110">Contenuto del buffer.</span><span class="sxs-lookup"><span data-stu-id="16ccf-110">The buffer contents.</span></span> <span data-ttu-id="16ccf-111">Nella maggior parte dei casi si tratta di dati XML.</span><span class="sxs-lookup"><span data-stu-id="16ccf-111">In most cases this is XML data.</span></span>

<span data-ttu-id="16ccf-112">*tipo* </span><span class="sxs-lookup"><span data-stu-id="16ccf-112">*type* </span></span>  
<span data-ttu-id="16ccf-113">Stringa COM che indica il tipo di contenuto restituito nel buffer.</span><span class="sxs-lookup"><span data-stu-id="16ccf-113">A COM string that indicates the type of content returned in the buffer.</span></span>

## <a name="return-value"></a><span data-ttu-id="16ccf-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="16ccf-114">Return value</span></span>

<span data-ttu-id="16ccf-115">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="16ccf-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="16ccf-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="16ccf-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="16ccf-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="16ccf-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="16ccf-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="16ccf-118">Header</span></span></p></td><td><span data-ttu-id="16ccf-119">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="16ccf-119">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="16ccf-120"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="16ccf-120"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="16ccf-121">**IGenericBufferDataCallback**</span><span class="sxs-lookup"><span data-stu-id="16ccf-121">**IGenericBufferDataCallback**</span></span>](/windows/desktop/direct3dtools/igenericbufferdatacallback)

 

 
