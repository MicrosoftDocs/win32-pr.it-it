---
description: In Windows Vista e Windows Server 2008, i percorsi predefiniti per i dati utente e i dati di sistema sono stati modificati.
ms.assetid: 78679851-91f5-447f-8580-12cbf0323fb8
title: Punti di giunzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57f1823c67e2c6b95ae366b7604054b47305062e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310704"
---
# <a name="junction-points"></a><span data-ttu-id="cb4b0-103">Punti di giunzione</span><span class="sxs-lookup"><span data-stu-id="cb4b0-103">Junction Points</span></span>

<span data-ttu-id="cb4b0-104">In Windows Vista e Windows Server 2008, i percorsi predefiniti per i dati utente e i dati di sistema sono stati modificati.</span><span class="sxs-lookup"><span data-stu-id="cb4b0-104">In Windows Vista and Windows Server 2008, the default locations for user data and system data have changed.</span></span> <span data-ttu-id="cb4b0-105">Ad esempio, i dati utente archiviati in precedenza nella directory% SystemDrive% \\ Documents and Settings sono ora archiviati nella directory% SystemDrive% \\ Users.</span><span class="sxs-lookup"><span data-stu-id="cb4b0-105">For example, user data that was previously stored in the %SystemDrive%\\Documents and Settings directory is now stored in the %SystemDrive%\\Users directory.</span></span> <span data-ttu-id="cb4b0-106">Per compatibilità con le versioni precedenti, i percorsi precedenti hanno punti di giunzione che puntano alle nuove posizioni.</span><span class="sxs-lookup"><span data-stu-id="cb4b0-106">For backward compatibility, the old locations have junction points that point to the new locations.</span></span> <span data-ttu-id="cb4b0-107">Ad esempio, C: \\ Documents and Settings è ora un punto di giunzione che punta a c: \\ Users.</span><span class="sxs-lookup"><span data-stu-id="cb4b0-107">For example, C:\\Documents and Settings is now a junction point that points to C:\\Users.</span></span> <span data-ttu-id="cb4b0-108">Le applicazioni di backup devono essere in grado di eseguire il backup e il ripristino dei punti di giunzione.</span><span class="sxs-lookup"><span data-stu-id="cb4b0-108">Backup applications must be capable of backing up and restoring junction points.</span></span>

<span data-ttu-id="cb4b0-109">Questi punti di giunzione possono essere identificati come segue:</span><span class="sxs-lookup"><span data-stu-id="cb4b0-109">These junction points can be identified as follows:</span></span>

-   <span data-ttu-id="cb4b0-110">Hanno l'attributo file \_ \_ reparse \_ Point, l' \_ attributo file \_ Hidden e \_ \_ gli attributi file System attribute set.</span><span class="sxs-lookup"><span data-stu-id="cb4b0-110">They have the FILE\_ATTRIBUTE\_REPARSE\_POINT, FILE\_ATTRIBUTE\_HIDDEN, and FILE\_ATTRIBUTE\_SYSTEM file attributes set.</span></span>
-   <span data-ttu-id="cb4b0-111">Dispongono anche di elenchi di controllo di accesso (ACL) impostati per negare l'accesso in lettura a tutti.</span><span class="sxs-lookup"><span data-stu-id="cb4b0-111">They also have their access control lists (ACLs) set to deny read access to everyone.</span></span>

<span data-ttu-id="cb4b0-112">Le applicazioni che chiamano un percorso specifico possono attraversare questi punti di giunzione se dispongono delle autorizzazioni necessarie.</span><span class="sxs-lookup"><span data-stu-id="cb4b0-112">Applications that call out a specific path can traverse these junction points if they have the required permissions.</span></span> <span data-ttu-id="cb4b0-113">Tuttavia, i tentativi di enumerare il contenuto dei punti di giunzione provocheranno errori.</span><span class="sxs-lookup"><span data-stu-id="cb4b0-113">However, attempts to enumerate the contents of the junction points will result in failures.</span></span> <span data-ttu-id="cb4b0-114">È importante che le applicazioni di backup non attraversino questi punti di giunzione o tentino di eseguire il backup dei dati in essi contenuti, per due motivi:</span><span class="sxs-lookup"><span data-stu-id="cb4b0-114">It is important that backup applications do not traverse these junction points, or attempt to backup data under them, for two reasons:</span></span>

