---
title: Attributi di ascolto
description: Attributi di ascolto
ms.assetid: 51b10507-5c2e-49ca-b560-6db6a1a7ee87
keywords:
- Interfacce di Media Player Windows, attributi in ascolto
- interfacce, attributi di ascolto
- riferimento per le interfacce, gli attributi di ascolto
- attributi di ascolto
- attributi, ascolto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 349a549966f7fba5ea152f8f0bb002a92f6dfb8e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515676"
---
# <a name="listening-attributes"></a><span data-ttu-id="af71d-108">Attributi di ascolto</span><span class="sxs-lookup"><span data-stu-id="af71d-108">Listening Attributes</span></span>

<span data-ttu-id="af71d-109">Un attributo in ascolto viene usato per connettere un attributo a un altro, in modo che il valore venga modificato ogni volta che il valore dell'altro attributo viene modificato.</span><span class="sxs-lookup"><span data-stu-id="af71d-109">A listening attribute is used to connect one attribute to another so that its value changes every time the value of the other attribute changes.</span></span>

<span data-ttu-id="af71d-110">L'attributo listening **wmpprop:** è il più utile.</span><span class="sxs-lookup"><span data-stu-id="af71d-110">The listening attribute **wmpprop:** is the most useful.</span></span> <span data-ttu-id="af71d-111">Se il valore di un attributo viene specificato come **wmpprop:** di un secondo attributo, il primo valore verrà aggiornato automaticamente in modo da riflettere il secondo valore ogni volta che viene modificato il secondo valore.</span><span class="sxs-lookup"><span data-stu-id="af71d-111">If the value of one attribute is specified to be the **wmpprop:** of a second attribute, the first value will be automatically updated to reflect the second value each time the second value changes.</span></span>

<span data-ttu-id="af71d-112">**Esempio:**</span><span class="sxs-lookup"><span data-stu-id="af71d-112">**Example:**</span></span>


```C++
<TEXT
  value="wmpprop:mySlider.value"
/>

```



<span data-ttu-id="af71d-113">In questo modo, il valore di caslider, illustrato dalla posizione del controllo dispositivo di scorrimento, può essere visualizzato anche come numero in una casella di testo.</span><span class="sxs-lookup"><span data-stu-id="af71d-113">In this way, the value of mySlider, shown by the position of the slider control, can also be shown as a number within a text box.</span></span>

<span data-ttu-id="af71d-114">Gli altri due attributi di ascolto, **wmpenabled:** e **wmpdisabled:**, possono essere usati per modificare l'attributo **Enabled** di un controllo a seconda che la funzionalità sia attualmente disponibile nel lettore.</span><span class="sxs-lookup"><span data-stu-id="af71d-114">The two other listening attributes, **wmpenabled:** and **wmpdisabled:**, can be used to change the **enabled** attribute of a control depending on whether its functionality is currently available in the player.</span></span> <span data-ttu-id="af71d-115">Questi attributi possono restare in ascolto solo dei metodi dell'oggetto **Controls** .</span><span class="sxs-lookup"><span data-stu-id="af71d-115">These attributes can listen only to methods of the **Controls** object.</span></span>

<span data-ttu-id="af71d-116">**Esempio:**</span><span class="sxs-lookup"><span data-stu-id="af71d-116">**Example:**</span></span>


```C++
<BUTTON 
  id="play" 
  enabled="wmpenabled:player.controls.play"
/>

```



## <a name="related-topics"></a><span data-ttu-id="af71d-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="af71d-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af71d-118">**Varie**</span><span class="sxs-lookup"><span data-stu-id="af71d-118">**Miscellaneous**</span></span>](miscellaneous.md)
</dt> </dl>

 

 




