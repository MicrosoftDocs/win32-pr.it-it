---
description: Rappresentazione della funzionalità
ms.assetid: 34a4a015-614d-4fac-98d8-29ae43165798
title: Rappresentazione della funzionalità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 101614592224a1a5ac079b1f9c3dc89cea9afefe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883149"
---
# <a name="representing-functionality"></a><span data-ttu-id="9f361-103">Rappresentazione della funzionalità</span><span class="sxs-lookup"><span data-stu-id="9f361-103">Representing Functionality</span></span>

<span data-ttu-id="9f361-104">Gli oggetti funzionali sono disponibili per identificare o raggruppare logicamente le funzionalità di un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9f361-104">Functional objects exist to identify or logically group feature capabilities of a device.</span></span> <span data-ttu-id="9f361-105">Ad esempio, un'applicazione può vedere che un dispositivo supporta SMS cercando l'oggetto funzionale SMS.</span><span class="sxs-lookup"><span data-stu-id="9f361-105">For example, an application can see that a device supports SMS by looking for the SMS functional object.</span></span> <span data-ttu-id="9f361-106">Analogamente, l'applicazione può verificare che un dispositivo disponga di funzionalità della fotocamera cercando l'oggetto funzionale Acquisisci immagine ancora.</span><span class="sxs-lookup"><span data-stu-id="9f361-106">Similarly, the application can see that a device has camera capabilities by looking for the Still Image Capture functional object.</span></span>

<span data-ttu-id="9f361-107">Questa rappresentazione flessibile degli oggetti consente un supporto semplice per i dispositivi con funzionalità multifunzione.</span><span class="sxs-lookup"><span data-stu-id="9f361-107">This flexible object representation helps enable easy support for devices with multi-function capabilities.</span></span> <span data-ttu-id="9f361-108">I driver possono semplicemente esporre gli oggetti funzionali che rappresentano il dispositivo, più granulare rispetto all'uso delle classi di dispositivi tradizionali.</span><span class="sxs-lookup"><span data-stu-id="9f361-108">Drivers can simply expose whatever functional objects represent their device, which is more granular than using traditional device classes.</span></span> <span data-ttu-id="9f361-109">La rappresentazione dell'oggetto consente inoltre di isolare le parti funzionali sovrapposte; ad esempio, alcuni telefoni possono avere due fotocamere o quattro archivi.</span><span class="sxs-lookup"><span data-stu-id="9f361-109">The object representation also helps isolate overlapping functional pieces; for example, some phones may have two cameras or four storages.</span></span>

<span data-ttu-id="9f361-110">Nel sistema operativo Windows 7 i servizi estendono gli oggetti funzionali fornendo query complete sulle funzionalità e un raggruppamento astratto di contenuti.</span><span class="sxs-lookup"><span data-stu-id="9f361-110">In the Windows 7 operating system, services extend functional objects by providing rich queries of capabilities and an abstract grouping of content.</span></span> <span data-ttu-id="9f361-111">Le applicazioni possono usare i servizi per individuare le funzionalità del dispositivo e interagire con il contenuto in modo più efficiente.</span><span class="sxs-lookup"><span data-stu-id="9f361-111">Applications can use services to discover device capabilities and to interact with content more efficiently.</span></span> <span data-ttu-id="9f361-112">Ad esempio, un'applicazione può verificare che un dispositivo supporti le funzionalità di sincronizzazione dei contatti cercando un oggetto servizio contatti e possa trovare tutti i contatti come oggetti figlio dell'oggetto servizio, senza dover eseguire ricerche ricorsive nella gerarchia di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="9f361-112">For example, an application can see that a device supports the contacts-synchronization capabilities by looking for a Contacts service object, and can find all contacts as child objects of the service object, without having to recursively search the storage hierarchy.</span></span>

<span data-ttu-id="9f361-113">I servizi consentono inoltre alle applicazioni di individuare e richiamare un comportamento personalizzato in un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9f361-113">Services also allow applications to discover and invoke custom behavior on a device.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9f361-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9f361-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f361-115">**Panoramica dell'applicazione**</span><span class="sxs-lookup"><span data-stu-id="9f361-115">**Application Overview**</span></span>](application-overview.md)
</dt> </dl>

 

 



