---
title: Linee guida relative alle prestazioni
description: Linee guida per lo sviluppo di applicazioni che offrono prestazioni ottimali in un ambiente Servizi Desktop remoto.
ms.assetid: 50f0c1f6-8046-4ceb-b2c4-6fc1ae86fd73
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ea7ada6ee2b51943d47f39446d0b1bb3b7d6718
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396819"
---
# <a name="performance-guidelines"></a><span data-ttu-id="cec90-103">Linee guida relative alle prestazioni</span><span class="sxs-lookup"><span data-stu-id="cec90-103">Performance guidelines</span></span>

<span data-ttu-id="cec90-104">Nelle sezioni seguenti vengono fornite le linee guida per lo sviluppo di applicazioni con prestazioni ottimali in un ambiente Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="cec90-104">The following sections provide guidelines for developing applications that perform well in a Remote Desktop Services environment.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="cec90-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="cec90-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="cec90-106">Effetti grafici</span><span class="sxs-lookup"><span data-stu-id="cec90-106">Graphic effects</span></span>](graphic-effects.md)
</dt> <dd>

<span data-ttu-id="cec90-107">Elenco di funzionalità che devono essere disabilitate durante l'esecuzione come sessione remota in un ambiente Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="cec90-107">A list of features that should be disabled when running as a remote session in a Remote Desktop Services environment.</span></span>

</dd> <dt>

[<span data-ttu-id="cec90-108">Linee guida per le attività in background in Servizi Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="cec90-108">Guidelines for background tasks in Remote Desktop Services</span></span>](background-tasks.md)
</dt> <dd>

<span data-ttu-id="cec90-109">Per ottimizzare la disponibilità della CPU per tutti gli utenti, disabilitare le attività in background durante l'esecuzione in un ambiente Servizi Desktop remoto o creare attività in background efficienti che non richiedono un uso intensivo delle risorse.</span><span class="sxs-lookup"><span data-stu-id="cec90-109">To maximize CPU availability for all users, either disable background tasks when running in a Remote Desktop Services environment or create efficient background tasks that are not resource-intensive.</span></span>

</dd> <dt>

[<span data-ttu-id="cec90-110">Utilizzo di thread</span><span class="sxs-lookup"><span data-stu-id="cec90-110">Thread usage</span></span>](thread-usage.md)
</dt> <dd>

<span data-ttu-id="cec90-111">È consigliabile ottimizzare e bilanciare l'utilizzo dei thread dell'applicazione per un ambiente multiutente Servizi Desktop remoto multiprocessore.</span><span class="sxs-lookup"><span data-stu-id="cec90-111">You should tune and balance application thread usage for a multiuser, multiprocessor Remote Desktop Services environment.</span></span>

</dd> <dt>

[<span data-ttu-id="cec90-112">Rilevamento dell'ambiente Servizi Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="cec90-112">Detecting the Remote Desktop Services environment</span></span>](detecting-the-terminal-services-environment.md)
</dt> <dd>

<span data-ttu-id="cec90-113">Per ottimizzare le prestazioni, è consigliabile che le applicazioni rilevino se sono in esecuzione in una sessione client Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="cec90-113">To optimize performance, it is good practice for applications to detect whether they are running in a Remote Desktop Services client session.</span></span>

</dd> </dl>

<span data-ttu-id="cec90-114">Verificare la presenza di perdite di memoria nell'applicazione e risolvere eventuali problemi.</span><span class="sxs-lookup"><span data-stu-id="cec90-114">Check your application for memory leaks and resolve any problems.</span></span> <span data-ttu-id="cec90-115">Naturalmente, questo è un valido Consiglio per qualsiasi applicazione, ma in un ambiente Servizi Desktop remoto un'applicazione può essere eseguita più volte da più utenti, in modo da ingrandire rapidamente l'effetto di una perdita di memoria.</span><span class="sxs-lookup"><span data-stu-id="cec90-115">Of course this is good advice for any application, but in a Remote Desktop Services environment, an application can be run multiple times by multiple users, thus rapidly magnifying the effect of a memory leak.</span></span>

<span data-ttu-id="cec90-116">È necessario configurare animazioni, immagini di grandi dimensioni, audio e altri servizi con utilizzo intensivo della larghezza di banda.</span><span class="sxs-lookup"><span data-stu-id="cec90-116">Animations, large images, audio, and other bandwidth-intensive services must be configurable.</span></span> <span data-ttu-id="cec90-117">Quando questi servizi non sono la funzione primaria, possono essere disattivati per impostazione predefinita per le sessioni remote, ma abilitati quando una sessione viene eseguita localmente o tramite una connessione a larghezza di banda elevata.</span><span class="sxs-lookup"><span data-stu-id="cec90-117">When these services are not the primary function, they can be off by default for remote sessions, but enabled when a session is running locally or over a high bandwidth connection.</span></span> <span data-ttu-id="cec90-118">Se lo scopo di un'applicazione è fornire servizi a larghezza di banda elevata, ad esempio trasmissioni video di streaming, non è necessario che il servizio sia disattivato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="cec90-118">If the purpose of an application is to provide high bandwidth services, such as streaming video broadcasts, the service does not have to be off by default.</span></span>

 

 




