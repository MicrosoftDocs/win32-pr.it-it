---
description: Salva una trama.
MS-HAID: vspixengine.IPixEngine5\_SaveTextureAsync\_UINT\_BSTR\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IPixEngine5:: SaveTextureAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6F08F49E-6FFD-4A9B-86F5-8CB499947F57
api_name:
- IPixEngine5.SaveTextureAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2590f793d0ba05af1ccf9e10ba04fa8b6aa2421b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482636"
---
# <a name="span-idvspixengineipixengine5_savetextureasync_uint_bstr_ipixengine5callbacks_ptr_dword_dwordspanipixengine5savetextureasync-method"></a><span data-ttu-id="3046d-103"><span id="vspixengine.ipixengine5_savetextureasync_uint_bstr_ipixengine5callbacks_ptr_dword_dword"></span>Metodo IPixEngine5:: SaveTextureAsync</span><span class="sxs-lookup"><span data-stu-id="3046d-103"><span id="vspixengine.ipixengine5_savetextureasync_uint_bstr_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5::SaveTextureAsync method</span></span>

<span data-ttu-id="3046d-104">Salva una trama.</span><span class="sxs-lookup"><span data-stu-id="3046d-104">Saves a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="3046d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3046d-105">Syntax</span></span>


```C++
HRESULT SaveTextureAsync(
   UINT                  textureId,
   BSTR                  fileName,
   IPixEngine5Callbacks* callbacks,
   DWORD                 requestCookie,
   DWORD                 progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="3046d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3046d-106">Parameters</span></span>

<span data-ttu-id="3046d-107">*textureId* </span><span class="sxs-lookup"><span data-stu-id="3046d-107">*textureId* </span></span>  
<span data-ttu-id="3046d-108">ID della trama da salvare.</span><span class="sxs-lookup"><span data-stu-id="3046d-108">The ID of the texture to save.</span></span>

<span data-ttu-id="3046d-109">*fileName* </span><span class="sxs-lookup"><span data-stu-id="3046d-109">*fileName* </span></span>  
<span data-ttu-id="3046d-110">Stringa COM contenente il percorso della trama salvata.</span><span class="sxs-lookup"><span data-stu-id="3046d-110">A COM string containing the pathname of the saved texture.</span></span>

<span data-ttu-id="3046d-111">*callback* </span><span class="sxs-lookup"><span data-stu-id="3046d-111">*callbacks* </span></span>  
<span data-ttu-id="3046d-112">Indirizzo di un oggetto che fornisce l'interfaccia di callback IPixEngine5.</span><span class="sxs-lookup"><span data-stu-id="3046d-112">The address of an object that provides the IPixEngine5 callbacks interface.</span></span>

<span data-ttu-id="3046d-113">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="3046d-113">*requestCookie* </span></span>  
<span data-ttu-id="3046d-114">Un cookie che identifica in modo univoco la richiesta e può essere usato per segnalare l'annullamento.</span><span class="sxs-lookup"><span data-stu-id="3046d-114">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="3046d-115">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="3046d-115">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="3046d-116">Non usato.</span><span class="sxs-lookup"><span data-stu-id="3046d-116">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="3046d-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3046d-117">Return value</span></span>

<span data-ttu-id="3046d-118">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3046d-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3046d-119">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3046d-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3046d-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3046d-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="3046d-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3046d-121">Header</span></span></p></td><td><span data-ttu-id="3046d-122">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="3046d-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="3046d-123"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="3046d-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="3046d-124">**IPixEngine5**</span><span class="sxs-lookup"><span data-stu-id="3046d-124">**IPixEngine5**</span></span>](/windows/desktop/direct3dtools/ipixengine5)

 

 
