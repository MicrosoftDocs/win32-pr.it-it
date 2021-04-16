---
description: Ricezione di una risposta
ms.assetid: 48919608-a102-43e2-9ca0-80b17344b5eb
title: Ricezione di una risposta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e9e05ec392b7db828ad1efd1360c4d4fb232210
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524178"
---
# <a name="receiving-a-response"></a><span data-ttu-id="2f13b-103">Ricezione di una risposta</span><span class="sxs-lookup"><span data-stu-id="2f13b-103">Receiving a Response</span></span>

<span data-ttu-id="2f13b-104">Poiché i componenti in coda sono progettati per funzionare in modo asincrono, le applicazioni client non devono bloccarsi in attesa di una risposta da una richiesta in coda.</span><span class="sxs-lookup"><span data-stu-id="2f13b-104">Because queued components are designed to work asynchronously, client applications should not block while waiting for a response from a queued request.</span></span> <span data-ttu-id="2f13b-105">Tuttavia, è spesso utile per l'applicazione client o un'applicazione correlata nel computer client per ricevere una risposta alla fine.</span><span class="sxs-lookup"><span data-stu-id="2f13b-105">Nevertheless, it is often useful for the client application or a related application on the client machine to receive a response eventually.</span></span> <span data-ttu-id="2f13b-106">È ad esempio possibile che un client desideri ricevere una notifica quando una transazione richiesta è stata completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="2f13b-106">For example, a client may want to be notified when a requested transaction has been completed successfully.</span></span>

<span data-ttu-id="2f13b-107">Esistono diversi modi in cui un componente in coda Invia una risposta al chiamante in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="2f13b-107">There are a variety of ways for a queued component to send a response back to its caller asynchronously.</span></span> <span data-ttu-id="2f13b-108">Ad esempio, potrebbe inviare un messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="2f13b-108">For example, it could send an email.</span></span> <span data-ttu-id="2f13b-109">In alternativa, il server potrebbe pubblicare eventi a regime di controllo libero a cui il client può eseguire la sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="2f13b-109">Alternatively, the server could publish loosely coupled events to which the client could subscribe.</span></span>

<span data-ttu-id="2f13b-110">Un altro modo per ottenere una risposta da un componente in coda eseguito su un server è che il client passi il metodo chiamato un oggetto notifica.</span><span class="sxs-lookup"><span data-stu-id="2f13b-110">Another way for a client to obtain a response from a queued component that runs on a server is for the client to pass the called method a notification object.</span></span> <span data-ttu-id="2f13b-111">Un oggetto notifica è un'istanza di un componente in coda eseguito nel client.</span><span class="sxs-lookup"><span data-stu-id="2f13b-111">A notification object is an instance of a queued component that runs on the client.</span></span> <span data-ttu-id="2f13b-112">Un oggetto di notifica di questo tipo potrebbe essere piuttosto semplice, che contiene solo un numero intero usato per rappresentare un valore di errore o potrebbe essere piuttosto complesso, che contiene tutte le informazioni necessarie per eseguire il rollback di una transazione nel client.</span><span class="sxs-lookup"><span data-stu-id="2f13b-112">Such a notification object might be quite simple, containing only an integer that is used to represent an error value, or it might be quite complex, containing all the information necessary to roll back a transaction on the client.</span></span> <span data-ttu-id="2f13b-113">In entrambi i casi, il client chiamante passa un oggetto notifica come parametro di input quando si desidera una risposta da un componente in coda eseguito in un server.</span><span class="sxs-lookup"><span data-stu-id="2f13b-113">In either case, the calling client passes a notification object as an input parameter whenever it desires a response from a queued component that runs on a server.</span></span> <span data-ttu-id="2f13b-114">Poiché l'oggetto notifica viene accodato, il server può chiamare sui relativi metodi per modificarne lo stato, che può essere successivamente letto dal client.</span><span class="sxs-lookup"><span data-stu-id="2f13b-114">Because the notification object is queued, the server can call on its methods to alter its state, which can subsequently be read out by the client.</span></span> <span data-ttu-id="2f13b-115">In questo scenario, il servizio componenti in coda COM+ viene utilizzato sia sul client che sul server per consentire la comunicazione asincrona in entrambe le direzioni.</span><span class="sxs-lookup"><span data-stu-id="2f13b-115">In this scenario, the COM+ queued components service is used on both the client and the server to allow asynchronous communication in both directions.</span></span>

 

 



