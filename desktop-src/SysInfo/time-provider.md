---
description: Il sistema operativo Microsoft Windows fornisce il supporto per un'ampia gamma di dispositivi hardware e protocolli di tempo di rete mediante l'architettura del provider di servizi temporali.
ms.assetid: a7575373-eeda-4f2a-85e5-d1b50994e7ae
title: Provider di servizi temporali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c844e2c4d0d49e87e978a47621338b167c4f5a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884025"
---
# <a name="time-provider"></a><span data-ttu-id="ffe58-103">Provider di servizi temporali</span><span class="sxs-lookup"><span data-stu-id="ffe58-103">Time Provider</span></span>

<span data-ttu-id="ffe58-104">Il sistema operativo Microsoft Windows fornisce il supporto per un'ampia gamma di dispositivi hardware e protocolli di tempo di rete mediante l'architettura del *provider di servizi temporali* .</span><span class="sxs-lookup"><span data-stu-id="ffe58-104">The Microsoft Windows operating system provides support for a variety of hardware devices and network time protocols using the *time provider* architecture.</span></span> <span data-ttu-id="ffe58-105">I provider del tempo di input recuperano timestamp accurati dall'hardware o dalla rete e i provider del tempo di output forniscono indicatori temporali ad altri client nella rete.</span><span class="sxs-lookup"><span data-stu-id="ffe58-105">Input time providers retrieve accurate time stamps from hardware or the network, and output time providers provide time stamps to other clients on the network.</span></span>

<span data-ttu-id="ffe58-106">I provider di tempo sono gestiti da *gestione provider di servizi temporali*.</span><span class="sxs-lookup"><span data-stu-id="ffe58-106">Time providers are managed by the *time provider manager*.</span></span> <span data-ttu-id="ffe58-107">È responsabile del caricamento, dell'avvio e dell'arresto dei provider di servizi temporali come indicato da Gestione controllo servizi.</span><span class="sxs-lookup"><span data-stu-id="ffe58-107">It is responsible for loading, starting, and stopping time providers as directed by the service control manager.</span></span> <span data-ttu-id="ffe58-108">Questa interfaccia rende più semplice la scrittura di un provider di tempo rispetto alla scrittura di un servizio completo.</span><span class="sxs-lookup"><span data-stu-id="ffe58-108">This interface makes writing a time provider easier than writing a full service.</span></span>

-   [<span data-ttu-id="ffe58-109">Creazione di un provider Time</span><span class="sxs-lookup"><span data-stu-id="ffe58-109">Creating a Time Provider</span></span>](creating-a-time-provider.md)
-   [<span data-ttu-id="ffe58-110">Registrazione di un provider Time</span><span class="sxs-lookup"><span data-stu-id="ffe58-110">Registering a Time Provider</span></span>](registering-a-time-provider.md)
-   [<span data-ttu-id="ffe58-111">Provider ora di esempio</span><span class="sxs-lookup"><span data-stu-id="ffe58-111">Sample Time Provider</span></span>](sample-time-provider.md)

## <a name="related-topics"></a><span data-ttu-id="ffe58-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ffe58-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ffe58-113">Servizio Ora di Windows</span><span class="sxs-lookup"><span data-stu-id="ffe58-113">Windows Time Service</span></span>](https://www.microsoft.com/technet/prodtechnol/windowsserver2003/technologies/security/ws03mngd/26_s3wts.mspx)
</dt> </dl>

 

 



