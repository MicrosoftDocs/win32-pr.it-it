---
description: Gli autori dei pacchetti di installazione possono specificare che il programma di installazione copia i file condivisi (dll comunemente condivise) di un'applicazione nella cartella di tale applicazione anziché in un percorso condiviso.
ms.assetid: eb5f7088-30e0-4644-813a-c93e6f56ccbf
title: Componenti isolati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f29f614dfd819e093c5729a9a97a076247d281d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750119"
---
# <a name="isolated-components"></a><span data-ttu-id="919ce-103">Componenti isolati</span><span class="sxs-lookup"><span data-stu-id="919ce-103">Isolated Components</span></span>

<span data-ttu-id="919ce-104">Gli autori dei pacchetti di installazione possono specificare che il programma di installazione copia i file condivisi (dll comunemente condivise) di un'applicazione nella cartella di tale applicazione anziché in un percorso condiviso.</span><span class="sxs-lookup"><span data-stu-id="919ce-104">Authors of installation packages can specify that the installer copy the shared files (commonly shared DLLs) of an application into that application's folder rather than to a shared location.</span></span> <span data-ttu-id="919ce-105">Questo set di file privato (dll) viene quindi usato solo dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="919ce-105">This private set of files (DLLs) are then used only by the application.</span></span> <span data-ttu-id="919ce-106">L'isolamento dell'applicazione insieme ai componenti condivisi in questo modo presenta i vantaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="919ce-106">Isolating the application together with its shared components in this manner has the following advantages:</span></span>

-   <span data-ttu-id="919ce-107">L'applicazione usa sempre le versioni dei file condivisi con cui è stata distribuita.</span><span class="sxs-lookup"><span data-stu-id="919ce-107">The application always uses the versions of the shared files with which it was deployed.</span></span>
-   <span data-ttu-id="919ce-108">L'installazione dell'applicazione non sovrascrive altre versioni dei file condivisi da altre applicazioni.</span><span class="sxs-lookup"><span data-stu-id="919ce-108">Installing the application does not overwrite other versions of the shared files by other applications.</span></span>
-   <span data-ttu-id="919ce-109">Le installazioni successive di altre applicazioni che utilizzano versioni diverse dei file condivisi non possono sovrascrivere i file utilizzati da questa applicazione.</span><span class="sxs-lookup"><span data-stu-id="919ce-109">Subsequent installations of other applications using different versions of the shared files cannot overwrite the files used by this application.</span></span>

<span data-ttu-id="919ce-110">Poiché l'implementazione corrente di COM mantiene un unico percorso completo nel registro di sistema per ogni coppia CLSID/contesto, impone a tutte le applicazioni di usare la stessa versione di una DLL condivisa.</span><span class="sxs-lookup"><span data-stu-id="919ce-110">Because the current implementation of COM keeps a single full path in the registry for each CLSID/Context pair, it forces all applications to use the same version of a shared DLL.</span></span> <span data-ttu-id="919ce-111">Per consentire a un'applicazione di memorizzare una copia privata di un server COM, il caricatore di sistema in Windows 2000 verifica la presenza di una. File locale nella cartella dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="919ce-111">To enable an application to keep a private copy of a COM server, the system loader in Windows 2000 checks for the presence of a .LOCAL file in the application's folder.</span></span> <span data-ttu-id="919ce-112">Se il caricatore di sistema rileva un oggetto. Il file locale modifica la logica di ricerca per preferire le dll che si trovano nella stessa cartella dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="919ce-112">If the system loader detects a .LOCAL file, it alters its search logic to prefer DLLs located in the same folder as the application.</span></span>

<span data-ttu-id="919ce-113">Quando Windows Installer esegue l' [azione IsolateComponents](isolatecomponents-action.md) , copiano i file del componente (in genere una DLL condivisa) specificata nella \_ colonna condivisa Component della [tabella IsolatedComponent](isolatedcomponent-table.md) nella stessa cartella del componente, in genere un file con estensione exe, specificato nella \_ colonna applicazione componente.</span><span class="sxs-lookup"><span data-stu-id="919ce-113">When Windows Installer runs the [IsolateComponents action](isolatecomponents-action.md) they copy the files of the component (commonly a shared DLL) specified in the Component\_Shared column of the [IsolatedComponent table](isolatedcomponent-table.md) into the same folder as the component (commonly an .exe file) specified in the Component\_Application column.</span></span> <span data-ttu-id="919ce-114">Il programma di installazione crea un file in questa directory, con una lunghezza pari a zero byte, con il nome di file breve del file di chiave per l' \_ applicazione componente (in genere il nome è lo stesso dell'applicazione con estensione exe) accodato con. Locale.</span><span class="sxs-lookup"><span data-stu-id="919ce-114">The installer creates a file in this directory, zero bytes in length, having the short file name of the key file for Component\_Application (typically the name is the same as the application's .exe) appended with .LOCAL.</span></span> <span data-ttu-id="919ce-115">Il programma di installazione usa la registrazione per il componente nel percorso condiviso e non scrive le informazioni di registrazione per la copia del componente nel percorso privato.</span><span class="sxs-lookup"><span data-stu-id="919ce-115">The installer uses the registration for the component in its shared location and does not write any registration information for the copy of the component in the private location.</span></span>

<span data-ttu-id="919ce-116">Per altre informazioni, vedere:</span><span class="sxs-lookup"><span data-stu-id="919ce-116">For more information, see:</span></span>

-   [<span data-ttu-id="919ce-117">Installazione di componenti isolati</span><span class="sxs-lookup"><span data-stu-id="919ce-117">Installation of Isolated Components</span></span>](installation-of-isolated-components.md)
-   [<span data-ttu-id="919ce-118">Reinstallazione dei componenti isolati</span><span class="sxs-lookup"><span data-stu-id="919ce-118">Reinstallation of Isolated Components</span></span>](reinstallation-of-isolated-components.md)
-   [<span data-ttu-id="919ce-119">Rimozione di componenti isolati</span><span class="sxs-lookup"><span data-stu-id="919ce-119">Removal of Isolated Components</span></span>](removal-of-isolated-components.md)
-   [<span data-ttu-id="919ce-120">Utilizzo di componenti isolati</span><span class="sxs-lookup"><span data-stu-id="919ce-120">Using Isolated Components</span></span>](using-isolated-components.md)

 

 



