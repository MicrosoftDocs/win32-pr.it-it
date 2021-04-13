---
description: Libera una trama e notifica l'host in modo asincrono.
MS-HAID: vspixengine.IPixEngine5\_FreeTextureAsync\_UINT\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IPixEngine5:: FreeTextureAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9A2D46D4-AA09-4E50-8109-774CE7F538E7
api_name:
- IPixEngine5.FreeTextureAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: aed7d29653b9da6f39b1ef6ec4e600c1857744f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482573"
---
# <a name="span-idvspixengineipixengine5_freetextureasync_uint_ipixengine5callbacks_ptr_dword_dwordspanipixengine5freetextureasync-method"></a><span data-ttu-id="22329-103"><span id="vspixengine.ipixengine5_freetextureasync_uint_ipixengine5callbacks_ptr_dword_dword"></span>Metodo IPixEngine5:: FreeTextureAsync</span><span class="sxs-lookup"><span data-stu-id="22329-103"><span id="vspixengine.ipixengine5_freetextureasync_uint_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5::FreeTextureAsync method</span></span>

<span data-ttu-id="22329-104">Libera una trama e notifica l'host in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="22329-104">Frees a texture and notifies the host asynchronously.</span></span>

## <a name="syntax"></a><span data-ttu-id="22329-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="22329-105">Syntax</span></span>


```C++
HRESULT FreeTextureAsync(
   UINT                  textureId,
   IPixEngine5Callbacks* callbacks,
   DWORD                 requestCookie,
   DWORD                 progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="22329-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="22329-106">Parameters</span></span>

<span data-ttu-id="22329-107">*textureId* </span><span class="sxs-lookup"><span data-stu-id="22329-107">*textureId* </span></span>  
<span data-ttu-id="22329-108">ID della trama da liberare.</span><span class="sxs-lookup"><span data-stu-id="22329-108">The ID of the texture to free..</span></span>

<span data-ttu-id="22329-109">*callback* </span><span class="sxs-lookup"><span data-stu-id="22329-109">*callbacks* </span></span>  
<span data-ttu-id="22329-110">Indirizzo di un oggetto che fornisce l'interfaccia di callback IPixEngine5.</span><span class="sxs-lookup"><span data-stu-id="22329-110">The address of an object that provides the IPixEngine5 callbacks interface.</span></span>

<span data-ttu-id="22329-111">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="22329-111">*requestCookie* </span></span>  
<span data-ttu-id="22329-112">Un cookie che idenfies in modo univoco la richiesta e può essere usato per segnalare l'annullamento.</span><span class="sxs-lookup"><span data-stu-id="22329-112">A cookie that uniquely idenfies the request, and can be used to signal for it to be canceled.</span></span>

<span data-ttu-id="22329-113">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="22329-113">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="22329-114">Non usato.</span><span class="sxs-lookup"><span data-stu-id="22329-114">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="22329-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="22329-115">Return value</span></span>

<span data-ttu-id="22329-116">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="22329-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="22329-117">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="22329-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="22329-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="22329-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="22329-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="22329-119">Header</span></span></p></td><td><span data-ttu-id="22329-120">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="22329-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="22329-121"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="22329-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="22329-122">**IPixEngine5**</span><span class="sxs-lookup"><span data-stu-id="22329-122">**IPixEngine5**</span></span>](/windows/desktop/direct3dtools/ipixengine5)

 

 
