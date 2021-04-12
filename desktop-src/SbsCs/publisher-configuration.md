---
description: Un file di configurazione del server di pubblicazione reindirizza a livello globale le applicazioni e gli assembly che hanno una dipendenza da una versione di un assembly affiancato per usare un'altra versione dello stesso assembly.
ms.assetid: 9146c81e-8f43-4854-bbc4-1daaeb5fdda8
title: Configurazione del server di pubblicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c50ceb5263830cb1778aaaede673974cd7faca75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233297"
---
# <a name="publisher-configuration"></a><span data-ttu-id="4d19d-103">Configurazione del server di pubblicazione</span><span class="sxs-lookup"><span data-stu-id="4d19d-103">Publisher Configuration</span></span>

<span data-ttu-id="4d19d-104">Un [file di configurazione del server di pubblicazione](publisher-configuration-files.md) reindirizza a livello globale le applicazioni e gli assembly che hanno una dipendenza da una versione di un assembly affiancato per usare un'altra versione dello stesso assembly.</span><span class="sxs-lookup"><span data-stu-id="4d19d-104">A [publisher configuration file](publisher-configuration-files.md) globally redirects applications and assemblies having a dependence on one version of a side-by-side assembly to use another version of the same assembly.</span></span> <span data-ttu-id="4d19d-105">Ciò consente alle applicazioni e agli assembly di utilizzare l'assembly aggiornato senza dover ricompilare tutte le applicazioni interessate.</span><span class="sxs-lookup"><span data-stu-id="4d19d-105">This enables applications and assemblies to use the updated assembly without having to rebuild all of the affected applications.</span></span>

<span data-ttu-id="4d19d-106">I [file di configurazione del server di pubblicazione](publisher-configuration-files.md) possono essere forniti dall'autore di un assembly quando si emette una nuova versione dell'assembly con correzioni di bug compatibili o aggiornamenti della sicurezza.</span><span class="sxs-lookup"><span data-stu-id="4d19d-106">[Publisher configuration files](publisher-configuration-files.md) may be provided by the publisher of an assembly when issuing a new version of the assembly with compatible bug fixes or security updates.</span></span> <span data-ttu-id="4d19d-107">La versione aggiornata deve essere completamente compatibile con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="4d19d-107">The updated version should be fully backward compatible.</span></span> <span data-ttu-id="4d19d-108">Un file di configurazione dell'editore non deve mai essere usato per aggiungere nuove funzionalità, a meno che l'aggiornamento non sia completamente compatibile con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="4d19d-108">A publisher configuration file should never be used to add new features unless the update is fully backward compatible.</span></span> <span data-ttu-id="4d19d-109">I file di configurazione del server di pubblicazione non devono mai essere usati per incrementare la versione principale o secondaria di un assembly.</span><span class="sxs-lookup"><span data-stu-id="4d19d-109">Publisher configuration files should never be used to increment the major or minor version of an assembly.</span></span> <span data-ttu-id="4d19d-110">Ad esempio, non reindirizzare l'assembly versione 6.0.0.0 a 7.0.0.0 o versione 6.1.0.0.</span><span class="sxs-lookup"><span data-stu-id="4d19d-110">For example, do not redirect assembly version 6.0.0.0 to 7.0.0.0 or to 6.1.0.0.</span></span>

<span data-ttu-id="4d19d-111">I file di configurazione del server di pubblicazione devono essere emessi solo dal server di pubblicazione dell'assembly.</span><span class="sxs-lookup"><span data-stu-id="4d19d-111">Publisher configuration files should only be issued by the publisher of the assembly.</span></span> <span data-ttu-id="4d19d-112">Gli sviluppatori di assembly devono firmare gli assembly side-by-side condivisi e i file di configurazione del server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="4d19d-112">Assembly developers should sign shared side-by-side assemblies and publisher configuration files.</span></span> <span data-ttu-id="4d19d-113">Utilizzare la stessa chiave per firmare l'assembly e i file di configurazione del server di pubblicazione associato.</span><span class="sxs-lookup"><span data-stu-id="4d19d-113">Use the same key to sign the assembly and the associated publisher configuration files.</span></span> <span data-ttu-id="4d19d-114">I file di configurazione del server di pubblicazione devono essere firmati usando gli stessi strumenti usati per gli assembly, vedere [esempio di firma di assembly](assembly-signing-example.md) e creazione di [file e cataloghi firmati](creating-signed-files-and-catalogs.md).</span><span class="sxs-lookup"><span data-stu-id="4d19d-114">Publisher configuration files should be signed using the same tools as used for assemblies, see [Assembly Signing Example](assembly-signing-example.md) and [Creating Signed Files and Catalogs](creating-signed-files-and-catalogs.md).</span></span>

<span data-ttu-id="4d19d-115">In genere, la nuova versione di un assembly e il file di configurazione del server di pubblicazione associato verranno installati in un Service Pack aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="4d19d-115">Typically, the new version of an assembly and the associated publisher configuration file will be installed in a service pack update.</span></span> <span data-ttu-id="4d19d-116">I file di configurazione del server di pubblicazione non devono mai essere forniti con le applicazioni come ridistribuibili perché l'installazione di un file di configurazione del server di pubblicazione reindirizza globalmente gli assembly nel sistema.</span><span class="sxs-lookup"><span data-stu-id="4d19d-116">Publisher configuration files should never be provided with applications as a redistributable because installing a publisher configuration file globally redirects assemblies on the system.</span></span> <span data-ttu-id="4d19d-117">Se l'assembly in fase di aggiornamento viene fornito come ridistribuibile, il server di pubblicazione deve fornire entrambi gli elementi seguenti.</span><span class="sxs-lookup"><span data-stu-id="4d19d-117">If the assembly being updated is provided as a redistributable, the publisher should provide both of the following.</span></span>

