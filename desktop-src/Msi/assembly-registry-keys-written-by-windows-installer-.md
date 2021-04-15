---
description: Se un pacchetto di Windows Installer installa o annuncia assembly, il programma di installazione archivia le informazioni su tali assembly nel registro di sistema locale.
ms.assetid: 1a6b0530-b5ad-49db-bc08-5b20d32420ef
title: Chiavi del registro di sistema dell'assembly scritte da Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bdd2ea7d290659fa9c1578d89be9a77dcc5cc10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528867"
---
# <a name="assembly-registry-keys-written-by-windows-installer"></a><span data-ttu-id="6c5ee-103">Chiavi del registro di sistema dell'assembly scritte da Windows Installer</span><span class="sxs-lookup"><span data-stu-id="6c5ee-103">Assembly Registry Keys Written by Windows Installer</span></span>

<span data-ttu-id="6c5ee-104">Se un pacchetto di Windows Installer installa o annuncia assembly, il programma di installazione archivia le informazioni su tali assembly nel registro di sistema locale.</span><span class="sxs-lookup"><span data-stu-id="6c5ee-104">If a Windows Installer package installs or advertises assemblies, the installer stores information about those assemblies in the local system registry.</span></span> <span data-ttu-id="6c5ee-105">Si noti che queste chiavi del registro di sistema sono destinate esclusivamente all'uso interno da Windows Installer e non devono essere basate sull'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6c5ee-105">Please note that these registry keys are only intended to be used internally by Windows Installer and they should not be relied upon by your application.</span></span> <span data-ttu-id="6c5ee-106">Il contenuto, la posizione e la struttura delle informazioni archiviate in queste chiavi sono soggette a modifiche.</span><span class="sxs-lookup"><span data-stu-id="6c5ee-106">The content, location, and structure of information stored in these keys is subject to change.</span></span> <span data-ttu-id="6c5ee-107">Le applicazioni devono basarsi su [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) per gestire gli assembly.</span><span class="sxs-lookup"><span data-stu-id="6c5ee-107">Applications should rely upon [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) to manage assemblies.</span></span>

<span data-ttu-id="6c5ee-108">Gli assembly vengono registrati con i rispettivi nomi di assembly.</span><span class="sxs-lookup"><span data-stu-id="6c5ee-108">Assemblies are registered by their assembly names.</span></span> <span data-ttu-id="6c5ee-109">I nomi dei valori archiviati nei percorsi seguenti sono i nomi degli assembly.</span><span class="sxs-lookup"><span data-stu-id="6c5ee-109">The names of the values stored in the following locations are the assembly names.</span></span> <span data-ttu-id="6c5ee-110">I valori effettivi sono di tipo REG \_ \_ multisz e contengono i dati utilizzati da [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) per installare o ripristinare gli assembly.</span><span class="sxs-lookup"><span data-stu-id="6c5ee-110">The actual values are of the type REG\_MULTI\_SZ and contain data used by [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) to install or repair assemblies.</span></span>

## <a name="information-about-private-assemblies"></a><span data-ttu-id="6c5ee-111">Informazioni sugli assembly privati</span><span class="sxs-lookup"><span data-stu-id="6c5ee-111">Information About Private Assemblies</span></span>

<span data-ttu-id="6c5ee-112">Windows Installer archivia le informazioni sugli assembly privati trasportati dai pacchetti Windows Installer installati come applicazioni per utente gestite con la seguente chiave del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="6c5ee-112">Windows Installer stores information about private assemblies carried by Windows Installer packages that have been installed as managed per-user applications under the following registry key:</span></span>

<span data-ttu-id="6c5ee-113">**HKLM** \\ **Software** \\ di **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Programma di installazione** \\ **Gestione** \\ di **SID *_\\_* utente** Percorso assembly del programma di installazione del \\  \\ \* *_file di configurazione_* _</span><span class="sxs-lookup"><span data-stu-id="6c5ee-113">**HKLM**\\**SOFTWARE**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Installer**\\**Managed**\\**_User SID_*_\\_\* Installer**\\**Assemblies**\\**_path to config file_* _</span></span>

