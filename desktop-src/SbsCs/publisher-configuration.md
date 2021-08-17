---
description: Un file di configurazione dell'editore reindirizza a livello globale le applicazioni e gli assembly che hanno una dipendenza da una versione di un assembly side-by-side per usare un'altra versione dello stesso assembly.
ms.assetid: 9146c81e-8f43-4854-bbc4-1daaeb5fdda8
title: Publisher Configurazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1134fa29775fc34384f5da19e660d91de10532110304caf8b6ecacbb92fec87e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141954"
---
# <a name="publisher-configuration"></a>Publisher Configurazione

Un [file di configurazione](publisher-configuration-files.md) dell'editore reindirizza a livello globale le applicazioni e gli assembly che hanno una dipendenza da una versione di un assembly side-by-side per usare un'altra versione dello stesso assembly. In questo modo le applicazioni e gli assembly possono usare l'assembly aggiornato senza dover ricompilare tutte le applicazioni interessate.

[Publisher](publisher-configuration-files.md) file di configurazione possono essere forniti dall'autore di un assembly quando si emette una nuova versione dell'assembly con correzioni di bug compatibili o aggiornamenti della sicurezza. La versione aggiornata deve essere completamente compatibile con le versioni precedenti. Un file di configurazione dell'editore non deve mai essere usato per aggiungere nuove funzionalità, a meno che l'aggiornamento non sia completamente compatibile con le versioni precedenti. Publisher file di configurazione non devono mai essere usati per incrementare la versione principale o secondaria di un assembly. Ad esempio, non reindirizzare la versione dell'assembly 6.0.0.0 a 7.0.0.0 o a 6.1.0.0.

Publisher file di configurazione devono essere rilasciati solo dall'autore dell'assembly. Gli sviluppatori di assembly devono firmare assembly side-by-side condivisi e file di configurazione dell'editore. Usare la stessa chiave per firmare l'assembly e i file di configurazione dell'editore associati. Publisher file di configurazione devono essere firmati usando gli stessi strumenti usati per gli assembly, vedere Esempio di firma degli [assembly](assembly-signing-example.md) e Creazione di file [e cataloghi firmati.](creating-signed-files-and-catalogs.md)

In genere, la nuova versione di un assembly e il file di configurazione dell'editore associato verranno installati in un aggiornamento del Service Pack. Publisher file di configurazione non devono mai essere forniti con le applicazioni come ridistribuibili perché l'installazione di un file di configurazione del server di pubblicazione reindirizza a livello globale gli assembly nel sistema. Se l'assembly da aggiornare viene fornito come ridistribuibile, il server di pubblicazione deve fornire entrambi gli elementi seguenti.

-   Pacchetto Windows Installer (file .msi) che include la nuova versione dell'assembly con la configurazione dell'editore. Può essere installato come Service Pack o QFE perché in questo caso il cliente ha scelto di aggiornare a livello globale il sistema. Questa versione del pacchetto non deve mai essere installata dalle applicazioni.
-   Un Windows merge del programma di installazione (file con estensione msm) che include solo la nuova versione dell'assembly. Questa versione può essere inclusa nelle applicazioni.

Le applicazioni che richiedono una versione minima dell'assembly devono determinare la dipendenza dalla versione minima. Se la versione minima non è disponibile in un sistema, l'applicazione non verrà avviata. Se è disponibile come ridistribuibile, deve essere incluso nella configurazione dell'applicazione.

Ad esempio, l'installazione del file di [configurazione](publisher-configuration-files.md) dell'editore seguente reindirizza l'associazione dalla versione 2.0.0.0 di Microsoft. Windows. SampleAssembly alla versione 2.0.1.0. Verrà aggiunto un nuovo criterio, denominato 1.1.0.0.Policy, in %systemDrive% \\ windows \\ winsxs \\ policies \\ x86 \_ policy.2.0.Microsoft.Windows. SampleAssembly \_ 75e377300ab7b886 \_ x-ww \_ < *hashvalue*>.

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

L'installazione del file di configurazione dell'editore seguente per lo stesso assembly reindirizza l'associazione dalla versione 2.0.0.0 di Microsoft. Windows. SampleAssembly alla versione 2.0.3.0. Verrà aggiunto un altro criterio, denominato 2.1.0.0.Policy, in %systemDrive% \\ windows \\ winsxs \\ policies \\ x86 \_ policy.2.0.Microsoft.Windows. SampleAssembly \_ 75e377300ab7b886 \_ x-ww \_ < *hashvalue*>.

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

 

 



