---
description: In Windows XP, la configurazione per applicazione esegue l'override sia della configurazione predefinita che della configurazione dell'editore per ogni applicazione.
ms.assetid: 5b55d12d-8805-4820-91af-5ef583de3463
title: Configurazione per applicazione in Windows XP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9f07860a42951e073403e8145037074c35e6ec6a267736381f6beab385f3bb2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127461"
---
# <a name="per-application-configuration-on-windows-xp"></a>Configurazione per applicazione in Windows XP

In Windows XP, la configurazione per applicazione [](default-configuration.md) esegue [](publisher-configuration.md) l'override sia della configurazione predefinita che della configurazione dell'editore per ogni applicazione. In questo modo la dipendenza di un'applicazione specifica viene reindirizzata da una versione di un assembly side-by-side a un'altra versione specificata dell'assembly.

> [!Note]  
> A partire da Windows Server 2003, la [](publisher-configuration.md) configurazione per applicazione esegue l'override della configurazione dell'editore per ogni applicazione solo se il [file](application-configuration-files.md) di configurazione dell'applicazione specifica *apply="no"* in **publisherPolicy** ed è presente una voce corrispondente nel database di compatibilità dell'applicazione. La configurazione per applicazione esegue sempre l'override [della configurazione predefinita](default-configuration.md). Per informazioni, vedere [Configurazione per applicazione](per-application-configuration.md).

 

Una configurazione per applicazione può diventare necessaria se il corretto funzionamento di una determinata applicazione richiede una versione dell'assembly diversa da quella normalmente specificata come configurazione predefinita o dell'editore. Ad esempio, un aggiornamento globale della versione dell'assembly da parte dell'editore potrebbe correggere l'assembly ma interrompere questa particolare applicazione. In questo caso, è possibile usare la configurazione per applicazione per consentire all'applicazione di continuare l'esecuzione con la versione precedente dell'assembly. Un altro esempio, un'installazione del [](publisher-configuration.md) Service Pack contenente un aggiornamento dell'assembly potrebbe usare la configurazione dell'editore per reindirizzare le dipendenze di tutte le applicazioni e gli assembly nel sistema dalla versione 1.0.0.0 alla 1.0.1.0. Se è presente un'applicazione che richiede la versione 1.0.0.0 per il corretto funzionamento, è possibile reindirizzarla alla versione 1.0.0.0 usando la configurazione per applicazione.

Gli amministratori delle applicazioni possono implementare una configurazione per ogni applicazione mediante la creazione e l'installazione di [file di configurazione dell'applicazione](application-configuration-files.md). In questo modo un'applicazione specifica viene reindirizzata dalla dipendenza da una versione di un assembly side-by-side alla dipendenza da un'altra versione. [*I file di configurazione*](/windows/desktop/Msi/a-gly) dell'applicazione [possono](publisher-configuration-files.md) eseguire l'override dei file di configurazione dell'editore e della configurazione predefinita specificata dai [manifesti dell'applicazione](application-manifests.md) e [dai manifesti dell'assembly](assembly-manifests.md). Il file di configurazione dell'applicazione include le informazioni usate dal caricatore quando [**viene chiamato CreateProcess.**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)

Per configurare un'applicazione per eseguire l'override sia del manifesto dell'applicazione che della configurazione dell'editore, uno sviluppatore deve creare un file di configurazione dell'applicazione. Il file di configurazione dell'applicazione viene quindi distribuito e installato nella stessa cartella del file eseguibile dell'applicazione. Per un elenco dello schema di file, vedere [Schema del file di configurazione dell'applicazione](application-configuration-file-schema.md).

Si noti che se l'applicazione usa la configurazione per applicazione, non riceverà correzioni di sicurezza importanti o correzioni di bug che l'autore dell'assembly potrebbe rilasciare come file di configurazione dell'editore. Un'applicazione che usa la configurazione per applicazione può pertanto rimanere non sicura o continuare a funzionare in modo non corretto anche dopo l'applicazione di un nuovo assembly con queste correzioni al sistema. Per questo motivo, gli sviluppatori di applicazioni non devono mai spedire un'applicazione con una configurazione per applicazione. La configurazione per applicazione deve essere usata dagli amministratori aziendali come correzione temporanea solo quando l'applicazione viene interrotta da una configurazione dell'editore. In questo caso, la soluzione permanente è che gli sviluppatori dell'assembly e gli sviluppatori dell'applicazione dovranno collaborare per garantire che gli assembly con la configurazione dell'editore siano completamente compatibili con le versioni precedenti.

Di seguito è riportato un esempio di un file di configurazione dell'applicazione. Per altre informazioni, vedere [File di configurazione dell'applicazione](application-configuration-files.md).

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

 

 
