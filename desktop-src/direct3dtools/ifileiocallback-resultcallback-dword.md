---
description: Funzione di callback utilizzata per notificare l'host degli errori durante l'acquisizione o la riproduzione.
MS-HAID: vspixengine.IFileIOCallback\_ResultCallback\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IFileIOCallback:: ResultCallback'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E4418A63-47C6-4F12-94FA-0F1B5465FE84
api_name:
- IFileIOCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 751c4d0b57165e148002218ae2151aaba69e48f8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124620"
---
# <a name="span-idvspixengineifileiocallback_resultcallback_dwordspanifileiocallbackresultcallback-method"></a><span data-ttu-id="1a6fa-103"><span id="vspixengine.ifileiocallback_resultcallback_dword"></span>Metodo IFileIOCallback:: ResultCallback</span><span class="sxs-lookup"><span data-stu-id="1a6fa-103"><span id="vspixengine.ifileiocallback_resultcallback_dword"></span>IFileIOCallback::ResultCallback method</span></span>

<span data-ttu-id="1a6fa-104">Funzione di callback utilizzata per notificare l'host degli errori durante l'acquisizione o la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="1a6fa-104">A callback function used to notify the host of errors while during capture or playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a6fa-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a6fa-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD resultState
);
```

## <a name="parameters"></a><span data-ttu-id="1a6fa-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1a6fa-106">Parameters</span></span>

<span data-ttu-id="1a6fa-107">*resultState* </span><span class="sxs-lookup"><span data-stu-id="1a6fa-107">*resultState* </span></span>  
<span data-ttu-id="1a6fa-108">Indica il tipo di errore rilevato.</span><span class="sxs-lookup"><span data-stu-id="1a6fa-108">Indicates the kind of error encountered.</span></span>

## <a name="return-value"></a><span data-ttu-id="1a6fa-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1a6fa-109">Return value</span></span>

<span data-ttu-id="1a6fa-110">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1a6fa-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1a6fa-111">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1a6fa-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a6fa-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1a6fa-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="1a6fa-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1a6fa-113">Header</span></span></p></td><td><span data-ttu-id="1a6fa-114">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="1a6fa-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="1a6fa-115"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="1a6fa-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="1a6fa-116">**IFileIOCallback**</span><span class="sxs-lookup"><span data-stu-id="1a6fa-116">**IFileIOCallback**</span></span>](/windows/desktop/direct3dtools/ifileiocallback)

 

 
