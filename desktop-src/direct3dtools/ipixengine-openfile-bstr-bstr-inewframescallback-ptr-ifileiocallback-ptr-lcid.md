---
description: Apre un log di grafica.
MS-HAID: vspixengine.IPixEngine\_OpenFile\_BSTR\_BSTR\_INewFramesCallback\_ptr\_IFileIOCallback\_ptr\_LCID
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IPixEngine:: OpenFile'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8E0E1336-9FC7-4C32-AF3C-F3BDF39A36D9
api_name:
- IPixEngine.OpenFile
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d18b0ff4d6d2301c6d52d2bc855d48a3db124ccb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124338"
---
# <a name="span-idvspixengineipixengine_openfile_bstr_bstr_inewframescallback_ptr_ifileiocallback_ptr_lcidspanipixengineopenfile-method"></a><span data-ttu-id="b5401-103"><span id="vspixengine.ipixengine_openfile_bstr_bstr_inewframescallback_ptr_ifileiocallback_ptr_lcid"></span>Metodo IPixEngine:: OpenFile</span><span class="sxs-lookup"><span data-stu-id="b5401-103"><span id="vspixengine.ipixengine_openfile_bstr_bstr_inewframescallback_ptr_ifileiocallback_ptr_lcid"></span>IPixEngine::OpenFile method</span></span>

<span data-ttu-id="b5401-104">Apre un log di grafica.</span><span class="sxs-lookup"><span data-stu-id="b5401-104">Opens a graphics log.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5401-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b5401-105">Syntax</span></span>


```C++
HRESULT OpenFile(
   BSTR                FileName,
   BSTR                registryBoot,
   INewFramesCallback* callbacks,
   IFileIOCallback*    pFileIOCallback,
   LCID                uiLocale
);
```

## <a name="parameters"></a><span data-ttu-id="b5401-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b5401-106">Parameters</span></span>

<span data-ttu-id="b5401-107">*FileName* </span><span class="sxs-lookup"><span data-stu-id="b5401-107">*FileName* </span></span>  
<span data-ttu-id="b5401-108">Stringa COM contenente il nome del log di grafica.</span><span class="sxs-lookup"><span data-stu-id="b5401-108">A COM string containing the name of the graphics log.</span></span>

<span data-ttu-id="b5401-109">*registryBoot* </span><span class="sxs-lookup"><span data-stu-id="b5401-109">*registryBoot* </span></span>  
<span data-ttu-id="b5401-110">Stringa COM contenente la radice del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="b5401-110">A COM string containing the registry root.</span></span> <span data-ttu-id="b5401-111">Il motore cerca il DIA e altre chiavi del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="b5401-111">The engine looks here for DIA and other registry keys.</span></span>

<span data-ttu-id="b5401-112">*callback* </span><span class="sxs-lookup"><span data-stu-id="b5401-112">*callbacks* </span></span>  
<span data-ttu-id="b5401-113">Indirizzo di una funzione utilizzata per notificare all'host che sono stati analizzati nuovi frame.</span><span class="sxs-lookup"><span data-stu-id="b5401-113">The address of a function used to notify the host that new frames have been parsed.</span></span>

<span data-ttu-id="b5401-114">*pFileIOCallback* </span><span class="sxs-lookup"><span data-stu-id="b5401-114">*pFileIOCallback* </span></span>  
<span data-ttu-id="b5401-115">Indirizzo di una funzione utilizzata per notificare all'host gli errori di i/o di file durante l'analisi.</span><span class="sxs-lookup"><span data-stu-id="b5401-115">The address of a function used to notify the host of file IO errors during parsing.</span></span>

<span data-ttu-id="b5401-116">*uiLocale* </span><span class="sxs-lookup"><span data-stu-id="b5401-116">*uiLocale* </span></span>  
<span data-ttu-id="b5401-117">ID delle impostazioni locali utilizzato per presentare i messaggi di errore in base alle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="b5401-117">The locale ID used to present error messages according to locale settings.</span></span>

## <a name="return-value"></a><span data-ttu-id="b5401-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b5401-118">Return value</span></span>

<span data-ttu-id="b5401-119">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b5401-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b5401-120">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b5401-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5401-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b5401-121">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="b5401-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b5401-122">Header</span></span></p></td><td><span data-ttu-id="b5401-123">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="b5401-123">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="b5401-124"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="b5401-124"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="b5401-125">**IPixEngine**</span><span class="sxs-lookup"><span data-stu-id="b5401-125">**IPixEngine**</span></span>](/windows/desktop/direct3dtools/ipixengine)

 

 
