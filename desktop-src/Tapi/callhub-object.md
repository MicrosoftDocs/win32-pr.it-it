---
description: L'oggetto CallHub rappresenta una visualizzazione di terze parti di una chiamata a più parti.
ms.assetid: ea23ae25-2fbb-4060-8273-cd7921d49e52
title: Oggetto CallHub
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d43594db13c9175490b4cbb0941d1fb4e45b2ced
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967858"
---
# <a name="callhub-object"></a><span data-ttu-id="cb2fb-103">Oggetto CallHub</span><span class="sxs-lookup"><span data-stu-id="cb2fb-103">CallHub Object</span></span>

<span data-ttu-id="cb2fb-104">L'oggetto CallHub rappresenta una visualizzazione di terze parti di una chiamata a più parti.</span><span class="sxs-lookup"><span data-stu-id="cb2fb-104">The CallHub object represents a third-party view of a multiparty call.</span></span> <span data-ttu-id="cb2fb-105">Le interfacce e i metodi associati ottengono e impostano informazioni relative all'hub, ad esempio se è attivo.</span><span class="sxs-lookup"><span data-stu-id="cb2fb-105">The associated interfaces and methods get and set information concerning the hub, such as whether it is active.</span></span> <span data-ttu-id="cb2fb-106">Utilizzando l'oggetto CallHub, un utente con la sicurezza necessaria può individuare e potenzialmente controllare altri partecipanti in una chiamata.</span><span class="sxs-lookup"><span data-stu-id="cb2fb-106">Using the CallHub object, a user with the required security can discover and potentially control other participants in a call.</span></span>

<span data-ttu-id="cb2fb-107">Un oggetto CallHub non può essere creato direttamente da un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cb2fb-107">A CallHub object cannot be created directly by an application.</span></span> <span data-ttu-id="cb2fb-108">Un oggetto CallHub viene creato indirettamente quando viene ricevuta una chiamata in ingresso tramite TAPI 3.</span><span class="sxs-lookup"><span data-stu-id="cb2fb-108">A CallHub object is created indirectly when an incoming call is received through TAPI 3.</span></span>

<span data-ttu-id="cb2fb-109">TAPI 3 si basa sui provider di servizi TAPI per fornire le informazioni necessarie sulle chiamate da implementare utilizzando l'oggetto CallHub.</span><span class="sxs-lookup"><span data-stu-id="cb2fb-109">TAPI 3 relies on TAPI service providers to provide the necessary information about calls to implement using the CallHub object.</span></span> <span data-ttu-id="cb2fb-110">Poiché non tutti i provider di servizi forniscono queste informazioni e non tutti i componenti hardware supportano il rilevamento dell'hub delle chiamate, le informazioni disponibili sugli altri utenti della connessione possono essere limitate o inesistenti.</span><span class="sxs-lookup"><span data-stu-id="cb2fb-110">Because not all service providers provide this information, and not all hardware supports call hub tracking, the information available about the other users in the connection may be limited or nonexistent.</span></span>

<span data-ttu-id="cb2fb-111">L'esempio di codice per la [creazione di una conferenza semplice](create-a-simple-conference.md) illustra l'uso di un oggetto CallHub.</span><span class="sxs-lookup"><span data-stu-id="cb2fb-111">The [Create a Simple Conference](create-a-simple-conference.md) code example illustrates use of a CallHub object.</span></span>

<span data-ttu-id="cb2fb-112">Per un elenco di tutte le interfacce associate all'oggetto CallHub, vedere [interfacce oggetto CallHub](callhub-object-interfaces.md) .</span><span class="sxs-lookup"><span data-stu-id="cb2fb-112">See [CallHub Object Interfaces](callhub-object-interfaces.md) for a list of all interfaces associated with the CallHub object.</span></span>

 

 



