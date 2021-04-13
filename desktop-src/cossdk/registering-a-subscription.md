---
description: Dopo la registrazione di una classe di evento nel catalogo COM+, è possibile aggiungere sottoscrittori alla classe di evento e alle sottoscrizioni dei sottoscrittori.
ms.assetid: 101b1075-3724-4508-9c9e-2f12ac6ab65d
title: Registrazione di una sottoscrizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a03d5710fc792cad6282683d51df21d2ede10451
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401486"
---
# <a name="registering-a-subscription"></a><span data-ttu-id="500b5-103">Registrazione di una sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="500b5-103">Registering a Subscription</span></span>

<span data-ttu-id="500b5-104">Dopo la registrazione di una classe di evento nel catalogo COM+, è possibile aggiungere sottoscrittori alla classe di evento e alle sottoscrizioni dei sottoscrittori.</span><span class="sxs-lookup"><span data-stu-id="500b5-104">After you have registered an event class in the COM+ catalog, you can add subscribers to the event class and subscriptions to the subscribers.</span></span> <span data-ttu-id="500b5-105">Le sottoscrizioni possono sottoscrivere un solo metodo o tutti i metodi di un'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="500b5-105">Subscriptions can subscribe to a single method or to all the methods of an interface.</span></span> <span data-ttu-id="500b5-106">Per ricevere chiamate su più di un metodo, ma non su ogni metodo, di un'interfaccia, è necessario aggiungere una sottoscrizione per ogni metodo a cui si desidera ricevere una chiamata.</span><span class="sxs-lookup"><span data-stu-id="500b5-106">To receive calls on more than one method—but not to every method—of an interface, you must add a subscription for each method to which you want to receive a call.</span></span> <span data-ttu-id="500b5-107">Lo strumento di amministrazione Servizi componenti può eseguire ricerche nel catalogo COM+ per le classi di evento registrate che supportano le interfacce implementate dal Sottoscrittore e offre la possibilità di effettuare la sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="500b5-107">The Component Services administration tool can search the COM+ catalog for registered event classes that support the interfaces implemented by the subscriber and offers you the choice to subscribe.</span></span> <span data-ttu-id="500b5-108">Scegliere il server di pubblicazione che offre gli eventi desiderati.</span><span class="sxs-lookup"><span data-stu-id="500b5-108">Choose the publisher that offers you the desired events.</span></span>

<span data-ttu-id="500b5-109">Per aggiungere i Sottoscrittori al componente del Sottoscrittore, attenersi alla procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="500b5-109">To add subscribers to the subscriber component, use the following steps:</span></span>

1.  <span data-ttu-id="500b5-110">Dopo aver creato una nuova applicazione COM+ e installato il componente del Sottoscrittore, fare clic con il pulsante destro del mouse sulla cartella **sottoscrizioni** per abilitare la creazione guidata nuova sottoscrizione com+.</span><span class="sxs-lookup"><span data-stu-id="500b5-110">After creating a new COM+ application and installing the subscriber component, right-click the **Subscriptions** folder to enable the COM+ New Subscription Wizard.</span></span>

2.  <span data-ttu-id="500b5-111">Scegliere la classe di evento da cui si desidera ricevere gli eventi.</span><span class="sxs-lookup"><span data-stu-id="500b5-111">Choose the event class from which you want to receive events.</span></span>

3.  <span data-ttu-id="500b5-112">Immettere un nome per la sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="500b5-112">Enter a name for the subscription.</span></span>

4.  <span data-ttu-id="500b5-113">Abilitare la sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="500b5-113">Enable the subscription.</span></span>

5.  <span data-ttu-id="500b5-114">Fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="500b5-114">Click **OK**.</span></span>

<span data-ttu-id="500b5-115">Quando un'applicazione del server di pubblicazione desidera generare un evento, il server di pubblicazione crea un'istanza dell'oggetto classe di evento e chiama un metodo su di esso.</span><span class="sxs-lookup"><span data-stu-id="500b5-115">When a publisher application wants to fire an event, the publisher instantiates the event class object and calls a method on it.</span></span> <span data-ttu-id="500b5-116">COM+ esegue una ricerca nel catalogo COM+ per trovare tutti i sottoscrittori.</span><span class="sxs-lookup"><span data-stu-id="500b5-116">COM+ searches the COM+ catalog to find all the subscribers.</span></span> <span data-ttu-id="500b5-117">Crea l'oggetto sottoscrittore (direttamente, in coda o con un moniker) e passa la chiamata al metodo originariamente eseguita dal server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="500b5-117">It creates the subscriber object (directly, queued, or with a moniker) and passes on the method call originally made by the publisher.</span></span>

## <a name="related-topics"></a><span data-ttu-id="500b5-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="500b5-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="500b5-119">Registrazione di una classe di evento</span><span class="sxs-lookup"><span data-stu-id="500b5-119">Registering an Event Class</span></span>](registering-an-event-class.md)
</dt> </dl>

 

 



