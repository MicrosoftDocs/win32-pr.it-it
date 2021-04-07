---
description: Funzione di callback utilizzata per notificare all'host le informazioni sulla tabella degli oggetti.
MS-HAID: vspixengine.IObjectTableCallback\_ResultCallback\_DWORD\_DWORD\_DWORD\_VARIANT\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IObjectTableCallback:: ResultCallback'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: AAD02864-AE08-406B-A0E9-2228DC9A73E7
api_name:
- IObjectTableCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 66247dddbf0926b420faa998461393397a4717b7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747394"
---
# <a name="span-idvspixengineiobjecttablecallback_resultcallback_dword_dword_dword_variant_arrspaniobjecttablecallbackresultcallback-method"></a><span data-ttu-id="5b491-103"><span id="vspixengine.iobjecttablecallback_resultcallback_dword_dword_dword_variant_arr"></span>Metodo IObjectTableCallback:: ResultCallback</span><span class="sxs-lookup"><span data-stu-id="5b491-103"><span id="vspixengine.iobjecttablecallback_resultcallback_dword_dword_dword_variant_arr"></span>IObjectTableCallback::ResultCallback method</span></span>

<span data-ttu-id="5b491-104">Funzione di callback utilizzata per notificare all'host le informazioni sulla tabella degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="5b491-104">A callback function used to notify the host of object table information.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b491-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5b491-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD      numElements,
   DWORD      numRows,
   DWORD      numColumns,
   VARIANT [] count0_pRowData
);
```

## <a name="parameters"></a><span data-ttu-id="5b491-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5b491-106">Parameters</span></span>

<span data-ttu-id="5b491-107">*numElements* </span><span class="sxs-lookup"><span data-stu-id="5b491-107">*numElements* </span></span>  
<span data-ttu-id="5b491-108">Numero totale di campi in tutte le colonne di tutti gli oggetti.</span><span class="sxs-lookup"><span data-stu-id="5b491-108">The total number of fields in all columns of all objects.</span></span>

<span data-ttu-id="5b491-109">*numRows* </span><span class="sxs-lookup"><span data-stu-id="5b491-109">*numRows* </span></span>  
<span data-ttu-id="5b491-110">Numero di oggetti trasferiti.</span><span class="sxs-lookup"><span data-stu-id="5b491-110">The number of objects being transferred.</span></span>

<span data-ttu-id="5b491-111">*numColumns* </span><span class="sxs-lookup"><span data-stu-id="5b491-111">*numColumns* </span></span>  
<span data-ttu-id="5b491-112">Numero di colonne (campi) di informazioni da trasferire per ogni oggetto.</span><span class="sxs-lookup"><span data-stu-id="5b491-112">The number of columns (fields) of information being transferred for each object.</span></span>

<span data-ttu-id="5b491-113">*\_pRowData count0* </span><span class="sxs-lookup"><span data-stu-id="5b491-113">*count0\_pRowData* </span></span>  
<span data-ttu-id="5b491-114">Informazioni sugli oggetti; un elemento per ogni campo di ciascun oggetto.</span><span class="sxs-lookup"><span data-stu-id="5b491-114">Information about the objects; one item for each field of each object.</span></span>

## <a name="return-value"></a><span data-ttu-id="5b491-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5b491-115">Return value</span></span>

<span data-ttu-id="5b491-116">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5b491-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5b491-117">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5b491-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b491-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5b491-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="5b491-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5b491-119">Header</span></span></p></td><td><span data-ttu-id="5b491-120">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="5b491-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="5b491-121"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="5b491-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="5b491-122">**IObjectTableCallback**</span><span class="sxs-lookup"><span data-stu-id="5b491-122">**IObjectTableCallback**</span></span>](/windows/desktop/direct3dtools/iobjecttablecallback)

 

 
