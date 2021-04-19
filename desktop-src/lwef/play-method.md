---
title: Metodo Play (funzionalità legacy dell'ambiente Windows)
description: Metodo Play
ms.assetid: 7e89341a-b4d3-4bea-8e7f-31c649ff06b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1d06f4275d7b4c0959a59536c8b20a95c14ab1c
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300743"
---
# <a name="play-method-legacy-windows-environment-features"></a><span data-ttu-id="0b05d-103">Metodo Play (funzionalità legacy dell'ambiente Windows)</span><span class="sxs-lookup"><span data-stu-id="0b05d-103">Play Method (Legacy Windows Environment Features)</span></span>

<span data-ttu-id="0b05d-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0b05d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="0b05d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="0b05d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="0b05d-106">Riproduce l'animazione specificata per il carattere specificato.</span><span class="sxs-lookup"><span data-stu-id="0b05d-106">Plays the specified animation for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="0b05d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="0b05d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="0b05d-108">\*agente \***. Caratteri ("**_CharacterID_*_"). Riproduci_* "*animationName*"</span><span class="sxs-lookup"><span data-stu-id="0b05d-108">*agent\***.Characters ("**_CharacterID_*_").Play_\* "*AnimationName*"</span></span>

</dd> </dl> 

| <span data-ttu-id="0b05d-109">Parte</span><span class="sxs-lookup"><span data-stu-id="0b05d-109">Part</span></span>            | <span data-ttu-id="0b05d-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0b05d-110">Description</span></span>                                                          |
|-----------------|----------------------------------------------------------------------|
| <span data-ttu-id="0b05d-111">*AnimationName*</span><span class="sxs-lookup"><span data-stu-id="0b05d-111">*AnimationName*</span></span> | <span data-ttu-id="0b05d-112">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="0b05d-112">Required.</span></span> <span data-ttu-id="0b05d-113">Stringa che specifica il nome di una sequenza di animazione.</span><span class="sxs-lookup"><span data-stu-id="0b05d-113">A string that specifies the name of an animation sequence.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="0b05d-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="0b05d-114">Remarks</span></span>

<span data-ttu-id="0b05d-115">Il nome di un'animazione viene definito quando il carattere viene compilato con l'editor dei caratteri di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="0b05d-115">An animation's name is defined when the character is compiled with the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="0b05d-116">Prima di riprodurre l'animazione specificata, il server tenta di riprodurre l'animazione **restituita** per l'animazione precedente, se ne è stata assegnata una.</span><span class="sxs-lookup"><span data-stu-id="0b05d-116">Before playing the specified animation, the server attempts to play the **Return** animation for the previous animation, if one has been assigned.</span></span>

<span data-ttu-id="0b05d-117">Quando si accede alle animazioni di un carattere usando un protocollo file convenzionale, è possibile usare semplicemente il metodo **Play** specificando il nome dell'animazione.</span><span class="sxs-lookup"><span data-stu-id="0b05d-117">When accessing a character's animations using a conventional file protocol, you can simply use the **Play** method specifying the name of the animation.</span></span> <span data-ttu-id="0b05d-118">Tuttavia, se si utilizza il protocollo HTTP per accedere ai dati di animazione dei caratteri, utilizzare il metodo **Get** per caricare l'animazione prima di chiamare il metodo **Play** .</span><span class="sxs-lookup"><span data-stu-id="0b05d-118">However, if you are using the HTTP protocol to access character animation data, use the **Get** method to load the animation before calling the **Play** method.</span></span>

<span data-ttu-id="0b05d-119">Per ulteriori informazioni, vedere il metodo **Get** .</span><span class="sxs-lookup"><span data-stu-id="0b05d-119">For more information, see the **Get** method.</span></span>

<span data-ttu-id="0b05d-120">Per semplificare la sintassi, è possibile dichiarare un riferimento a un oggetto e impostarlo in modo che faccia riferimento all'oggetto [**character**](/windows/desktop/lwef/the-characters-object) nella raccolta [**characters**](/windows/desktop/lwef/the-characters-object) e usare il riferimento come parte delle istruzioni **Play** :</span><span class="sxs-lookup"><span data-stu-id="0b05d-120">To simplify your syntax, you can declare an object reference and set it to reference the [**Character**](/windows/desktop/lwef/the-characters-object) object in the [**Characters**](/windows/desktop/lwef/the-characters-object) collection and use the reference as part of your **Play** statements:</span></span>


```
   Dim Genie   
   Agent1.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"

   Set Genie = Agent1.Characters ("Genie")
   
   Genie.Get "state", "Showing"
   Genie.Show

   Genie.Get "animation", "Greet, GreetReturn"
   Genie.Play "Greet"
   Genie.Speak "Hello."
```



<span data-ttu-id="0b05d-121">Se si dichiara un riferimento a un oggetto e lo si imposta su questo metodo, viene restituito un oggetto [**Request**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="0b05d-121">If you declare an object reference and set it to this method, it returns a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="0b05d-122">Inoltre, se si specifica un'animazione che non viene caricata o se il carattere non è stato caricato correttamente, il server imposta la proprietà [**status**](status-property.md) dell'oggetto **Request** su "failed" con un numero di errore appropriato.</span><span class="sxs-lookup"><span data-stu-id="0b05d-122">In addition, if you specify an animation that is not loaded or if the character has not been successfully loaded, the server sets the [**Status**](status-property.md) property of **Request** object to "failed" with an appropriate error number.</span></span> <span data-ttu-id="0b05d-123">Tuttavia, se l'animazione non esiste e i dati del carattere sono già stati caricati correttamente, il server genera un errore.</span><span class="sxs-lookup"><span data-stu-id="0b05d-123">However, if the animation does not exist and the character's data has already been successfully loaded, the server raises an error.</span></span>

<span data-ttu-id="0b05d-124">Il metodo **Play** non rende visibile il carattere.</span><span class="sxs-lookup"><span data-stu-id="0b05d-124">The **Play** method does not make the character visible.</span></span> <span data-ttu-id="0b05d-125">Se il carattere non è visibile, il server riproduce l'animazione in maniera invisibile e imposta la proprietà [**status**](status-property.md) dell'oggetto [**Request**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="0b05d-125">If the character is not visible, the server plays the animation invisibly, and sets the [**Status**](status-property.md) property of the [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span>

 

 