-   <span data-ttu-id="cb4b0-115">In questo modo, l'applicazione di backup può eseguire il backup degli stessi dati più di una volta.</span><span class="sxs-lookup"><span data-stu-id="cb4b0-115">Doing so can cause the backup application to back up the same data more than once.</span></span>
-   <span data-ttu-id="cb4b0-116">Può anche causare cicli (riferimenti circolari).</span><span class="sxs-lookup"><span data-stu-id="cb4b0-116">It can also lead to cycles (circular references).</span></span>

## <a name="per-user-junctions-and-system-junctions"></a><span data-ttu-id="cb4b0-117">Giunzioni di Per-User e giunzioni di sistema</span><span class="sxs-lookup"><span data-stu-id="cb4b0-117">Per-User Junctions and System Junctions</span></span>

<span data-ttu-id="cb4b0-118">I punti di giunzione utilizzati per fornire la virtualizzazione di file e registro di sistema in Windows Vista e Windows Server 2008 possono essere divisi in due classi: giunzioni per utente e giunzioni di sistema.</span><span class="sxs-lookup"><span data-stu-id="cb4b0-118">The junction points that are used to provide file and registry virtualization in Windows Vista and Windows Server 2008 can be divided into two classes: per-user junctions and system junctions.</span></span>

<span data-ttu-id="cb4b0-119">Le giunzioni per utente vengono create all'interno del profilo di ogni singolo utente per garantire la compatibilità con le versioni precedenti per le applicazioni utente.</span><span class="sxs-lookup"><span data-stu-id="cb4b0-119">Per-user junctions are created inside each individual user's profile to provide backward compatibility for user applications.</span></span> <span data-ttu-id="cb4b0-120">Il punto di giunzione in C: \\ Users \\ *nomeutente* i \\ documenti che puntano a c: \\ utenti \\ *nomeutente* \\ documenti è un esempio di giunzione per utente.</span><span class="sxs-lookup"><span data-stu-id="cb4b0-120">The junction point at C:\\Users\\*username*\\My Documents that points to C:\\Users\\*username*\\Documents is an example of a per-user junction.</span></span> <span data-ttu-id="cb4b0-121">Le giunzioni per utente vengono create dal servizio profili quando viene creato il profilo dell'utente.</span><span class="sxs-lookup"><span data-stu-id="cb4b0-121">Per-user junctions are created by the Profile service when the user's profile is created.</span></span>

<span data-ttu-id="cb4b0-122">Le altre giunzioni sono giunzioni di sistema che non risiedono nella \\ directory *username* degli utenti.</span><span class="sxs-lookup"><span data-stu-id="cb4b0-122">The other junctions are system junctions that do not reside under the Users\\*username* directory.</span></span> <span data-ttu-id="cb4b0-123">Esempi di giunzioni di sistema includono:</span><span class="sxs-lookup"><span data-stu-id="cb4b0-123">Examples of system junctions include:</span></span>

-   <span data-ttu-id="cb4b0-124">Documenti e impostazioni</span><span class="sxs-lookup"><span data-stu-id="cb4b0-124">Documents and Settings</span></span>
-   <span data-ttu-id="cb4b0-125">Giunzioni nei profili utente tutti gli utenti, pubblici e predefiniti</span><span class="sxs-lookup"><span data-stu-id="cb4b0-125">Junctions within the All Users, Public, and Default User profiles</span></span>

<span data-ttu-id="cb4b0-126">Le giunzioni di sistema vengono create da userenv.dll quando viene richiamato da Windows Welcome (noto anche come Machine out-of-Box-Experience o mOOBE).</span><span class="sxs-lookup"><span data-stu-id="cb4b0-126">System junctions are created by userenv.dll when it is invoked by Windows Welcome (also called the machine out-of-box-experience, or mOOBE).</span></span>

> [!Note]  
> <span data-ttu-id="cb4b0-127">Se l'utente modifica la lingua di sistema in una lingua diversa dall'inglese, i punti di giunzione per utente e sistema verranno creati con nomi localizzati.</span><span class="sxs-lookup"><span data-stu-id="cb4b0-127">If the user changes the system language to a language other than English, the per-user and system junction points will be created with localized names.</span></span>

 

 

 



