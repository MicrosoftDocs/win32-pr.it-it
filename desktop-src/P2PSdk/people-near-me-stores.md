---
description: Negozi di persone nelle vicinanze
ms.assetid: 3f2aa9bd-49ca-4fa6-b718-7cbeeef857c7
title: Negozi di persone nelle vicinanze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d18bf60e43aba278862fbd19f3c8909e344bc67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883338"
---
# <a name="people-near-me-stores"></a><span data-ttu-id="3cd3c-103">Negozi di persone nelle vicinanze</span><span class="sxs-lookup"><span data-stu-id="3cd3c-103">People Near Me Stores</span></span>

<span data-ttu-id="3cd3c-104">Le applicazioni in grado di [persone nelle vicinanze](about-people-near-me.md) (persone nelle vicinanze) possono usare gli archivi dati seguenti:</span><span class="sxs-lookup"><span data-stu-id="3cd3c-104">Applications capable of [People Near Me](about-people-near-me.md) (PNM) can use the following data stores:</span></span>

### <a name="windows-address-book"></a><span data-ttu-id="3cd3c-105">Rubrica di Windows</span><span class="sxs-lookup"><span data-stu-id="3cd3c-105">Windows Address Book</span></span>

<span data-ttu-id="3cd3c-106">La Rubrica di Windows archivia le informazioni sui contatti e i relativi certificati digitali.</span><span class="sxs-lookup"><span data-stu-id="3cd3c-106">The Windows Address Book stores information on contacts and their digital certificates.</span></span> <span data-ttu-id="3cd3c-107">Il contatto "**me**", che rappresenta l'utente attualmente connesso, viene archiviato anche nella Rubrica di Windows.</span><span class="sxs-lookup"><span data-stu-id="3cd3c-107">The '**Me**' contact, representing the currently logged in user, is also stored in the Windows Address Book.</span></span>

### <a name="certificate-store"></a><span data-ttu-id="3cd3c-108">Archivio certificati</span><span class="sxs-lookup"><span data-stu-id="3cd3c-108">Certificate Store</span></span>

<span data-ttu-id="3cd3c-109">L'archivio certificati contiene il certificato autofirmato per il contatto "**me**".</span><span class="sxs-lookup"><span data-stu-id="3cd3c-109">The Certificate Store contains the self-signed certificate for the '**Me**' contact.</span></span>

### <a name="application-store"></a><span data-ttu-id="3cd3c-110">Archivio applicazioni</span><span class="sxs-lookup"><span data-stu-id="3cd3c-110">Application Store</span></span>

<span data-ttu-id="3cd3c-111">Un programma di installazione dell'applicazione registra un'applicazione con persone nelle vicinanze durante il processo di installazione.</span><span class="sxs-lookup"><span data-stu-id="3cd3c-111">An application installer registers an application with PNM during the installation process.</span></span> <span data-ttu-id="3cd3c-112">Si tratta degli oggetti che possono essere cercati da altri utenti durante il tentativo di connessione a un utente con un'applicazione comune, ad esempio un gioco per computer.</span><span class="sxs-lookup"><span data-stu-id="3cd3c-112">These are the objects that can be searched for by other users when attempting to connect to a user with a common application, such as a computer game.</span></span> <span data-ttu-id="3cd3c-113">Per ogni applicazione, l'archivio applicazioni contiene il nome dell'applicazione, un identificatore univoco globale (GUID), un ambito dell'applicazione, una descrizione e un percorso del file eseguibile del programma.</span><span class="sxs-lookup"><span data-stu-id="3cd3c-113">For each application, the Application Store contains the name of the application, a globally unique identifier (GUID), a scope of the application, a description, and a path to the executable file of the program.</span></span> <span data-ttu-id="3cd3c-114">L'ambito di un'applicazione può essere impostato su None (non annunciato), persone nelle vicinanze (annunciate nella subnet locale), contatti (annunciati solo per contatti) o tutti (annunciati nella subnet locale e per i contatti).</span><span class="sxs-lookup"><span data-stu-id="3cd3c-114">The scope of an application can be set to None (not advertised), People Near Me (advertised on the local subnet), Contacts (advertised just for contacts), or All (advertised on the local subnet and for contacts).</span></span> <span data-ttu-id="3cd3c-115">L'archivio applicazioni si trova nel registro di sistema di Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3cd3c-115">The Application Store is located in the Windows Vista registry.</span></span>

 

 



