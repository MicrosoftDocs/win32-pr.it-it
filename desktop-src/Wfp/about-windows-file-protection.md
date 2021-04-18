---
description: Protezione risorse di Windows (WRP) impedisce la sostituzione dei file di sistema essenziali, delle cartelle e delle chiavi del registro di sistema installate come parte del sistema operativo.
ms.assetid: 39069f57-d9f6-4890-ba87-37175184d7a2
title: Informazioni su Protezione risorse di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c102225a547c4e454c3fb67ac94f715cd3adf8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317026"
---
# <a name="about-windows-resource-protection"></a><span data-ttu-id="887fe-103">Informazioni su Protezione risorse di Windows</span><span class="sxs-lookup"><span data-stu-id="887fe-103">About Windows Resource Protection</span></span>

<span data-ttu-id="887fe-104">Protezione risorse di Windows (WRP) impedisce la sostituzione dei file di sistema essenziali, delle cartelle e delle chiavi del registro di sistema installate come parte del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="887fe-104">Windows Resource Protection (WRP) prevents the replacement of essential system files, folders, and registry keys that are installed as part of the operating system.</span></span> <span data-ttu-id="887fe-105">È diventato disponibile a partire da Windows Server 2008 e Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="887fe-105">It became available starting with Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="887fe-106">L'autorizzazione per l'accesso completo per modificare le risorse protette con WRP è limitata a TrustedInstaller.</span><span class="sxs-lookup"><span data-stu-id="887fe-106">Permission for full access to modify WRP-protected resources is restricted to TrustedInstaller.</span></span> <span data-ttu-id="887fe-107">Le risorse protette da WRP possono essere modificate solo usando i [meccanismi di sostituzione delle risorse supportati](supported-file-replacement-mechanisms.md) con il servizio moduli di installazione di Windows.</span><span class="sxs-lookup"><span data-stu-id="887fe-107">WRP-protected resources can only be changed using the [Supported Resource Replacement Mechanisms](supported-file-replacement-mechanisms.md) with the Windows Modules Installer service.</span></span> <span data-ttu-id="887fe-108">La protezione di queste risorse impedisce gli errori dell'applicazione e del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="887fe-108">Protecting these resources prevents application and operating system failures.</span></span>

<span data-ttu-id="887fe-109">Le applicazioni non devono tentare di modificare le risorse protette da WRP perché vengono usate da Windows e da altre applicazioni.</span><span class="sxs-lookup"><span data-stu-id="887fe-109">Applications should not attempt to modify WRP-protected resources because these are used by Windows and other applications.</span></span> <span data-ttu-id="887fe-110">Se un'applicazione tenta di modificare una risorsa protetta da WRP, può presentare i risultati seguenti.</span><span class="sxs-lookup"><span data-stu-id="887fe-110">If an application attempts to modify a WRP-protected resource, it can have the following results.</span></span>

-   <span data-ttu-id="887fe-111">I programmi di installazione di applicazioni che tentano di sostituire, modificare o eliminare file di Windows critici o chiavi del registro di sistema potrebbero non essere in grado di installare l'applicazione e riceveranno un messaggio di errore che informa che l'accesso alla risorsa è stato negato.</span><span class="sxs-lookup"><span data-stu-id="887fe-111">Application installers that attempt to replace, modify, or delete critical Windows files or registry keys may fail to install the application and will receive an error message stating that access to the resource was denied.</span></span>
-   <span data-ttu-id="887fe-112">Le applicazioni che tentano di aggiungere o rimuovere sottochiavi o modificare i valori delle chiavi del registro di sistema protette potrebbero avere esito negativo e riceveranno un messaggio di errore che informa che l'accesso alla risorsa è stato negato.</span><span class="sxs-lookup"><span data-stu-id="887fe-112">Applications that attempt to add or remove sub-keys or change the values of protected registry keys may fail and will receive an error message stating that access to the resource was denied.</span></span>
-   <span data-ttu-id="887fe-113">Le applicazioni che si basano sulla scrittura di informazioni in chiavi del registro di sistema protette, cartelle o file potrebbero avere esito negativo.</span><span class="sxs-lookup"><span data-stu-id="887fe-113">Applications that rely on writing any information into protected registry keys, folders, or files may fail.</span></span>

<span data-ttu-id="887fe-114">WRP è il nuovo nome per la protezione dei file di Windows (WFP).</span><span class="sxs-lookup"><span data-stu-id="887fe-114">WRP is the new name for Windows File Protection (WFP).</span></span> <span data-ttu-id="887fe-115">WRP protegge le chiavi del registro di sistema e le cartelle, nonché i file di sistema essenziali.</span><span class="sxs-lookup"><span data-stu-id="887fe-115">WRP protects registry keys and folders as well as essential system files.</span></span> <span data-ttu-id="887fe-116">Pam era disponibile in Microsoft Windows Server 2003 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="887fe-116">WFP was available in Microsoft Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="887fe-117">WRP sostituisce WFP in Windows Server 2008 e Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="887fe-117">WRP replaces WFP in Windows Server 2008 and Windows Vista.</span></span>

<span data-ttu-id="887fe-118">Gli argomenti seguenti descrivono WRP:</span><span class="sxs-lookup"><span data-stu-id="887fe-118">The following topics describe WRP:</span></span>

-   [<span data-ttu-id="887fe-119">Elenco delle risorse protette</span><span class="sxs-lookup"><span data-stu-id="887fe-119">Protected Resource List</span></span>](protected-file-list.md)
-   [<span data-ttu-id="887fe-120">Rilevamento della sostituzione delle risorse</span><span class="sxs-lookup"><span data-stu-id="887fe-120">Detecting Resource Replacement</span></span>](detecting-file-replacement.md)
-   [<span data-ttu-id="887fe-121">Meccanismi di sostituzione delle risorse supportati</span><span class="sxs-lookup"><span data-stu-id="887fe-121">Supported Resource Replacement Mechanisms</span></span>](supported-file-replacement-mechanisms.md)
-   [<span data-ttu-id="887fe-122">Controllo file di sistema</span><span class="sxs-lookup"><span data-stu-id="887fe-122">System File Checker</span></span>](system-file-checker.md)
-   [<span data-ttu-id="887fe-123">Considerazioni sull'amministrazione remota</span><span class="sxs-lookup"><span data-stu-id="887fe-123">Remote Administration Considerations</span></span>](remote-administration-considerations.md)

 

 



