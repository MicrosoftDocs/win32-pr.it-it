---
title: EQUALIZERSETTINGS.nextPreset
description: Il metodo nextPreset applica il set di impostazioni di equalizzatore successivo.
ms.assetid: 67d40ec9-2744-4d63-aa56-0ee20496e896
keywords:
- Media Player Windows EQUALIZERSETTINGS. nextPreset
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.nextPreset
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b464c0fca9b38a14a65a24185e51813e4520eee0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332819"
---
# <a name="equalizersettingsnextpreset"></a><span data-ttu-id="7b38f-104">EQUALIZERSETTINGS.nextPreset</span><span class="sxs-lookup"><span data-stu-id="7b38f-104">EQUALIZERSETTINGS.nextPreset</span></span>

<span data-ttu-id="7b38f-105">Il metodo **nextPreset** applica il set di impostazioni di equalizzatore successivo.</span><span class="sxs-lookup"><span data-stu-id="7b38f-105">The **nextPreset** method applies the next equalizer preset.</span></span>

``` syntax
        elementID.nextPreset()
```

## <a name="parameters"></a><span data-ttu-id="7b38f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7b38f-106">Parameters</span></span>

<span data-ttu-id="7b38f-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="7b38f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7b38f-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7b38f-108">Return Value</span></span>

<span data-ttu-id="7b38f-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="7b38f-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b38f-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="7b38f-110">Remarks</span></span>

<span data-ttu-id="7b38f-111">Se il set di impostazioni corrente è l'ultimo disponibile, il primo set di impostazioni viene reso corrente.</span><span class="sxs-lookup"><span data-stu-id="7b38f-111">If the current preset is the last one available, the first preset is made current.</span></span>

## <a name="examples"></a><span data-ttu-id="7b38f-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="7b38f-112">Examples</span></span>


```JScript
<SUBVIEW id="eqtray">
  <EQUALIZERSETTINGS id="eq"/>
  <BUTTON
    id="nextPreset" 
    onClick="eq.nextPreset();"
  />
  <BUTTON
    id="prevPreset" 
    onClick="eq.previousPreset();"
  />
  <TEXT
    id="currentPreset" 
    value="wmpprop:eq.currentPresetTitle" 
  />
</SUBVIEW>
```



## <a name="requirements"></a><span data-ttu-id="7b38f-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7b38f-113">Requirements</span></span>



| <span data-ttu-id="7b38f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b38f-114">Requirement</span></span> | <span data-ttu-id="7b38f-115">Valore</span><span class="sxs-lookup"><span data-stu-id="7b38f-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="7b38f-116">Versione</span><span class="sxs-lookup"><span data-stu-id="7b38f-116">Version</span></span><br/> | <span data-ttu-id="7b38f-117">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="7b38f-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7b38f-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7b38f-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b38f-119">**Elemento EQUALIZERSETTINGS**</span><span class="sxs-lookup"><span data-stu-id="7b38f-119">**EQUALIZERSETTINGS Element**</span></span>](equalizersettings-element.md)
</dt> <dt>

[<span data-ttu-id="7b38f-120">**EQUALIZERSETTINGS.previousPreset**</span><span class="sxs-lookup"><span data-stu-id="7b38f-120">**EQUALIZERSETTINGS.previousPreset**</span></span>](equalizersettings-previouspreset.md)
</dt> </dl>

 

 





