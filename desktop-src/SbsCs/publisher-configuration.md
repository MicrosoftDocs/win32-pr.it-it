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
# <a name="publisher-configuration"></a>Configurazione del server di pubblicazione

Un [file di configurazione del server di pubblicazione](publisher-configuration-files.md) reindirizza a livello globale le applicazioni e gli assembly che hanno una dipendenza da una versione di un assembly affiancato per usare un'altra versione dello stesso assembly. Ciò consente alle applicazioni e agli assembly di utilizzare l'assembly aggiornato senza dover ricompilare tutte le applicazioni interessate.

I [file di configurazione del server di pubblicazione](publisher-configuration-files.md) possono essere forniti dall'autore di un assembly quando si emette una nuova versione dell'assembly con correzioni di bug compatibili o aggiornamenti della sicurezza. La versione aggiornata deve essere completamente compatibile con le versioni precedenti. Un file di configurazione dell'editore non deve mai essere usato per aggiungere nuove funzionalità, a meno che l'aggiornamento non sia completamente compatibile con le versioni precedenti. I file di configurazione del server di pubblicazione non devono mai essere usati per incrementare la versione principale o secondaria di un assembly. Ad esempio, non reindirizzare l'assembly versione 6.0.0.0 a 7.0.0.0 o versione 6.1.0.0.

I file di configurazione del server di pubblicazione devono essere emessi solo dal server di pubblicazione dell'assembly. Gli sviluppatori di assembly devono firmare gli assembly side-by-side condivisi e i file di configurazione del server di pubblicazione. Utilizzare la stessa chiave per firmare l'assembly e i file di configurazione del server di pubblicazione associato. I file di configurazione del server di pubblicazione devono essere firmati usando gli stessi strumenti usati per gli assembly, vedere [esempio di firma di assembly](assembly-signing-example.md) e creazione di [file e cataloghi firmati](creating-signed-files-and-catalogs.md).

In genere, la nuova versione di un assembly e il file di configurazione del server di pubblicazione associato verranno installati in un Service Pack aggiornamento. I file di configurazione del server di pubblicazione non devono mai essere forniti con le applicazioni come ridistribuibili perché l'installazione di un file di configurazione del server di pubblicazione reindirizza globalmente gli assembly nel sistema. Se l'assembly in fase di aggiornamento viene fornito come ridistribuibile, il server di pubblicazione deve fornire entrambi gli elementi seguenti.

-   Un pacchetto di Windows Installer (file con estensione msi) che include la nuova versione dell'assembly con la configurazione del server di pubblicazione. Questo può essere installato come Service Pack o QFE perché in questo caso il cliente ha scelto di aggiornare il sistema a livello globale. Questa versione del pacchetto non deve mai essere installata dalle applicazioni.
-   Un modulo Windows Installer Unione (file MSM) che include solo la nuova versione dell'assembly. Questa versione può essere inclusa con le applicazioni.

Le applicazioni che richiedono una versione minima dell'assembly dovrebbero indicare la dipendenza dalla versione minima, se la versione minima non è disponibile in un sistema, l'applicazione non verrà avviata. Se è disponibile come ridistribuibile, è necessario che sia incluso nella configurazione dell'applicazione.

Ad esempio, l'installazione del seguente [file di configurazione del server di pubblicazione](publisher-configuration-files.md) reindirizza il binding dalla versione 2.0.0.0 di Microsoft. Windows. SampleAssembly alla versione 2.0.1.0. Verrà aggiunto un nuovo criterio, denominato 1.1.0.0. Policy, in% systemDrive% \\ Windows \\ WinSxS \\ Policies \\ x86 \_ policy. 2.0. Microsoft. Windows. SampleAssembly \_ 75e377300ab7b886 \_ x-ww \_ < *HashValue*>.

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

L'installazione del file di configurazione del server di pubblicazione seguente per lo stesso assembly reindirizza il binding dalla versione 2.0.0.0 di Microsoft. Windows. SampleAssembly alla versione 2.0.3.0. In questo modo viene aggiunto un altro criterio, denominato 2.1.0.0. Policy, in% systemDrive% \\ Windows \\ WinSxS \\ Policies \\ x86 \_ policy. 2.0. Microsoft. Windows. SampleAssembly \_ 75e377300ab7b886 \_ x-ww \_ < *HashValue*>.

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

 

 



