---
description: In Windows XP, la configurazione per applicazione sostituisce la configurazione predefinita e la configurazione del server di pubblicazione per ogni singola applicazione.
ms.assetid: 5b55d12d-8805-4820-91af-5ef583de3463
title: Configurazione per applicazione in Windows XP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea6fa2e14e24e48be84247a23feecddf2784fbc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884538"
---
# <a name="per-application-configuration-on-windows-xp"></a>Configurazione per applicazione in Windows XP

In Windows XP, la configurazione per applicazione sostituisce la configurazione [predefinita](default-configuration.md) e la configurazione del [server di pubblicazione](publisher-configuration.md) per ogni singola applicazione. Questo consente di reindirizzare la dipendenza di un'applicazione specifica da una versione di un assembly affiancato a un'altra versione specificata dell'assembly.

> [!Note]  
> A partire da Windows Server 2003, la configurazione per applicazione esegue l'override della configurazione del server di [pubblicazione](publisher-configuration.md) in base alle singole applicazioni solo se il [file di configurazione dell'applicazione](application-configuration-files.md) specifica *Apply = "No"* in **publisherPolicy apply** ed è presente una voce corrispondente nel database di compatibilità delle applicazioni. La configurazione per applicazione esegue sempre l'override della [configurazione predefinita](default-configuration.md). Per informazioni, vedere [configurazione per ogni applicazione](per-application-configuration.md).

 

Una configurazione per ogni applicazione potrebbe essere necessaria se il corretto funzionamento di una particolare applicazione richiede una versione dell'assembly diversa rispetto alla versione normalmente specificata come configurazione predefinita o del server di pubblicazione. Ad esempio, un aggiornamento globale della versione dell'assembly da parte del server di pubblicazione potrebbe correggere l'assembly, ma interrompere questa particolare applicazione. In questo caso, è possibile usare la configurazione per applicazione per consentire all'applicazione di continuare a eseguire con la versione precedente dell'assembly. Un altro esempio: un'installazione di Service Pack contenente un aggiornamento dell'assembly può utilizzare la [configurazione del server di pubblicazione](publisher-configuration.md) per reindirizzare le dipendenze di tutte le applicazioni e degli assembly del sistema dalla versione 1.0.0.0 a 1.0.1.0. Se è presente un'applicazione che richiede il corretto funzionamento della versione 1.0.0.0, è possibile reindirizzarla alla versione 1.0.0.0 usando la configurazione per ogni applicazione.

Gli amministratori di applicazioni possono implementare una configurazione per ogni applicazione mediante la creazione e l'installazione dei [file di configurazione dell'applicazione](application-configuration-files.md). Questi reindirizza un'applicazione specifica dalla dipendenza da una versione di un assembly affiancato alla dipendenza da un'altra versione. I file di [*configurazione dell'applicazione*](/windows/desktop/Msi/a-gly) possono sostituire i [file di configurazione del server di pubblicazione](publisher-configuration-files.md) e la configurazione predefinita specificata dai [manifesti dell'applicazione](application-manifests.md) e dei [manifesti dell'assembly](assembly-manifests.md) Il file di configurazione dell'applicazione include le informazioni utilizzate dal caricatore quando [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) viene chiamato.

Per configurare un'applicazione in modo che esegua l'override del manifesto dell'applicazione e della configurazione del server di pubblicazione, uno sviluppatore deve creare un file di configurazione dell'applicazione. Il file di configurazione dell'applicazione viene quindi distribuito e installato nella stessa cartella del file eseguibile dell'applicazione. Per un elenco dello schema dei file, vedere [schema del file di configurazione dell'applicazione](application-configuration-file-schema.md).

Si noti che se l'applicazione usa la configurazione per applicazione, non riceverà eventuali correzioni di bug o correzioni di sicurezza importanti che l'autore dell'assembly potrebbe emettere come file di configurazione dell'editore. Un'applicazione che usa la configurazione per applicazione può pertanto rimanere non sicura o continuare a funzionare in modo non corretto anche dopo che un nuovo assembly con queste correzioni viene applicato al sistema. Per questo motivo, gli sviluppatori di applicazioni non devono mai spedire un'applicazione con una configurazione per ogni applicazione. La configurazione per applicazione deve essere usata solo dagli amministratori aziendali come correzione temporanea quando l'applicazione è interruppe da una configurazione del server di pubblicazione. In questo caso, la soluzione permanente consiste nel fare in modo che gli sviluppatori dell'assembly e gli sviluppatori dell'applicazione debbano collaborare per assicurarsi che gli assembly con la configurazione del server di pubblicazione siano completamente compatibili con le versioni precedenti.

Di seguito è riportato un esempio di un file di configurazione dell'applicazione. Per ulteriori informazioni, vedere [file di configurazione dell'applicazione](application-configuration-files.md).

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<configuration>
  <windows>
    <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">
      <assemblyIdentity 
          name="Microsoft.Windows.mysampleApp" 
          processorArchitecture="x86" 
          version="1.0.0.0" type="win32"/>
        <dependentAssembly>
          <assemblyIdentity type="win32" 
              name="Microsoft.Windows.SampleAssembly" 
              processorArchitecture="x86" 
              publicKeyToken="0000000000000000"/>
          <bindingRedirect 
              oldVersion="2.0.0.0" 
              newVersion="2.0.1.0"/>
        </dependentAssembly>
    </assemblyBinding>
   </windows>
</configuration>
```

 

 
