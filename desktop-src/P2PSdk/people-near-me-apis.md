---
description: API di persone nelle vicinanze
ms.assetid: 3b142d23-a9b2-465c-9bdc-484afbde154e
title: API di persone nelle vicinanze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 132d358a7d51a1069f7a4d1dc1ddfe2752dbdd1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967534"
---
# <a name="people-near-me-apis"></a><span data-ttu-id="c5809-103">API di persone nelle vicinanze</span><span class="sxs-lookup"><span data-stu-id="c5809-103">People Near Me APIs</span></span>

<span data-ttu-id="c5809-104">Tutte le applicazioni in grado di [persone nelle vicinanze](about-people-near-me.md) (persone nelle vicinanze) possono usare le API Win32 seguenti:</span><span class="sxs-lookup"><span data-stu-id="c5809-104">Any applications capable of [People Near Me](about-people-near-me.md) (PNM) can use the following Win32 APIs:</span></span>

### <a name="contacts-api"></a><span data-ttu-id="c5809-105">API contatti</span><span class="sxs-lookup"><span data-stu-id="c5809-105">Contacts API</span></span>

<span data-ttu-id="c5809-106">L'API Contacts viene usata per accedere alle informazioni di contatto per l'utente connesso, recuperare informazioni sui contatti archiviati in precedenza o archiviare le informazioni di contatto e il certificato digitale di un nuovo contatto.</span><span class="sxs-lookup"><span data-stu-id="c5809-106">The Contacts API is used to access the contact information for the logged on user, retrieve information about previously stored contacts, or store the contact information and digital certificate of a new contact.</span></span>

### <a name="people-near-me-api"></a><span data-ttu-id="c5809-107">API persone nelle vicinanze</span><span class="sxs-lookup"><span data-stu-id="c5809-107">People Near Me API</span></span>

<span data-ttu-id="c5809-108">L'API persone nelle vicinanze viene usata per trovare gli utenti vicini, i relativi interessi pubblicizzati, gli oggetti arbitrari che scelgono di pubblicare e le applicazioni annunciate.</span><span class="sxs-lookup"><span data-stu-id="c5809-108">The PNM API is used to find users nearby, their advertised interests, any arbitrary objects they choose to publish, and advertised applications.</span></span>

### <a name="publication-api"></a><span data-ttu-id="c5809-109">API di pubblicazione</span><span class="sxs-lookup"><span data-stu-id="c5809-109">Publication API</span></span>

<span data-ttu-id="c5809-110">L'API di pubblicazione viene utilizzata per interagire con i contatti remoti.</span><span class="sxs-lookup"><span data-stu-id="c5809-110">The Publication API is used to interact with remote contacts.</span></span> <span data-ttu-id="c5809-111">Il livello di [segnalazione peer](windows-peer-components-for-people-near-me.md) utilizzato dal gestore delle pubblicazioni viene utilizzato anche dal modulo persone nelle vicinanze per stabilire le connessioni.</span><span class="sxs-lookup"><span data-stu-id="c5809-111">The [Peer Signaling](windows-peer-components-for-people-near-me.md) layer used by the Publication Manager is also used by the PNM module for establishing connections.</span></span>

### <a name="invitation-api"></a><span data-ttu-id="c5809-112">API di invito</span><span class="sxs-lookup"><span data-stu-id="c5809-112">Invitation API</span></span>

<span data-ttu-id="c5809-113">L'API di invito viene utilizzata da un'applicazione di collaborazione per invitare peer specifici in un'attività di collaborazione.</span><span class="sxs-lookup"><span data-stu-id="c5809-113">The Invitation API is used by a collaboration application to invite specific peer(s) into a collaboration activity.</span></span>

### <a name="application-registration-api"></a><span data-ttu-id="c5809-114">API di registrazione dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="c5809-114">Application Registration API</span></span>

<span data-ttu-id="c5809-115">L'API di registrazione dell'applicazione viene usata dal programma di installazione di un'applicazione di collaborazione per registrare l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c5809-115">The Application Registration API is used by the installer of a collaboration application to register the application.</span></span> <span data-ttu-id="c5809-116">Un'applicazione con supporto per persone nelle vicinanze richiederà all'utente durante il processo di installazione di determinare se l'applicazione deve essere resa disponibile agli utenti nella subnet.</span><span class="sxs-lookup"><span data-stu-id="c5809-116">A PNM-capable application will prompt the user during the installation process to determine whether the application should be made available to users on the subnet.</span></span>

 

 



