---
title: Eventi interni
description: Eventi interni
ms.assetid: d99e84ec-41db-42e7-ab26-5ca6a3ba610b
keywords:
- Windows Media Player Skin, eventi interni
- interfacce, eventi interni
- eventi, interni
- scrittura di codice per interfacce, eventi interni
- eventi interni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f08ed2abca3f23a89ea6fe261a29639d671e0d58
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955254"
---
# <a name="internal-events"></a><span data-ttu-id="eecfc-108">Eventi interni</span><span class="sxs-lookup"><span data-stu-id="eecfc-108">Internal Events</span></span>

<span data-ttu-id="eecfc-109">È possibile rilevare le modifiche apportate in Windows Media Player o modifiche nell'interfaccia personalizzata.</span><span class="sxs-lookup"><span data-stu-id="eecfc-109">You can detect changes that occur in Windows Media Player or changes in your own skin.</span></span> <span data-ttu-id="eecfc-110">Queste modifiche possono essere apportate alle proprietà o ai metodi dell'oggetto Media Player di Windows, alle modifiche degli attributi di interfaccia e così via.</span><span class="sxs-lookup"><span data-stu-id="eecfc-110">These can be changes in Windows Media Player object properties or methods, changes in skin attributes, and so on.</span></span>

## <a name="windows-media-player-property-changes"></a><span data-ttu-id="eecfc-111">Modifiche alle proprietà di Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="eecfc-111">Windows Media Player Property Changes</span></span>

<span data-ttu-id="eecfc-112">È possibile elaborare le modifiche in Windows Media Player usando il listener wmpprop.</span><span class="sxs-lookup"><span data-stu-id="eecfc-112">You can process changes in Windows Media Player by using the wmpprop listener.</span></span> <span data-ttu-id="eecfc-113">È necessario configurare il listener come valore di un attributo.</span><span class="sxs-lookup"><span data-stu-id="eecfc-113">You must set up the listener as a value of an attribute.</span></span> <span data-ttu-id="eecfc-114">Inserire il valore tra virgolette doppie e iniziare con la parola "wmpprop" seguita da due punti.</span><span class="sxs-lookup"><span data-stu-id="eecfc-114">Put the value in double quotes, and start with the word "wmpprop" followed by a colon.</span></span> <span data-ttu-id="eecfc-115">Si includerà quindi la proprietà che si vuole ascoltare.</span><span class="sxs-lookup"><span data-stu-id="eecfc-115">Then you include the property you want to listen to.</span></span> <span data-ttu-id="eecfc-116">Quando la proprietà viene modificata, anche il valore dell'attributo viene modificato.</span><span class="sxs-lookup"><span data-stu-id="eecfc-116">When the property changes, the value of the attribute will change also.</span></span> <span data-ttu-id="eecfc-117">Ad esempio, per modificare il valore di un elemento Slider ogni volta che viene modificato il valore dell'attributo **currentPosition** , digitare quanto segue:</span><span class="sxs-lookup"><span data-stu-id="eecfc-117">For example, to have a slider element value change whenever the value of the **currentPosition** attribute changes, type the following:</span></span>


```C++
<SLIDER id="mySlider" value="wmpprop:player.Controls.currentPosition" />
```



-   <span data-ttu-id="eecfc-118">**Importante** Non usare wmpprop nei metodi Media Player di Windows.</span><span class="sxs-lookup"><span data-stu-id="eecfc-118">**Important** Do not use wmpprop on Windows Media Player methods.</span></span> <span data-ttu-id="eecfc-119">Potrebbero verificarsi risultati imprevisti.</span><span class="sxs-lookup"><span data-stu-id="eecfc-119">Unexpected results may occur.</span></span>

## <a name="windows-media-player-method-changes"></a><span data-ttu-id="eecfc-120">Modifiche al metodo Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="eecfc-120">Windows Media Player Method Changes</span></span>

<span data-ttu-id="eecfc-121">È possibile far rispondere la propria interfaccia alla disponibilità dei metodi in Windows Media Player usando wmpenabled e wmpdisabled.</span><span class="sxs-lookup"><span data-stu-id="eecfc-121">You can make your skin respond to the availability of methods on Windows Media Player using wmpenabled and wmpdisabled.</span></span> <span data-ttu-id="eecfc-122">Questi vengono usati in modo analogo al listener wmpprop, ad eccezione del fatto che è possibile usarli solo su metodi dell'oggetto **controllo** supportati dal metodo **disavailable** .</span><span class="sxs-lookup"><span data-stu-id="eecfc-122">These are used similarly to the wmpprop listener except that you can only use these on methods of the **Control** object that are supported by the **isAvailable** method.</span></span>