<span data-ttu-id="6c5ee-114">Windows Installer archivia le informazioni sugli assembly privati trasferiti da Windows Installer pacchetti installati per utente con la seguente chiave del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="6c5ee-114">Windows Installer stores information about private assemblies carried by Windows Installer packages that have been installed per-user under the following registry key:</span></span>

<span data-ttu-id="6c5ee-115">_***\\** Percorso degli **\\** **\\** assembly di Microsoft Installer per HKCU Software per il **\\** **\\** _file di configurazione_*_</span><span class="sxs-lookup"><span data-stu-id="6c5ee-115">_*HKCU **\\** Software **\\** Microsoft **\\** Installer **\\** Assemblies **\\**_path to config file_*_</span></span>

<span data-ttu-id="6c5ee-116">Windows Installer archivia le informazioni sugli assembly privati trasferiti dai pacchetti Windows Installer e installati per computer con la seguente chiave del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="6c5ee-116">Windows Installer stores information about private assemblies carried by Windows Installer packages and installed per-machine under the following registry key:</span></span>

<span data-ttu-id="6c5ee-117">_***\\** Percorso degli **\\** assembly del programma di installazione delle classi Software HKLM **\\** **\\** **\\** _al file di configurazione_*_</span><span class="sxs-lookup"><span data-stu-id="6c5ee-117">_*HKLM **\\** SOFTWARE **\\** Classes **\\** Installer **\\** Assemblies **\\**_path to config file_*_</span></span>

## <a name="information-about-global-or-shared-assemblies"></a><span data-ttu-id="6c5ee-118">Informazioni sugli assembly globali o condivisi</span><span class="sxs-lookup"><span data-stu-id="6c5ee-118">Information About Global or Shared Assemblies</span></span>

<span data-ttu-id="6c5ee-119">Windows Installer archivia le informazioni sugli assembly condivisi trasportati dai pacchetti Windows Installer installati come applicazioni per utente gestite con la seguente chiave del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="6c5ee-119">Windows Installer stores information about shared assemblies carried by Windows Installer packages that have been installed as managed per-user applications under the following registry key:</span></span>

<span data-ttu-id="6c5ee-120">_*HKLM **\\** SOFTWARE **\\** Microsoft **\\** Windows **\\** CurrentVersion **\\** Installer **\\** Managed **\\** _User SID_*_ \\ _ *installazione **\\** assembly **\\** globali*\*</span><span class="sxs-lookup"><span data-stu-id="6c5ee-120">_*HKLM **\\** SOFTWARE **\\** Microsoft **\\** Windows **\\** CurrentVersion **\\** Installer **\\** Managed **\\**_User SID_*_\\_ *Installer **\\** Assemblies **\\** Global*\*</span></span>

<span data-ttu-id="6c5ee-121">Windows Installer archivia le informazioni sugli assembly condivisi trasferiti dai pacchetti Windows Installer installati per utente con la seguente chiave del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="6c5ee-121">Windows Installer stores information about shared assemblies carried by Windows Installer packages that have been installed per-user under the following registry key:</span></span>

<span data-ttu-id="6c5ee-122">**HKCU** \\ **Software** \\ di **Microsoft** \\ **Programma di installazione** \\ **Assembly** \\ **Globali**</span><span class="sxs-lookup"><span data-stu-id="6c5ee-122">**HKCU**\\**Software**\\**Microsoft**\\**Installer**\\**Assemblies**\\**Global**</span></span>

<span data-ttu-id="6c5ee-123">Windows Installer archivia le informazioni sugli assembly condivisi trasferiti dai pacchetti Windows Installer e installati per computer con la seguente chiave del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="6c5ee-123">Windows Installer stores information about shared assemblies carried by Windows Installer packages and installed per-machine under the following registry key:</span></span>

<span data-ttu-id="6c5ee-124">**HKLM** \\ **Software** \\ di **Classi** \\ **Programma di installazione** \\ **Assembly** \\ **Globali**</span><span class="sxs-lookup"><span data-stu-id="6c5ee-124">**HKLM**\\**SOFTWARE**\\**Classes**\\**Installer**\\**Assemblies**\\**Global**</span></span>

 

 



