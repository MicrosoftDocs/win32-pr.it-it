---
title: Settings. rate
description: La proprietà rate specifica o recupera la frequenza di riproduzione corrente dei supporti video.
ms.assetid: 0f95f7ac-1bb6-4c80-89eb-eb300a03a0f1
keywords:
- Impostazioni. Frequenza Media Player di Windows
topic_type:
- apiref
api_name:
- Settings.rate
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e61287789487fddbe7e77fba5fc033d3103aecb8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327371"
---
# <a name="settingsrate"></a><span data-ttu-id="db879-104">Settings. rate</span><span class="sxs-lookup"><span data-stu-id="db879-104">Settings.rate</span></span>

<span data-ttu-id="db879-105">La proprietà **rate** specifica o recupera la frequenza di riproduzione corrente dei supporti video.</span><span class="sxs-lookup"><span data-stu-id="db879-105">The **rate** property specifies or retrieves the current playback rate of video media.</span></span>

## <a name="syntax"></a><span data-ttu-id="db879-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="db879-106">Syntax</span></span>

<span data-ttu-id="db879-107">Player. Settings. rate</span><span class="sxs-lookup"><span data-stu-id="db879-107">player.settings.rate</span></span>

## <a name="possible-values"></a><span data-ttu-id="db879-108">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="db879-108">Possible Values</span></span>

<span data-ttu-id="db879-109">Questa proprietà è un **numero** di lettura/scrittura (**Double**) il cui valore predefinito è 1,0.</span><span class="sxs-lookup"><span data-stu-id="db879-109">This property is a read/write **Number** (**double**) with a default value of 1.0.</span></span>

## <a name="remarks"></a><span data-ttu-id="db879-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="db879-110">Remarks</span></span>

<span data-ttu-id="db879-111">Questa proprietà funge da valore moltiplicatore che consente di riprodurre una clip a una velocità più veloce o più lenta.</span><span class="sxs-lookup"><span data-stu-id="db879-111">This property acts as a multiplier value that allows you to play a clip at a faster or slower rate.</span></span> <span data-ttu-id="db879-112">Il valore predefinito 1,0 indica la velocità creata.</span><span class="sxs-lookup"><span data-stu-id="db879-112">The default value of 1.0 indicates the authored speed.</span></span> <span data-ttu-id="db879-113">Si noti che una traccia audio diventa difficile da comprendere a una velocità inferiore a 0,5 o superiore a 1,5.</span><span class="sxs-lookup"><span data-stu-id="db879-113">Note that an audio track becomes difficult to understand at rates lower than 0.5 or higher than 1.5.</span></span> <span data-ttu-id="db879-114">Una velocità di riproduzione pari a 2 corrisponde al doppio della velocità di riproduzione normale.</span><span class="sxs-lookup"><span data-stu-id="db879-114">A playback rate of 2 equates to twice the normal playback speed.</span></span>

<span data-ttu-id="db879-115">Windows Media Player tenterà di utilizzare il più efficace di quattro diverse modalità di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="db879-115">Windows Media Player will attempt to use the most effective of four different playback modes.</span></span> <span data-ttu-id="db879-116">Queste modalità sono la riproduzione video uniforme con il pitch audio mantenuto e la riproduzione video uniforme con il pitch audio non mantenuto, la riproduzione video uniforme senza audio e la riproduzione di video con fotogrammi chiave senza audio.</span><span class="sxs-lookup"><span data-stu-id="db879-116">These modes are smooth video playback with audio pitch maintained, smooth video playback with audio pitch not maintained, smooth video playback with no audio, and keyframe video playback with no audio.</span></span> <span data-ttu-id="db879-117">La modalità scelta dal lettore dipende da numerosi fattori, tra cui il tipo di file e la posizione, il sistema operativo, la rete e il server.</span><span class="sxs-lookup"><span data-stu-id="db879-117">The mode chosen by the Player depends on numerous factors including file type and location, operating system, network, and server.</span></span>

<span data-ttu-id="db879-118">Si applicano anche altre considerazioni, a seconda del tipo di supporto:</span><span class="sxs-lookup"><span data-stu-id="db879-118">Other considerations apply as well, depending on media type:</span></span>

-   <span data-ttu-id="db879-119">File Windows Media Format (WMV) e ASF: i valori ottimali per questa proprietà sono compresi tra 1 e 10 o da 1 a 10 per la riproduzione inversa.</span><span class="sxs-lookup"><span data-stu-id="db879-119">Windows Media Format (WMV) and ASF files: Optimal values for this property are from 1 to 10, or from  1 to  10 for reverse play.</span></span> <span data-ttu-id="db879-120">I valori compresi tra 0,5 e 1,0 o da-0,5 a-1,0 possono anche funzionare correttamente nei casi in cui è possibile mantenere il pitch audio, ad esempio quando si giocano i file che si trovano nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="db879-120">Values from 0.5 to 1.0 or from -0.5 to -1.0 may also work well in cases where audio pitch can be maintained, for example, when playing files located on the local computer.</span></span> <span data-ttu-id="db879-121">I valori con una grandezza assoluta maggiore di 10 sono consentiti, ma non sono molto significativi.</span><span class="sxs-lookup"><span data-stu-id="db879-121">Values with an absolute magnitude greater than 10 are allowed, but are not very meaningful.</span></span>
-   <span data-ttu-id="db879-122">Altri tipi di supporti video: questa proprietà può variare da 0 a 9.</span><span class="sxs-lookup"><span data-stu-id="db879-122">Other Video Media Types: This property can range from 0 to 9.</span></span> <span data-ttu-id="db879-123">I valori negativi non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="db879-123">Negative values are not allowed.</span></span> <span data-ttu-id="db879-124">I valori minori di 1 rappresentano un movimento lento.</span><span class="sxs-lookup"><span data-stu-id="db879-124">Values less than 1 represent slow motion.</span></span> <span data-ttu-id="db879-125">I valori superiori a 9 sono consentiti, ma non sono molto significativi.</span><span class="sxs-lookup"><span data-stu-id="db879-125">Values above 9 are allowed, but are not very meaningful.</span></span>