<span data-ttu-id="eecfc-123">Ad esempio, è possibile abilitare un pulsante solo quando il metodo **Play** è abilitato, usando un codice simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="eecfc-123">For example, you could enable a button only when the **Play** method is enabled, using code like this:</span></span>


```C++
<BUTTON ... enabled="wmpenabled:player.Controls.Play();" />

```



-   <span data-ttu-id="eecfc-124">**Importante** Non usare wmpenabled o wmpdisabled nelle proprietà Media Player di Windows.</span><span class="sxs-lookup"><span data-stu-id="eecfc-124">**Important** Do not use wmpenabled or wmpdisabled on Windows Media Player properties.</span></span> <span data-ttu-id="eecfc-125">Potrebbero verificarsi risultati imprevisti.</span><span class="sxs-lookup"><span data-stu-id="eecfc-125">Unexpected results may occur.</span></span>

## <a name="skin-attribute-changes"></a><span data-ttu-id="eecfc-126">Modifiche all'attributo Skin</span><span class="sxs-lookup"><span data-stu-id="eecfc-126">Skin Attribute Changes</span></span>

<span data-ttu-id="eecfc-127">È possibile rispondere alle modifiche negli attributi dell'interfaccia utente in uno dei due modi seguenti, usando wmpprop o l'evento **\_ OnChange** .</span><span class="sxs-lookup"><span data-stu-id="eecfc-127">You can respond to changes in your skin attributes in one of two ways, by using wmpprop or the **\_onchange** event.</span></span>

<span data-ttu-id="eecfc-128">È possibile usare wmpprop per restare in ascolto delle modifiche nell'interfaccia personalizzata.</span><span class="sxs-lookup"><span data-stu-id="eecfc-128">You can use wmpprop to listen for changes in your own skin.</span></span> <span data-ttu-id="eecfc-129">Ad esempio, per visualizzare il valore del dispositivo di scorrimento in una casella di testo, è possibile digitare quanto segue:</span><span class="sxs-lookup"><span data-stu-id="eecfc-129">For example, to show the Slider value in a text box, you could type the following:</span></span>


```C++
<TEXT ... value="wmpprop:mySlider.value">

```



<span data-ttu-id="eecfc-130">È possibile utilizzare l'evento **\_ OnChange** per elaborare gli eventi all'interno di un elemento.</span><span class="sxs-lookup"><span data-stu-id="eecfc-130">You can use the **\_onchange** event to process events inside an element.</span></span> <span data-ttu-id="eecfc-131">È necessario alleghi il nome dell'attributo di cui si vuole tenere traccia per la **\_ modifica**.</span><span class="sxs-lookup"><span data-stu-id="eecfc-131">You must attach the name of the attribute you want to track to **\_onchange**.</span></span> <span data-ttu-id="eecfc-132">Se ad esempio si desidera tenere traccia del valore di una casella di testo, digitare:</span><span class="sxs-lookup"><span data-stu-id="eecfc-132">For example, if you want to track the value of a text box, you would type:</span></span>


```C++
value_onchange

```



<span data-ttu-id="eecfc-133">Si assegnerà quindi una stringa JScript che si desidera eseguire quando cambia il valore.</span><span class="sxs-lookup"><span data-stu-id="eecfc-133">You would then assign a JScript string that you want to run when the value changes.</span></span> <span data-ttu-id="eecfc-134">Ad esempio, per rispondere a una modifica nel valore di una casella di testo che può essere usata per regolare il volume di Media Player di Windows, digitare quanto segue all'interno dell'elemento di **testo** come attributo:</span><span class="sxs-lookup"><span data-stu-id="eecfc-134">For example, to respond to a change in the value of a text box that can be used to adjust the volume of Windows Media Player, type the following inside your **TEXT** element as an attribute:</span></span>


```C++
value_onchange = "JScript: player.Settings.Volume = myText.value"

```



## <a name="related-topics"></a><span data-ttu-id="eecfc-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="eecfc-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eecfc-136">**Gestione degli eventi**</span><span class="sxs-lookup"><span data-stu-id="eecfc-136">**Handling Events**</span></span>](handling-events.md)
</dt> </dl>

 

 




