---
description: Un Request to Send i percorsi dei simboli di debug al motore locale (non remoto).
MS-HAID: vspixengine.ISymbolSettings\_UpdateSymbolSettings\_SymbolServerInfo
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo ISymbolSettings:: UpdateSymbolSettings'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E48E509F-8C33-49D6-B799-B16F70C1AA64
api_name:
- ISymbolSettings.UpdateSymbolSettings
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4c60ceacbf8d11f951896979862dad6520c32837
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303834"
---
# <a name="span-idvspixengineisymbolsettings_updatesymbolsettings_symbolserverinfospanisymbolsettingsupdatesymbolsettings-method"></a><span data-ttu-id="5eec3-103"><span id="vspixengine.isymbolsettings_updatesymbolsettings_symbolserverinfo"></span>Metodo ISymbolSettings:: UpdateSymbolSettings</span><span class="sxs-lookup"><span data-stu-id="5eec3-103"><span id="vspixengine.isymbolsettings_updatesymbolsettings_symbolserverinfo"></span>ISymbolSettings::UpdateSymbolSettings method</span></span>

<span data-ttu-id="5eec3-104">Un Request to Send i percorsi dei simboli di debug al motore locale (non remoto).</span><span class="sxs-lookup"><span data-stu-id="5eec3-104">A request to send debug symbol paths to the local (non-remote) engine.</span></span>

## <a name="syntax"></a><span data-ttu-id="5eec3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5eec3-105">Syntax</span></span>


```C++
HRESULT UpdateSymbolSettings(
   SymbolServerInfo symbolServerInfo
);
```

## <a name="parameters"></a><span data-ttu-id="5eec3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5eec3-106">Parameters</span></span>

<span data-ttu-id="5eec3-107">*symbolServerInfo* </span><span class="sxs-lookup"><span data-stu-id="5eec3-107">*symbolServerInfo* </span></span>  
<span data-ttu-id="5eec3-108">Informazioni sul percorso del server di simboli di debug.</span><span class="sxs-lookup"><span data-stu-id="5eec3-108">Debug symbol server path information.</span></span>

## <a name="return-value"></a><span data-ttu-id="5eec3-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5eec3-109">Return value</span></span>

<span data-ttu-id="5eec3-110">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5eec3-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5eec3-111">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5eec3-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5eec3-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5eec3-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="5eec3-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5eec3-113">Header</span></span></p></td><td><span data-ttu-id="5eec3-114">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="5eec3-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="5eec3-115"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="5eec3-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="5eec3-116">**ISymbolSettings**</span><span class="sxs-lookup"><span data-stu-id="5eec3-116">**ISymbolSettings**</span></span>](/windows/desktop/direct3dtools/isymbolsettings)

 

 
