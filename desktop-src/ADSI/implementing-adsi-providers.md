---
title: Implementazione di provider di interfacce del servizio Active Directory
description: Le interfacce ADSI (Active Directory Service Interfaces) sono interfacce COM che eseguono il wrapping di oggetti del servizio directory per esporli ai client dei servizi directory. Fornendo un'implementazione di ADSI, espandere la base client al set di applicazioni client ADSI.
ms.assetid: f86f36f0-44ff-41b7-8cf6-b97b721a8572
ms.tgt_platform: multiple
keywords:
- Implementazione di Active Directory provider di interfacce di servizio ADSI
- Implementazione di ADSI Providers ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30bdd0da406d9e65af898664e76b5e455540ebeb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707414"
---
# <a name="implementing-active-directory-service-interfaces-providers"></a>Implementazione di provider di interfacce del servizio Active Directory

Le interfacce ADSI (Active Directory Service Interfaces) sono interfacce COM che eseguono il wrapping di oggetti del servizio directory per esporli ai client dei servizi directory. Fornendo un'implementazione di ADSI, espandere la base client al set di applicazioni client ADSI.

Come per qualsiasi implementazione COM, è possibile scrivere un provider ADSI in molte lingue. Le interfacce COM ADSI sono definite come interfacce duali che consentono la risoluzione dei nomi in fase di esecuzione e in fase di compilazione e possono essere chiamate da linguaggi conformi all'automazione, ad esempio Visual Basic, Visual Basic Scripting Edition, nonché i linguaggi più efficienti in termini di prestazioni e efficienza, ad esempio C e C++. I client ADSI includono inoltre le applicazioni Web che utilizzano Active Server pagine e gli snap-in di amministrazione tramite Microsoft Management Console.

Poiché ADSI fornisce il proprio provider OLE DB, l'implementazione delle funzionalità di ricerca definite da [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) consente inoltre ai client ADSI di eseguire query sul servizio directory per i dati.

Tutti gli oggetti del servizio di directory possono essere rappresentati tramite un oggetto ADSI generico che supporta [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject). ADSI fornisce i blocchi predefiniti necessari per rappresentare le funzionalità e i servizi di qualsiasi servizio di directory.

Inoltre, le metainterfacce ADSI rappresentano gli oggetti comuni utilizzati dagli amministratori di directory. È possibile eseguire il mapping delle proprietà delle metainterfacce alle proprietà supportate dal servizio directory. I client ADSI che programmano le interfacce del servizio Active Directory ottengono l'accesso al servizio directory non appena il provider viene installato e il sistema viene riavviato.

Se il servizio Directory supporta una rappresentazione dello schema, il supporto delle interfacce di gestione dello schema rende lo spazio dei nomi accessibile direttamente ai browser del servizio directory. Grazie alla pubblicazione delle funzionalità tramite lo schema, i client possono eseguire query sul servizio directory online e usufruire dei servizi offerti. Grazie alla disponibilità dello schema online e al vantaggio dell'interfaccia COM, è possibile continuare a rendere disponibili nuove funzionalità per il software client, supportando al tempo stesso le versioni di livello inferiore.

 

 




