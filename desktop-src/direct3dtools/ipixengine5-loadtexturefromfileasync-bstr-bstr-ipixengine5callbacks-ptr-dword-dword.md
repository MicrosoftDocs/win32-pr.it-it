---
description: Carica una trama da un file e notifica l'host in modo asincrono quando viene completato.
MS-HAID: vspixengine.IPixEngine5\_LoadTextureFromFileAsync\_BSTR\_BSTR\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IPixEngine5:: LoadTextureFromFileAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: DF10C209-B6B5-4692-81D7-7FD59CE49F56
api_name:
- IPixEngine5.LoadTextureFromFileAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bef4e4e5117680f7c18f13cc99f801c8e8b8bdfd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125379"
---
# <a name="span-idvspixengineipixengine5_loadtexturefromfileasync_bstr_bstr_ipixengine5callbacks_ptr_dword_dwordspanipixengine5loadtexturefromfileasync-method"></a><span data-ttu-id="42ca6-103"><span id="vspixengine.ipixengine5_loadtexturefromfileasync_bstr_bstr_ipixengine5callbacks_ptr_dword_dword"></span>Metodo IPixEngine5:: LoadTextureFromFileAsync</span><span class="sxs-lookup"><span data-stu-id="42ca6-103"><span id="vspixengine.ipixengine5_loadtexturefromfileasync_bstr_bstr_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5::LoadTextureFromFileAsync method</span></span>

<span data-ttu-id="42ca6-104">Carica una trama da un file e notifica l'host in modo asincrono quando viene completato.</span><span class="sxs-lookup"><span data-stu-id="42ca6-104">Loads a texture from a file and notifies the host asynchronously when it completes.</span></span>

## <a name="syntax"></a><span data-ttu-id="42ca6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="42ca6-105">Syntax</span></span>


```C++
HRESULT LoadTextureFromFileAsync(
   BSTR                  fileName,
   BSTR                  histogramDataFileName,
   IPixEngine5Callbacks* callbacks,
   DWORD                 requestCookie,
   DWORD                 progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="42ca6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="42ca6-106">Parameters</span></span>

<span data-ttu-id="42ca6-107">*fileName* </span><span class="sxs-lookup"><span data-stu-id="42ca6-107">*fileName* </span></span>  
<span data-ttu-id="42ca6-108">Stringa COM contenente il nome del file di trama.</span><span class="sxs-lookup"><span data-stu-id="42ca6-108">A COM string containing the name of the texture file.</span></span>

<span data-ttu-id="42ca6-109">*histogramDataFileName* </span><span class="sxs-lookup"><span data-stu-id="42ca6-109">*histogramDataFileName* </span></span>  
<span data-ttu-id="42ca6-110">Stringa COM contenente il nome del file di dati dell'istogramma associato alla trama.</span><span class="sxs-lookup"><span data-stu-id="42ca6-110">A COM string containing the name of the histogram data file associated with the texture.</span></span>

<span data-ttu-id="42ca6-111">*callback* </span><span class="sxs-lookup"><span data-stu-id="42ca6-111">*callbacks* </span></span>  
<span data-ttu-id="42ca6-112">Indirizzo di un oggetto che fornisce l'interfaccia di callback IPixEngine5.</span><span class="sxs-lookup"><span data-stu-id="42ca6-112">The address of an object that provides the IPixEngine5 callbacks interface.</span></span>

<span data-ttu-id="42ca6-113">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="42ca6-113">*requestCookie* </span></span>  
<span data-ttu-id="42ca6-114">Un cookie che idenfies in modo univoco la richiesta e può essere usato per segnalare l'annullamento.</span><span class="sxs-lookup"><span data-stu-id="42ca6-114">A cookie that uniquely idenfies the request, and can be used to signal for it to be canceled.</span></span>

<span data-ttu-id="42ca6-115">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="42ca6-115">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="42ca6-116">Non usato.</span><span class="sxs-lookup"><span data-stu-id="42ca6-116">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="42ca6-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="42ca6-117">Return value</span></span>

<span data-ttu-id="42ca6-118">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="42ca6-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="42ca6-119">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="42ca6-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="42ca6-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="42ca6-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="42ca6-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="42ca6-121">Header</span></span></p></td><td><span data-ttu-id="42ca6-122">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="42ca6-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="42ca6-123"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="42ca6-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="42ca6-124">**IPixEngine5**</span><span class="sxs-lookup"><span data-stu-id="42ca6-124">**IPixEngine5**</span></span>](/windows/desktop/direct3dtools/ipixengine5)

 

 
