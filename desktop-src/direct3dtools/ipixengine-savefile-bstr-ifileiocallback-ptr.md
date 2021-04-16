---
description: Salva il log di grafica nel percorso specificato.
MS-HAID: vspixengine.IPixEngine\_SaveFile\_BSTR\_IFileIOCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IPixEngine:: SaveFile'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A80498F4-C8F5-4AC0-92C5-A90EB2A090B7
api_name:
- IPixEngine.SaveFile
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f7e1bed8765ca64123ccf13cbc3ee5f0d989b115
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522722"
---
# <a name="span-idvspixengineipixengine_savefile_bstr_ifileiocallback_ptrspanipixenginesavefile-method"></a><span data-ttu-id="b0fa2-103"><span id="vspixengine.ipixengine_savefile_bstr_ifileiocallback_ptr"></span>Metodo IPixEngine:: SaveFile</span><span class="sxs-lookup"><span data-stu-id="b0fa2-103"><span id="vspixengine.ipixengine_savefile_bstr_ifileiocallback_ptr"></span>IPixEngine::SaveFile method</span></span>

<span data-ttu-id="b0fa2-104">Salva il log di grafica nel percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="b0fa2-104">Saves the graphics log to the specified location.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0fa2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b0fa2-105">Syntax</span></span>


```C++
HRESULT SaveFile(
   BSTR             FileName,
   IFileIOCallback* pFileIOCallback
);
```

## <a name="parameters"></a><span data-ttu-id="b0fa2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b0fa2-106">Parameters</span></span>

<span data-ttu-id="b0fa2-107">*FileName* </span><span class="sxs-lookup"><span data-stu-id="b0fa2-107">*FileName* </span></span>  
<span data-ttu-id="b0fa2-108">Stringa COM contenente il percorso del log di grafica salvato.</span><span class="sxs-lookup"><span data-stu-id="b0fa2-108">A COM string containing the pathname of the saved graphics log.</span></span>

<span data-ttu-id="b0fa2-109">*pFileIOCallback* </span><span class="sxs-lookup"><span data-stu-id="b0fa2-109">*pFileIOCallback* </span></span>  
<span data-ttu-id="b0fa2-110">Indirizzo di un l'funzioni utilizzato per notificare all'host gli errori di i/o del file durante il salvataggio.</span><span class="sxs-lookup"><span data-stu-id="b0fa2-110">The address of a functon used to notify the host of file IO errors during save.</span></span>

## <a name="return-value"></a><span data-ttu-id="b0fa2-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b0fa2-111">Return value</span></span>

<span data-ttu-id="b0fa2-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b0fa2-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b0fa2-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b0fa2-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0fa2-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b0fa2-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="b0fa2-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b0fa2-115">Header</span></span></p></td><td><span data-ttu-id="b0fa2-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="b0fa2-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="b0fa2-117"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="b0fa2-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="b0fa2-118">**IPixEngine**</span><span class="sxs-lookup"><span data-stu-id="b0fa2-118">**IPixEngine**</span></span>](/windows/desktop/direct3dtools/ipixengine)

 

 
