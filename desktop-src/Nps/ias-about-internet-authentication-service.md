---
title: Informazioni sulle estensioni NPS
description: In questa sezione viene descritto come implementare le dll per estendere le funzionalità di NPS. Descrive l'interazione tra NPS e le dll e presenta alcune considerazioni di progettazione relative alle DLL.
ms.assetid: 3d4d8d22-4cd3-48e0-b4a4-dfa0a0b7b87f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05878a5243774046c1ca052052d59be9378483d6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300156"
---
# <a name="about-nps-extensions"></a>Informazioni sulle estensioni NPS

> [!Note]  
> Il servizio di autenticazione Internet (IAS) è stato rinominato server dei criteri di rete (NPS) a partire da Windows Server 2008. Il contenuto di questo argomento si applica sia a IAS che a NPS. In tutto il testo, NPS viene utilizzato per fare riferimento a tutte le versioni del servizio, incluse le versioni originariamente indicate come IAS.

 

In questa sezione viene descritto come implementare le dll per estendere le funzionalità di NPS. Descrive l'interazione tra NPS e le dll e presenta alcune considerazioni di progettazione relative alle DLL.

NPS fornisce due punti di estensione, uno per l'autenticazione e l'altro per l'autorizzazione. Per autenticazione si intende la verifica dell'identità dell'utente. L'autorizzazione si riferisce alla determinazione dei servizi che la rete deve fornire all'utente. I due punti di estensione corrispondono alle DLL dell'estensione di autenticazione e alle DLL dell'estensione di autorizzazione. Ogni punto di estensione può supportare più dll.

NPS fornisce servizi di autenticazione e autorizzazione. Le DLL dell'estensione di autenticazione vengono chiamate da NPS prima dell'autenticazione e dell'autorizzazione del server dei criteri di server. Le DLL dell'estensione di autorizzazione vengono chiamate dopo l'autenticazione e l'autorizzazione NPS.

Il diagramma seguente illustra il flusso di pacchetti tramite un server RADIUS NPS espanso mediante dll di estensione.

![processo di autenticazione e autorizzazione server dei criteri di server](images/ias03.png)

Se una DLL di estensione di autenticazione restituisce ACCEPT, il pacchetto ignora l'autenticazione NPS e passa direttamente all'autorizzazione NPS.

> [!Note]  
> Quando sono presenti più DLL dell'estensione di autenticazione, è possibile che vengano ignorate anche le altre DLL di estensione. Per ulteriori informazioni, vedere [configurazione delle DLL di estensione](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls) .

 

Se una DLL di estensione di autenticazione restituisce CONTINUE, il pacchetto passa all'autenticazione NPS e quindi all'autorizzazione NPS.

> [!Note]  
> Quando sono presenti più DLL di estensione di autenticazione, le altre DLL dell'estensione di autenticazione vengono richiamate prima dell'autenticazione NPS.

 

Gli argomenti seguenti descrivono le DLL di estensione in modo più dettagliato:

-   [Impostazione delle DLL di estensione](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls)
-   [Richiamo delle DLL di estensione](/windows/desktop/Nps/ias-authentication-and-authorization-process)
-   [Attributi di identificazione utente](/windows/desktop/Nps/ias-user-identification-attributes)

 

 