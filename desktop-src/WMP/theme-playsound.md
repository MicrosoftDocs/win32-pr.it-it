---
title: THEME. playSound
description: Il metodo playSound riproduce il file audio specificato.
ms.assetid: 42675a66-0139-4e74-9abe-1b42017fc6fe
keywords:
- THEME. playSound Windows Media Player
topic_type:
- apiref
api_name:
- THEME.playSound
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ceb30e5c47632a1358262019124fceae056294d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328389"
---
# <a name="themeplaysound"></a><span data-ttu-id="8fe07-104">THEME. playSound</span><span class="sxs-lookup"><span data-stu-id="8fe07-104">THEME.playSound</span></span>

<span data-ttu-id="8fe07-105">Il metodo **PlaySound** riproduce il file audio specificato.</span><span class="sxs-lookup"><span data-stu-id="8fe07-105">The **playSound** method plays the specified sound file.</span></span>

``` syntax
        theme.playSound(soundFile)
```

## <a name="parameters"></a><span data-ttu-id="8fe07-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8fe07-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fe07-107"><span id="soundFile"></span><span id="soundfile"></span><span id="SOUNDFILE"></span>*soundFile*</span><span class="sxs-lookup"><span data-stu-id="8fe07-107"><span id="soundFile"></span><span id="soundfile"></span><span id="SOUNDFILE"></span>*soundFile*</span></span>
</dt> <dd>

<span data-ttu-id="8fe07-108">**Stringa** che specifica il nome del file audio da riprodurre.</span><span class="sxs-lookup"><span data-stu-id="8fe07-108">A **String** specifying the name of the sound file to play.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fe07-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8fe07-109">Return Value</span></span>

<span data-ttu-id="8fe07-110">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="8fe07-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8fe07-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="8fe07-111">Remarks</span></span>

<span data-ttu-id="8fe07-112">Questo metodo consente di aggiungere effetti acustici a un'interfaccia, ad esempio quando si fa clic sui pulsanti.</span><span class="sxs-lookup"><span data-stu-id="8fe07-112">This method allows you to add sound effects to a skin for example, when buttons are clicked.</span></span> <span data-ttu-id="8fe07-113">Il suono viene riprodotto direttamente dal sistema operativo e non da Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="8fe07-113">The sound is played by the operating system directly and not by Windows Media Player.</span></span> <span data-ttu-id="8fe07-114">Ciò significa che non è possibile controllare il suono con le impostazioni e i metodi Media Player di Windows, ma può essere riprodotto mentre Windows Media Player sta eseguendo un altro file multimediale digitale.</span><span class="sxs-lookup"><span data-stu-id="8fe07-114">This means that the sound cannot be controlled with Windows Media Player settings and methods, but it can be played while Windows Media Player is playing another digital media file.</span></span>

<span data-ttu-id="8fe07-115">Questo metodo supporta solo file WAV.</span><span class="sxs-lookup"><span data-stu-id="8fe07-115">This method supports WAV files only.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fe07-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8fe07-116">Requirements</span></span>



| <span data-ttu-id="8fe07-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8fe07-117">Requirement</span></span> | <span data-ttu-id="8fe07-118">Valore</span><span class="sxs-lookup"><span data-stu-id="8fe07-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="8fe07-119">Versione</span><span class="sxs-lookup"><span data-stu-id="8fe07-119">Version</span></span><br/> | <span data-ttu-id="8fe07-120">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="8fe07-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8fe07-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8fe07-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fe07-122">**Elemento THEME**</span><span class="sxs-lookup"><span data-stu-id="8fe07-122">**THEME Element**</span></span>](theme-element.md)
</dt> </dl>

 

 





