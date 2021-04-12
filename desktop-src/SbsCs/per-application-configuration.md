---
description: La configurazione per applicazione reindirizza la dipendenza di una particolare applicazione da una versione di un assembly side-by-side a un'altra versione dell'assembly.
ms.assetid: b7988385-c87e-443c-8ec3-84ab3c172eab
title: Configurazione per applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b17543c9972deefe2a2beda1f5eeba1c5ace2ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233299"
---
# <a name="per-application-configuration"></a>Configurazione per applicazione

La configurazione per applicazione reindirizza la dipendenza di una particolare applicazione da una versione di un assembly side-by-side a un'altra versione dell'assembly. Una configurazione per ogni applicazione potrebbe essere necessaria se per il corretto funzionamento di una determinata applicazione è richiesta una versione dell'assembly diversa dalla versione normalmente specificata come configurazione [predefinita](default-configuration.md) o [configurazione del server di pubblicazione](publisher-configuration.md). Ad esempio, un aggiornamento globale della versione dell'assembly da parte del server di pubblicazione potrebbe correggere l'assembly, ma interrompere questa particolare applicazione. In questo caso, è possibile usare la configurazione per applicazione per consentire all'applicazione di continuare a eseguire con la versione precedente dell'assembly.

A partire da Windows Server 2003, la configurazione per applicazione esegue sempre l'override della [configurazione predefinita](default-configuration.md) per ogni singola applicazione. La configurazione per applicazione esegue l'override della [configurazione del server di pubblicazione](publisher-configuration.md) in base alle singole applicazioni solo se il file di [configurazione dell'applicazione](application-configuration-files.md) specifica *Apply = "No"* in **publisherPolicy apply** ed è presente una voce corrispondente nel database di compatibilità delle applicazioni.

> [!Note]  
> In Windows XP, la configurazione per applicazione sostituisce la configurazione [predefinita](default-configuration.md) e la configurazione del [server di pubblicazione](publisher-configuration.md) per ogni singola applicazione. Per informazioni, vedere [configurazione per ogni applicazione in Windows XP](per-application-configuration-on-windows-xp.md).

 

A partire da Windows Server 2003, una configurazione per applicazione eseguirà l'override di una [configurazione dell'editore](publisher-configuration.md) se il [file di configurazione dell'applicazione](application-configuration-files.md) specifica *Apply = "Yes"* in **publisherPolicy apply** e il flag EnableAppConfig è impostato per l'applicazione nel database di compatibilità delle applicazioni. Questa funzionalità consente di eseguire l'override di una configurazione del server di pubblicazione utilizzando una configurazione per applicazione, in modo che l'applicazione venga eseguita in modalità provvisoria. Per ulteriori informazioni sul database per la compatibilità delle applicazioni e sulla modalità provvisoria, vedere Windows Application Compatibility Toolkit. È possibile ottenere Windows Application Compatibility Toolkit da [https://www.microsoft.com/downloads](https://www.microsoft.com/Downloads/) .

> [!Note]  
> Se si inviano componenti con un [file di configurazione dell'applicazione](application-configuration-files.md) (file con estensione config) che specifica *Apply = "No"* in **publisherPolicy apply**, la generazione del contesto di attivazione avrà esito negativo. La configurazione per applicazione verrà ignorata se si inviano componenti con un file con estensione config specificando *Apply = "Yes"* in **publisherPolicy apply**.

 

Gli amministratori di applicazioni possono implementare una configurazione per ogni applicazione mediante la creazione e l'installazione dei file di configurazione dell'applicazione e l'aggiornamento del database di compatibilità delle applicazioni. Il file di configurazione dell'applicazione deve quindi essere distribuito e installato nella stessa cartella del file eseguibile dell'applicazione. Per un elenco dello schema dei file, vedere [schema del file di configurazione dell'applicazione](application-configuration-file-schema.md). Il database di compatibilità delle applicazioni deve essere distribuito come descritto in Application Compatibility Toolkit.

> [!Note]  
> Se l'applicazione viene eseguita in modalità provvisoria, non riceverà eventuali correzioni di bug o correzioni di sicurezza importanti che possono essere rilasciati dall'editore dell'assembly come file di configurazione del server di pubblicazione. Un'applicazione che usa la configurazione per applicazione può pertanto rimanere non sicura o continuare a funzionare in modo non corretto anche dopo che un nuovo assembly con queste correzioni viene applicato al sistema. Per questo motivo, gli sviluppatori di applicazioni non devono mai spedire un'applicazione con una configurazione per ogni applicazione. La configurazione per applicazione deve essere usata solo dagli amministratori aziendali come correzione temporanea quando l'applicazione è interruppe da una configurazione del server di pubblicazione. In questo caso, la soluzione permanente consiste nel fare in modo che gli sviluppatori dell'assembly e gli sviluppatori dell'applicazione debbano collaborare per assicurarsi che gli assembly con la configurazione del server di pubblicazione siano completamente compatibili con le versioni precedenti.

 

Di seguito è riportato un esempio di un file di configurazione dell'applicazione. Per ulteriori informazioni, vedere file di configurazione dell'applicazione.

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<configuration>
 <windows>
  <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">
   <assemblyIdentity  processorArchitecture="X86" name="Microsoft.Windows.mysampleApp" type="win32" version="1.0.0.0"/>
   <publisherPolicy apply="no"/>                     
   <dependentAssembly>
    <assemblyIdentity type="win32" processorArchitecture="x86" name="Microsoft.Windows.SampleAssembly" publicKeyToken="0000000000000000"/>
    <bindingRedirect oldVersion="2.0.0.0" newVersion="2.0.1.0"/>
   </dependentAssembly>
  </assemblyBinding>
 </windows>
</configuration>
```

L'amministratore dell'applicazione deve aggiungere le voci richieste al database di compatibilità delle applicazioni. Scaricare e installare Windows Application Compatibility Toolkit 2,6 da [https://www.microsoft.com/downloads](https://www.microsoft.com/Downloads/) . Creare un nuovo database personalizzato o aggiornare il database esistente usando l'amministratore della compatibilità come descritto nel Toolkit. La correzione della compatibilità che si vuole scegliere per il livello di compatibilità per l'applicazione è EnableAppConfig. Prima di installare un nuovo database di compatibilità, è sempre necessario testare le applicazioni.

 

 