-   <span data-ttu-id="4d19d-118">Un pacchetto di Windows Installer (file con estensione msi) che include la nuova versione dell'assembly con la configurazione del server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="4d19d-118">A Windows Installer package (.msi file) that includes the new version of the assembly with publisher configuration.</span></span> <span data-ttu-id="4d19d-119">Questo può essere installato come Service Pack o QFE perché in questo caso il cliente ha scelto di aggiornare il sistema a livello globale.</span><span class="sxs-lookup"><span data-stu-id="4d19d-119">This may be installed as a service pack or QFE because in this case the customer has chosen to globally update the system.</span></span> <span data-ttu-id="4d19d-120">Questa versione del pacchetto non deve mai essere installata dalle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="4d19d-120">This version of the package should never be installed by applications.</span></span>
-   <span data-ttu-id="4d19d-121">Un modulo Windows Installer Unione (file MSM) che include solo la nuova versione dell'assembly.</span><span class="sxs-lookup"><span data-stu-id="4d19d-121">A Windows Installer merge module (.msm file) that only includes the new version of the assembly.</span></span> <span data-ttu-id="4d19d-122">Questa versione può essere inclusa con le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="4d19d-122">This version may be included with applications.</span></span>

<span data-ttu-id="4d19d-123">Le applicazioni che richiedono una versione minima dell'assembly dovrebbero indicare la dipendenza dalla versione minima, se la versione minima non è disponibile in un sistema, l'applicazione non verrà avviata.</span><span class="sxs-lookup"><span data-stu-id="4d19d-123">Applications requiring a minimum version of the assembly should state their dependency on the minimum version, if the minimum version is unavailable on a system then the application will fail to start.</span></span> <span data-ttu-id="4d19d-124">Se è disponibile come ridistribuibile, è necessario che sia incluso nella configurazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4d19d-124">If it is available as a redistributable then it should be included in the application setup.</span></span>

<span data-ttu-id="4d19d-125">Ad esempio, l'installazione del seguente [file di configurazione del server di pubblicazione](publisher-configuration-files.md) reindirizza il binding dalla versione 2.0.0.0 di Microsoft. Windows. SampleAssembly alla versione 2.0.1.0.</span><span class="sxs-lookup"><span data-stu-id="4d19d-125">For example, installing the following [publisher configuration file](publisher-configuration-files.md) redirects binding from version 2.0.0.0 of the Microsoft.Windows.SampleAssembly to version 2.0.1.0.</span></span> <span data-ttu-id="4d19d-126">Verrà aggiunto un nuovo criterio, denominato 1.1.0.0. Policy, in% systemDrive% \\ Windows \\ WinSxS \\ Policies \\ x86 \_ policy. 2.0. Microsoft. Windows. SampleAssembly \_ 75e377300ab7b886 \_ x-ww \_ < *HashValue*>.</span><span class="sxs-lookup"><span data-stu-id="4d19d-126">This adds a new policy, named 1.1.0.0.Policy, under %systemDrive%\\windows\\winsxs\\policies\\x86\_policy.2.0.Microsoft.Windows.SampleAssembly\_75e377300ab7b886\_x-ww\_<*hashvalue*>.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
   <assemblyIdentity type="win32-policy" publicKeyToken="0000000000000000" name="policy.2.0.Microsoft.Windows.SampleAssembly" version="1.1.0.0" processorArchitecture="x86"/>
   <dependency>
      <dependentAssembly>
         <assemblyIdentity type="win32" name="Microsoft.Windows.SampleAssembly"  processorArchitecture="x86" publicKeyToken="75e377300ab7b886"/>
         <bindingRedirect oldVersion="2.0.0.0" newVersion="2.0.1.0"/>
      </dependentAssembly>
   </dependency>
</assembly>
```

<span data-ttu-id="4d19d-127">L'installazione del file di configurazione del server di pubblicazione seguente per lo stesso assembly reindirizza il binding dalla versione 2.0.0.0 di Microsoft. Windows. SampleAssembly alla versione 2.0.3.0.</span><span class="sxs-lookup"><span data-stu-id="4d19d-127">Installing the following publisher configuration file for the same assembly redirects binding from version 2.0.0.0 of the Microsoft.Windows.SampleAssembly to version 2.0.3.0.</span></span> <span data-ttu-id="4d19d-128">In questo modo viene aggiunto un altro criterio, denominato 2.1.0.0. Policy, in% systemDrive% \\ Windows \\ WinSxS \\ Policies \\ x86 \_ policy. 2.0. Microsoft. Windows. SampleAssembly \_ 75e377300ab7b886 \_ x-ww \_ < *HashValue*>.</span><span class="sxs-lookup"><span data-stu-id="4d19d-128">This adds another policy, named 2.1.0.0.Policy, under %systemDrive%\\windows\\winsxs\\policies\\x86\_policy.2.0.Microsoft.Windows.SampleAssembly\_75e377300ab7b886\_x-ww\_<*hashvalue*>.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
   <assemblyIdentity type="win32-policy" publicKeyToken="0000000000000000" name="policy.2.0.Microsoft.Windows.SampleAssembly" version="2.1.0.0" processorArchitecture="x86"/>
   <dependency>
      <dependentAssembly>
         <assemblyIdentity type="win32" name="Microsoft.Windows.SampleAssembly"  processorArchitecture="x86" publicKeyToken="75e377300ab7b886"/>
         <bindingRedirect oldVersion="2.0.0.0" newVersion="2.0.3.0"/>
      </dependentAssembly>
   </dependency>
</assembly>
```

 

 



