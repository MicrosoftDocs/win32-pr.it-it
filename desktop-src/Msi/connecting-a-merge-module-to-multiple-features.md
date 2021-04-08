---
description: Il metodo Connect dell'oggetto merge può essere utilizzato per connettere un modulo a una funzionalità aggiuntiva che è stata unita nel database o che verrà unita nel database. La funzionalità deve esistere prima di chiamare questo metodo.
ms.assetid: 8b59de42-bc3f-468b-a410-8f935ff73345
title: Connessione di un modulo merge a più funzionalità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d57b49f1ee27b4c8d3aa5d0b3ac1b0d7b8b8e11c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883689"
---
# <a name="connecting-a-merge-module-to-multiple-features"></a><span data-ttu-id="9f9db-104">Connessione di un modulo merge a più funzionalità</span><span class="sxs-lookup"><span data-stu-id="9f9db-104">Connecting a Merge Module to Multiple Features</span></span>

<span data-ttu-id="9f9db-105">Il metodo [**Connect**](merge-connect.md) dell' [oggetto merge](merge-object.md) può essere utilizzato per connettere un modulo a una funzionalità aggiuntiva che è stata unita nel database o che verrà unita nel database.</span><span class="sxs-lookup"><span data-stu-id="9f9db-105">The [**Connect**](merge-connect.md) method of the [Merge Object](merge-object.md) can be used to connect a module to an additional feature that has been merged into the database or that will be merged into the database.</span></span> <span data-ttu-id="9f9db-106">La funzionalità deve esistere prima di chiamare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="9f9db-106">The feature must exist before calling this method.</span></span>

<span data-ttu-id="9f9db-107">Un modulo merge non deve mai recapitare un componente contenente file di sistema alla funzionalità principale di un'applicazione, perché ciò può causare la convalida e il ripristino dell'applicazione ogni volta che viene usato il file di sistema.</span><span class="sxs-lookup"><span data-stu-id="9f9db-107">A merge module should never deliver a component containing system files to the main feature of an application, because this may cause the Installer to validate and repair the application each time the system file is used.</span></span> <span data-ttu-id="9f9db-108">È necessario creare un file con estensione MSI progettato per accettare i componenti di un modulo merge in modo che tutti i componenti che contengono file di sistema appartengano solo a funzionalità distinte dalla funzionalità principale dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9f9db-108">A .msi file that is intended to accept components from a merge module should be authored so that any components that contain system files only belong to features that are separate from the main feature of the application.</span></span>

<span data-ttu-id="9f9db-109">Se il pacchetto usa un modulo merge contenente file di sistema che collegano tutti i componenti del modulo merge alla funzionalità principale dell'applicazione, un tentativo di usare il file di sistema potrebbe attivare il programma di installazione per provare a riparare la funzionalità principale dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9f9db-109">If your package uses a merge module containing system files that link all the components from the merge module to the main feature of the application, an attempt to use the system file may trigger the Installer to try and repair the main feature of the application.</span></span> <span data-ttu-id="9f9db-110">Se non è possibile ripristinare la funzionalità principale, l'installazione potrebbe non riuscire.</span><span class="sxs-lookup"><span data-stu-id="9f9db-110">If the main feature cannot be repaired, the installation may fail.</span></span>

 

 



