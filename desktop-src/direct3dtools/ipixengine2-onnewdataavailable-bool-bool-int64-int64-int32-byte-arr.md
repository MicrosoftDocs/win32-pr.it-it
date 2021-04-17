---
description: Richieste per indicare che nel log di grafica sono contenuti nuovi dati.
MS-HAID: vspixengine.IPixEngine2\_OnNewDataAvailable\_BOOL\_BOOL\_INT64\_INT64\_INT32\_BYTE\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IPixEngine2:: OnNewDataAvailable'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B99FC54C-9395-4B14-93D5-B6408D655DC3
api_name:
- IPixEngine2.OnNewDataAvailable
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3de880153eec5b41849167f3a87a3f77f31aeffd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521529"
---
# <a name="span-idvspixengineipixengine2_onnewdataavailable_bool_bool_int64_int64_int32_byte_arrspanipixengine2onnewdataavailable-method"></a><span data-ttu-id="52eba-103"><span id="vspixengine.ipixengine2_onnewdataavailable_bool_bool_int64_int64_int32_byte_arr"></span>Metodo IPixEngine2:: OnNewDataAvailable</span><span class="sxs-lookup"><span data-stu-id="52eba-103"><span id="vspixengine.ipixengine2_onnewdataavailable_bool_bool_int64_int64_int32_byte_arr"></span>IPixEngine2::OnNewDataAvailable method</span></span>

<span data-ttu-id="52eba-104">Richieste per indicare che nel log di grafica sono contenuti nuovi dati.</span><span class="sxs-lookup"><span data-stu-id="52eba-104">Requests to indicate that the graphics log has new data inside of it.</span></span>

## <a name="syntax"></a><span data-ttu-id="52eba-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="52eba-105">Syntax</span></span>


```C++
HRESULT OnNewDataAvailable(
   BOOL    fSessionEnd,
   BOOL    fUnloadCurFrame,
   INT64   i64FilePositionStart,
   INT64   i64FilePositionEnd,
   INT32   iObjectTableDataSize,
   BYTE [] count4_pObjectTableData
);
```

## <a name="parameters"></a><span data-ttu-id="52eba-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="52eba-106">Parameters</span></span>

<span data-ttu-id="52eba-107">*fSessionEnd* </span><span class="sxs-lookup"><span data-stu-id="52eba-107">*fSessionEnd* </span></span>  
<span data-ttu-id="52eba-108">true se la sessione è terminata; in caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="52eba-108">true if the session has ended, otherwise false.</span></span>

<span data-ttu-id="52eba-109">*fUnloadCurFrame* </span><span class="sxs-lookup"><span data-stu-id="52eba-109">*fUnloadCurFrame* </span></span>  
<span data-ttu-id="52eba-110">Non usato.</span><span class="sxs-lookup"><span data-stu-id="52eba-110">Not used.</span></span>

<span data-ttu-id="52eba-111">*i64FilePositionStart* </span><span class="sxs-lookup"><span data-stu-id="52eba-111">*i64FilePositionStart* </span></span>  
<span data-ttu-id="52eba-112">Posizione del file, in byte, in cui iniziano i nuovi dati.</span><span class="sxs-lookup"><span data-stu-id="52eba-112">The file position, in bytes, at which the new data begins.</span></span>

<span data-ttu-id="52eba-113">*i64FilePositionEnd* </span><span class="sxs-lookup"><span data-stu-id="52eba-113">*i64FilePositionEnd* </span></span>  
<span data-ttu-id="52eba-114">Posizione del file, in byte, in cui terminano i nuovi dati.</span><span class="sxs-lookup"><span data-stu-id="52eba-114">The file position, in bytes, at which the new data ends.</span></span>

<span data-ttu-id="52eba-115">*iObjectTableDataSize* </span><span class="sxs-lookup"><span data-stu-id="52eba-115">*iObjectTableDataSize* </span></span>  
<span data-ttu-id="52eba-116">Numero di byte contenuti in count4 \_ pObjectTableData.</span><span class="sxs-lookup"><span data-stu-id="52eba-116">The number of bytes contained in count4\_pObjectTableData.</span></span>

<span data-ttu-id="52eba-117">*\_pObjectTableData count4* </span><span class="sxs-lookup"><span data-stu-id="52eba-117">*count4\_pObjectTableData* </span></span>  
<span data-ttu-id="52eba-118">Buffer contenente i dati per la tabella degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="52eba-118">An buffer containing data for the object table.</span></span>

## <a name="return-value"></a><span data-ttu-id="52eba-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="52eba-119">Return value</span></span>

<span data-ttu-id="52eba-120">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="52eba-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="52eba-121">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="52eba-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="52eba-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="52eba-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="52eba-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="52eba-123">Header</span></span></p></td><td><span data-ttu-id="52eba-124">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="52eba-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="52eba-125"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="52eba-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="52eba-126">**IPixEngine2**</span><span class="sxs-lookup"><span data-stu-id="52eba-126">**IPixEngine2**</span></span>](/windows/desktop/direct3dtools/ipixengine2)

 

 