<span data-ttu-id="db879-126">*Controlli*. il metodo **fastForward** imposta il valore di **rate** su 5,0, mentre i *controlli*. la **frequenza** delle modifiche al metodo **fastReverse** è 5,0.</span><span class="sxs-lookup"><span data-stu-id="db879-126">The *Controls*.**fastForward** method changes the value of **rate** to 5.0, while the *Controls*.**fastReverse** method changes **rate** to  5.0.</span></span>

<span data-ttu-id="db879-127">Non è possibile modificare la velocità di riproduzione di alcuni tipi di supporto.</span><span class="sxs-lookup"><span data-stu-id="db879-127">The playback rate of some media types cannot be altered.</span></span> <span data-ttu-id="db879-128">Usare le *Impostazioni*. **Metodo IsValid** per determinare se questa proprietà può essere specificata per un particolare elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="db879-128">Use the *Settings*.**isAvailable** method to determine whether this property can be specified for a particular media item.</span></span>

<span data-ttu-id="db879-129">**Windows Media Player 10 Mobile**: questa proprietà accetta o restituisce solo i valori-5,0, 1,0 o 5,0.</span><span class="sxs-lookup"><span data-stu-id="db879-129">**Windows Media Player 10 Mobile**: This property only accepts or returns values of -5.0, 1.0, or 5.0.</span></span>

## <a name="examples"></a><span data-ttu-id="db879-130">Esempio</span><span class="sxs-lookup"><span data-stu-id="db879-130">Examples</span></span>

<span data-ttu-id="db879-131">Nell'esempio seguente viene creato un elemento HTML SELECT che consente all'utente di modificare la velocità di riproduzione del supporto corrente.</span><span class="sxs-lookup"><span data-stu-id="db879-131">The following example creates an HTML SELECT element that allows the user to change the playback speed of the current media.</span></span> <span data-ttu-id="db879-132">Le opzioni di selezione offrono velocità di riproduzione normali, a metà velocità e a velocità doppia.</span><span class="sxs-lookup"><span data-stu-id="db879-132">The SELECT options offer normal speed, half -speed and double-speed playback rates.</span></span> <span data-ttu-id="db879-133">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="db879-133">The **Player** object was created with ID = "Player".</span></span>


```
<!-- Create the HTML SELECT element. -->
<SELECT  ID = pbRATE  NAME = "pbRATE"  LANGUAGE="JScript"
         onChange="
                   /* Test whether playback rate can be set. */
                   if(Player.settings.IsAvailable('Rate'))

                   /* Set the playback rate based on the current
                      value of the SELECT element. */
                   Player.settings.rate = this.value
">

/* Create the OPTION list. */
<OPTION VALUE = 1>NORMAL</OPTION>
<OPTION VALUE = .5>half speed</OPTION>
<OPTION VALUE = 2>2 speed</OPTION>
</SELECT>

```



## <a name="requirements"></a><span data-ttu-id="db879-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="db879-134">Requirements</span></span>



| <span data-ttu-id="db879-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="db879-135">Requirement</span></span> | <span data-ttu-id="db879-136">Valore</span><span class="sxs-lookup"><span data-stu-id="db879-136">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="db879-137">Versione</span><span class="sxs-lookup"><span data-stu-id="db879-137">Version</span></span><br/> | <span data-ttu-id="db879-138">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="db879-138">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="db879-139">DLL</span><span class="sxs-lookup"><span data-stu-id="db879-139">DLL</span></span><br/>     | <dl> <span data-ttu-id="db879-140"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db879-140"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db879-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="db879-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db879-142">**Controls. fastForward**</span><span class="sxs-lookup"><span data-stu-id="db879-142">**Controls.fastForward**</span></span>](controls-fastforward.md)
</dt> <dt>

[<span data-ttu-id="db879-143">**Controls. fastReverse**</span><span class="sxs-lookup"><span data-stu-id="db879-143">**Controls.fastReverse**</span></span>](controls-fastreverse.md)
</dt> <dt>

[<span data-ttu-id="db879-144">**Oggetto Settings**</span><span class="sxs-lookup"><span data-stu-id="db879-144">**Settings Object**</span></span>](settings-object.md)
</dt> <dt>

[<span data-ttu-id="db879-145">**Settings. available**</span><span class="sxs-lookup"><span data-stu-id="db879-145">**Settings.isAvailable**</span></span>](settings-isavailable.md)
</dt> </dl>

 

 





