---
description: Richiesta di aggiornamento dello stato iniziale di un oggetto. ad esempio, una trama o uno shader.
MS-HAID: vspixengine.IUpdateObject\_UpdateObject\_UINT\_DWORD\_BYTE\_arr\_IUpdateObjectCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IUpdateObject:: UpdateObject'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 824AB599-7377-4F77-8FC8-41E17ED57A79
api_name:
- IUpdateObject.UpdateObject
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9b04918878de15a2b9a5b004d3dff252ab3ddc9d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481997"
---
# <a name="span-idvspixengineiupdateobject_updateobject_uint_dword_byte_arr_iupdateobjectcallback_ptrspaniupdateobjectupdateobject-method"></a><span data-ttu-id="9b930-103"><span id="vspixengine.iupdateobject_updateobject_uint_dword_byte_arr_iupdateobjectcallback_ptr"></span>Metodo IUpdateObject:: UpdateObject</span><span class="sxs-lookup"><span data-stu-id="9b930-103"><span id="vspixengine.iupdateobject_updateobject_uint_dword_byte_arr_iupdateobjectcallback_ptr"></span>IUpdateObject::UpdateObject method</span></span>

<span data-ttu-id="9b930-104">Richiesta di aggiornamento dello stato iniziale di un oggetto. ad esempio, una trama o uno shader.</span><span class="sxs-lookup"><span data-stu-id="9b930-104">A request to update the initial state of an object; for example, a texture or shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b930-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9b930-105">Syntax</span></span>


```C++
HRESULT UpdateObject(
   UINT                    objectAddress,
   DWORD                   size,
   BYTE []                 count1_buffer,
   IUpdateObjectCallback * pCallback
);
```

## <a name="parameters"></a><span data-ttu-id="9b930-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9b930-106">Parameters</span></span>

<span data-ttu-id="9b930-107">*objectAddress* </span><span class="sxs-lookup"><span data-stu-id="9b930-107">*objectAddress* </span></span>  
<span data-ttu-id="9b930-108">ID dell'oggetto da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="9b930-108">The ID of the object to be updated.</span></span>

<span data-ttu-id="9b930-109">*dimensioni* </span><span class="sxs-lookup"><span data-stu-id="9b930-109">*size* </span></span>  
<span data-ttu-id="9b930-110">Dimensioni in byte del payload dell'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="9b930-110">The size of the update payload in bytes.</span></span>

<span data-ttu-id="9b930-111">*\_buffer count1* </span><span class="sxs-lookup"><span data-stu-id="9b930-111">*count1\_buffer* </span></span>  
<span data-ttu-id="9b930-112">Payload dell'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="9b930-112">The update payload.</span></span>

<span data-ttu-id="9b930-113">*pCallback* </span><span class="sxs-lookup"><span data-stu-id="9b930-113">*pCallback* </span></span>  
<span data-ttu-id="9b930-114">Indirizzo di una funzione utilizzata per notificare all'host che l'oggetto è stato aggiornato.</span><span class="sxs-lookup"><span data-stu-id="9b930-114">The address of a function used to notify the host that the object was updated.</span></span>

## <a name="return-value"></a><span data-ttu-id="9b930-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9b930-115">Return value</span></span>

<span data-ttu-id="9b930-116">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9b930-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9b930-117">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9b930-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b930-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9b930-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="9b930-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9b930-119">Header</span></span></p></td><td><span data-ttu-id="9b930-120">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="9b930-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="9b930-121"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="9b930-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="9b930-122">**IUpdateObject**</span><span class="sxs-lookup"><span data-stu-id="9b930-122">**IUpdateObject**</span></span>](/windows/desktop/direct3dtools/iupdateobject)

 

 
