---
description: Funzione di callback utilizzata per notificare all'host le interfacce supportate.
MS-HAID: vspixengine.IVersionCallback\_VersionTableReady\_GUID\_arr\_UINT
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IVersionCallback:: VersionTableReady'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 58D5E6B4-2CF8-4C13-9A62-93418D46CBCF
api_name:
- IVersionCallback.VersionTableReady
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4f31f8b4619d74f6f491f6be8faf7ddd457ee82c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124692"
---
# <a name="span-idvspixengineiversioncallback_versiontableready_guid_arr_uintspaniversioncallbackversiontableready-method"></a><span data-ttu-id="49166-103"><span id="vspixengine.iversioncallback_versiontableready_guid_arr_uint"></span>Metodo IVersionCallback:: VersionTableReady</span><span class="sxs-lookup"><span data-stu-id="49166-103"><span id="vspixengine.iversioncallback_versiontableready_guid_arr_uint"></span>IVersionCallback::VersionTableReady method</span></span>

<span data-ttu-id="49166-104">Funzione di callback utilizzata per notificare all'host le interfacce supportate.</span><span class="sxs-lookup"><span data-stu-id="49166-104">A callback function used to notify the host of which interfaces are supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="49166-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="49166-105">Syntax</span></span>


```C++
HRESULT VersionTableReady(
   GUID [] count1_interfaceIds,
   UINT    count
);
```

## <a name="parameters"></a><span data-ttu-id="49166-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="49166-106">Parameters</span></span>

<span data-ttu-id="49166-107">*\_interfaceIds count1* </span><span class="sxs-lookup"><span data-stu-id="49166-107">*count1\_interfaceIds* </span></span>  
<span data-ttu-id="49166-108">Matrice contenente i GUID degli ID di interfaccia supportati.</span><span class="sxs-lookup"><span data-stu-id="49166-108">An array containing the GUIDs of supported interface IDs.</span></span>

<span data-ttu-id="49166-109">*conteggio* </span><span class="sxs-lookup"><span data-stu-id="49166-109">*count* </span></span>  
<span data-ttu-id="49166-110">Numero di GUID passati in count1 \_ interfaceIds.</span><span class="sxs-lookup"><span data-stu-id="49166-110">The number of GUIDs passed in count1\_interfaceIds.</span></span>

## <a name="return-value"></a><span data-ttu-id="49166-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="49166-111">Return value</span></span>

<span data-ttu-id="49166-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="49166-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="49166-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="49166-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="49166-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="49166-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="49166-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="49166-115">Header</span></span></p></td><td><span data-ttu-id="49166-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="49166-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="49166-117"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="49166-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="49166-118">**IVersionCallback**</span><span class="sxs-lookup"><span data-stu-id="49166-118">**IVersionCallback**</span></span>](/windows/desktop/direct3dtools/iversioncallback)

 

 
