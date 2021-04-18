---
description: I tre tipi di spazi dei nomi in Windows Sockets (Winsock) SPI includono gli spazi dei nomi dinamici, statici e permanenti.
ms.assetid: 2968ac98-bd40-4d37-9dd7-7870c4decd40
title: Tipi di spazi dei nomi in SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e40356987c67604755696f1a8b7224de15851ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315762"
---
# <a name="types-of-namespaces-in-the-spi"></a><span data-ttu-id="fe0fd-103">Tipi di spazi dei nomi in SPI</span><span class="sxs-lookup"><span data-stu-id="fe0fd-103">Types of Namespaces in the SPI</span></span>

<span data-ttu-id="fe0fd-104">Sono disponibili tre tipi diversi di spazi dei nomi in cui è possibile registrare un servizio:</span><span class="sxs-lookup"><span data-stu-id="fe0fd-104">There are three different types of namespaces in which a service could be registered:</span></span>

-   <span data-ttu-id="fe0fd-105">Dynamic</span><span class="sxs-lookup"><span data-stu-id="fe0fd-105">Dynamic</span></span>
-   <span data-ttu-id="fe0fd-106">Static</span><span class="sxs-lookup"><span data-stu-id="fe0fd-106">Static</span></span>
-   <span data-ttu-id="fe0fd-107">Persistente</span><span class="sxs-lookup"><span data-stu-id="fe0fd-107">Persistent</span></span>

<span data-ttu-id="fe0fd-108">Gli spazi dei nomi dinamici consentono ai servizi di registrarsi allo spazio dei nomi in tempo reale e ai client di individuare i servizi disponibili in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="fe0fd-108">Dynamic namespaces allow services to register with the namespace on the fly, and for clients to discover the available services at run time.</span></span> <span data-ttu-id="fe0fd-109">Gli spazi dei nomi dinamici si basano spesso sulle trasmissioni per indicare la disponibilità continua di un servizio di rete.</span><span class="sxs-lookup"><span data-stu-id="fe0fd-109">Dynamic namespaces frequently rely on broadcasts to indicate the continued availability of a network service.</span></span> <span data-ttu-id="fe0fd-110">Esempi di spazi dei nomi dinamici includono lo spazio dei nomi SAP usato in un ambiente NetWare e lo spazio dei nomi avvio usato da AppleTalk.</span><span class="sxs-lookup"><span data-stu-id="fe0fd-110">Examples of dynamic namespaces include the SAP namespace used within a NetWare environment and the NBP namespace used by AppleTalk.</span></span>

<span data-ttu-id="fe0fd-111">Gli spazi dei nomi statici richiedono la registrazione di tutti i servizi in anticipo, ovvero quando viene creato lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="fe0fd-111">Static namespaces require all of the services to be registered ahead of time, that is, when the namespace is created.</span></span> <span data-ttu-id="fe0fd-112">Il DNS è un esempio di uno spazio dei nomi statico.</span><span class="sxs-lookup"><span data-stu-id="fe0fd-112">The DNS is an example of a static namespace.</span></span> <span data-ttu-id="fe0fd-113">Sebbene esista un metodo programmatico per la risoluzione dei nomi, non esiste alcun modo programmatico per registrare i nomi.</span><span class="sxs-lookup"><span data-stu-id="fe0fd-113">Although there is a programmatic way to resolve names, there is no programmatic way to register names.</span></span>

<span data-ttu-id="fe0fd-114">Gli spazi dei nomi permanenti consentono ai servizi di eseguire la registrazione con lo spazio dei nomi in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="fe0fd-114">Persistent namespaces allow services to register with the namespace on the fly.</span></span> <span data-ttu-id="fe0fd-115">A differenza degli spazi dei nomi dinamici, tuttavia, gli spazi dei nomi persistenti conservano le informazioni di registrazione in una risorsa di archiviazione non volatile dove rimangono fino al momento in cui il servizio richiede la rimozione.</span><span class="sxs-lookup"><span data-stu-id="fe0fd-115">Unlike dynamic namespaces however, persistent namespaces retain the registration information in nonvolatile storage where it remains until such time as the service requests that it be removed.</span></span> <span data-ttu-id="fe0fd-116">Gli spazi dei nomi permanenti sono caratterizzati da servizi directory quali X. 500 e NDS (servizio directory NetWare).</span><span class="sxs-lookup"><span data-stu-id="fe0fd-116">Persistent namespaces are typified by directory services such as X.500 and the NDS (NetWare Directory Service).</span></span> <span data-ttu-id="fe0fd-117">Questi ambienti consentono l'aggiunta, l'eliminazione e la modifica delle proprietà del servizio.</span><span class="sxs-lookup"><span data-stu-id="fe0fd-117">These environments allow the adding, deleting, and modification of service properties.</span></span> <span data-ttu-id="fe0fd-118">Inoltre, l'oggetto servizio che rappresenta il servizio all'interno del servizio directory potrebbe avere un'ampia gamma di attributi associati al servizio.</span><span class="sxs-lookup"><span data-stu-id="fe0fd-118">In addition, the service object representing the service within the directory service could have a variety of attributes associated with the service.</span></span> <span data-ttu-id="fe0fd-119">L'attributo più importante per le applicazioni client è le informazioni di indirizzamento del servizio.</span><span class="sxs-lookup"><span data-stu-id="fe0fd-119">The most important attribute for client applications is the service's addressing information.</span></span>

 

 



