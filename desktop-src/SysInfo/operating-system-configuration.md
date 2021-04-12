---
description: La directory Windows è la directory che contiene le applicazioni basate su Windows, i file di inizializzazione e i file della guida. La funzione GetWindowsDirectory Recupera il percorso di questa directory.
ms.assetid: c07c6337-2c92-42c5-8283-c95637fcb85a
title: Configurazione del sistema operativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a38aa2c2b6b4f6b3ac5caac78a89ad980a9bd074
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232650"
---
# <a name="operating-system-configuration"></a><span data-ttu-id="cb680-104">Configurazione del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="cb680-104">Operating System Configuration</span></span>

<span data-ttu-id="cb680-105">La *directory Windows* è la directory che contiene le applicazioni basate su Windows, i file di inizializzazione e i file della guida.</span><span class="sxs-lookup"><span data-stu-id="cb680-105">The *Windows directory* is the directory that contains Windows-based applications, initialization files, and help files.</span></span> <span data-ttu-id="cb680-106">La funzione [**GetWindowsDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) Recupera il percorso di questa directory.</span><span class="sxs-lookup"><span data-stu-id="cb680-106">The [**GetWindowsDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) function retrieves the path to this directory.</span></span>

<span data-ttu-id="cb680-107">La *directory di sistema* è la directory che contiene le librerie a collegamento dinamico, i driver e i file del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="cb680-107">The *system directory* is the directory that contains dynamic-link libraries, drivers, and font files.</span></span> <span data-ttu-id="cb680-108">La funzione [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) Recupera il percorso di questa directory.</span><span class="sxs-lookup"><span data-stu-id="cb680-108">The [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) function retrieves the path to this directory.</span></span>

<span data-ttu-id="cb680-109">La funzione [**GetUserName**](/windows/desktop/api/Winbase/nf-winbase-getusernamea) Recupera il nome dell'utente attualmente connesso al sistema.</span><span class="sxs-lookup"><span data-stu-id="cb680-109">The [**GetUserName**](/windows/desktop/api/Winbase/nf-winbase-getusernamea) function retrieves the name of the user currently logged onto the system.</span></span> <span data-ttu-id="cb680-110">Il nome utente è il nome dell'account di accesso o il nome completo dell'utente, se quest'ultimo è incluso nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="cb680-110">The user name is either the logon name or the user's full name, if the latter is included in the registry.</span></span>

<span data-ttu-id="cb680-111">Una *variabile di ambiente* è una variabile simbolica che rappresenta un elemento del sistema, ad esempio un percorso, un nome di file o altri dati letterali.</span><span class="sxs-lookup"><span data-stu-id="cb680-111">An *environment variable* is a symbolic variable that represents some element of the system, such as a path, a file name, or other literal data.</span></span> <span data-ttu-id="cb680-112">Ad esempio, il percorso della variabile di ambiente rappresenta le directory in cui cercare i file eseguibili.</span><span class="sxs-lookup"><span data-stu-id="cb680-112">For example, the environment variable PATH represents the directories in which to search for executable files.</span></span> <span data-ttu-id="cb680-113">Quando un utente esegue l'accesso, il sistema Inizializza le variabili di ambiente in base alla sezione dell'ambiente del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="cb680-113">When a user logs on, the system initializes environment variables based on the environment section of the registry.</span></span> <span data-ttu-id="cb680-114">La funzione [**ExpandEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-expandenvironmentstringsa) recupera i valori delle variabili di ambiente specificate.</span><span class="sxs-lookup"><span data-stu-id="cb680-114">The [**ExpandEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-expandenvironmentstringsa) function retrieves the values of specified environment variables.</span></span>

<span data-ttu-id="cb680-115">Le informazioni aggiuntive sono fornite dall'interfaccia [**IADsADSystemInfo**](/windows/desktop/api/iads/nn-iads-iadsadsysteminfo) .</span><span class="sxs-lookup"><span data-stu-id="cb680-115">Additional information is provided by the [**IADsADSystemInfo**](/windows/desktop/api/iads/nn-iads-iadsadsysteminfo) interface.</span></span>

 

 
