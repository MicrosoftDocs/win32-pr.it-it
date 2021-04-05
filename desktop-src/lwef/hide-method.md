---
title: Hide (metodo)
description: Hide (metodo)
ms.assetid: c30eda78-0951-43b4-8ae1-daccbd41170d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd50c3f7b8e3d2e60ebe4c00c42375737c05eb04
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104117675"
---
# <a name="hide-method"></a><span data-ttu-id="d23ad-103">Hide (metodo)</span><span class="sxs-lookup"><span data-stu-id="d23ad-103">Hide Method</span></span>

<span data-ttu-id="d23ad-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d23ad-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="d23ad-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="d23ad-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="d23ad-106">Nasconde il carattere specificato.</span><span class="sxs-lookup"><span data-stu-id="d23ad-106">Hides the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="d23ad-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="d23ad-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="d23ad-108">\*agente ***. Caratteri ("*** CharacterID \* \* *"). Nascondi* \*  \[ *veloce*\]</span><span class="sxs-lookup"><span data-stu-id="d23ad-108">*agent ***.Characters ("*** CharacterID\*\*\*").Hide*\* \[*Fast*\]</span></span>



| <span data-ttu-id="d23ad-109">Parte</span><span class="sxs-lookup"><span data-stu-id="d23ad-109">Part</span></span>   | <span data-ttu-id="d23ad-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d23ad-110">Description</span></span>                                                                                                                                                                                                                                      |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d23ad-111">*Veloce*</span><span class="sxs-lookup"><span data-stu-id="d23ad-111">*Fast*</span></span> | <span data-ttu-id="d23ad-112">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="d23ad-112">Optional.</span></span> <span data-ttu-id="d23ad-113">Valore booleano che indica se ignorare l'animazione associata allo stato nascosto del carattere **true** non riproduce l'animazione **nascosta** .</span><span class="sxs-lookup"><span data-stu-id="d23ad-113">A Boolean value that indicates whether to skip the animation associated with the character's Hiding state **True** Does not play the **Hiding** animation.</span></span> <br/> <span data-ttu-id="d23ad-114">**False** (impostazione predefinita) riproduce l'animazione **nascosta** .</span><span class="sxs-lookup"><span data-stu-id="d23ad-114">**False** (Default) Plays the **Hiding** animation.</span></span> <br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d23ad-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="d23ad-115">Remarks</span></span>

<span data-ttu-id="d23ad-116">Il server accoda le azioni del metodo **Hide** nella coda del carattere, quindi è possibile usarlo per nascondere il carattere dopo una sequenza di altre animazioni.</span><span class="sxs-lookup"><span data-stu-id="d23ad-116">The server queues the actions of the **Hide** method in the character's queue, so you can use it to hide the character after a sequence of other animations.</span></span> <span data-ttu-id="d23ad-117">È possibile riprodurre l'azione immediatamente usando il metodo [**Stop**](stop-method.md) prima di chiamare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="d23ad-117">You can play the action immediately by using the [**Stop**](stop-method.md) method before calling this method.</span></span>

<span data-ttu-id="d23ad-118">Se si dichiara un riferimento a un oggetto e lo si imposta su questo metodo, viene restituito un oggetto [**Request**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="d23ad-118">If you declare an object reference and set it to this method, it returns a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="d23ad-119">Inoltre, se l'animazione **nascosta** associata non è stata caricata e non è stato specificato il parametro **Fast** su **true**, il server imposta la proprietà **Request** Object [**status**](status-property.md) su "failed" con un numero di errore appropriato.</span><span class="sxs-lookup"><span data-stu-id="d23ad-119">In addition, if the associated **Hiding** animation has not been loaded and you have not specified the **Fast** parameter as **True**, the server sets the **Request** object [**Status**](status-property.md) property to "failed" with an appropriate error number.</span></span> <span data-ttu-id="d23ad-120">Se pertanto si utilizza il protocollo HTTP per accedere ai dati di tipo carattere o di animazione, **utilizzare il metodo** [**Get**](get-method.md) e specificare lo stato Hide per caricare l'animazione prima di chiamare il metodo **Hide** .</span><span class="sxs-lookup"><span data-stu-id="d23ad-120">Therefore, if you are using the HTTP protocol to access character or animation data, use the [**Get**](get-method.md) method and specify the **Hiding** state to load the animation before calling the **Hide** method.</span></span>

<span data-ttu-id="d23ad-121">Il nascondere un carattere può anche causare l'attivazione dell'evento [**ActivateInput**](activateinput-event.md) di un altro client.</span><span class="sxs-lookup"><span data-stu-id="d23ad-121">Hiding a character can also result in triggering the [**ActivateInput**](activateinput-event.md) event of another client.</span></span>

> [!Note]  
> <span data-ttu-id="d23ad-122">I caratteri nascosti non possono accedere al canale audio.</span><span class="sxs-lookup"><span data-stu-id="d23ad-122">Hidden characters cannot access the audio channel.</span></span> <span data-ttu-id="d23ad-123">Il server restituirà uno stato di errore nell'evento [**RequestComplete**](requestcomplete-event.md) se si genera una richiesta di animazione e il carattere è nascosto.</span><span class="sxs-lookup"><span data-stu-id="d23ad-123">The server will pass back a failure status in the [**RequestComplete**](requestcomplete-event.md) event if you generate an animation request and the character is hidden.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="d23ad-124">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="d23ad-124">See Also</span></span>

[<span data-ttu-id="d23ad-125">**Show (metodo)**</span><span class="sxs-lookup"><span data-stu-id="d23ad-125">**Show method**</span></span>](show-method.md)


 

