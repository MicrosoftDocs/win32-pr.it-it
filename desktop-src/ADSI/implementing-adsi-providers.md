---
title: Implementazione di provider di interfacce del servizio Active Directory
description: Active Directory Service Interfaces (ADSI) è un'interfaccia COM che esegue il wrapping degli oggetti servizio directory per esporli ai client dei servizi directory. Fornendo un'implementazione di ADSI, si espande la base client al set di applicazioni client ADSI.
ms.assetid: f86f36f0-44ff-41b7-8cf6-b97b721a8572
ms.tgt_platform: multiple
keywords:
- Implementazione di ACTIVE Directory Service Interfaces Providers ADSI
- Implementazione dei provider ADSI ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd3eb1275398a82a2ef179678e56cb9a7eda2e63eb4278906fc925fcb1d7cf6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118427560"
---
# <a name="implementing-active-directory-service-interfaces-providers"></a>Implementazione di provider di interfacce del servizio Active Directory

Active Directory Service Interfaces (ADSI) è un'interfaccia COM che esegue il wrapping degli oggetti servizio directory per esporli ai client dei servizi directory. Fornendo un'implementazione di ADSI, si espande la base client al set di applicazioni client ADSI.

Come per qualsiasi implementazione COM, è possibile scrivere un provider ADSI in molti linguaggi. Le interfacce COM ADSI sono definite come interfacce duali che consentono la risoluzione dei nomi sia in fase di esecuzione che in fase di compilazione e possono essere chiamate da linguaggi conformi ad Automazione, ad esempio Visual Basic, Visual Basic Scripting Edition, nonché linguaggi più efficienti ed efficienti come C e C++. I client ADSI includono anche applicazioni Web che usano Active Server e snap-in di amministrazione tramite Microsoft Management Console.

Poiché ADSI fornisce il proprio provider OLE DB, l'implementazione delle funzionalità di ricerca definite da [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) consente anche ai client ADSI di eseguire query sul servizio directory per i dati.

Tutti gli oggetti del servizio directory possono essere rappresentati tramite un oggetto ADSI generico che supporta [**IDirectoryObject.**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) ADSI fornisce i blocchi predefiniti necessari per rappresentare le funzionalità e i servizi di qualsiasi servizio directory.

Inoltre, le meta-interfacce ADSI rappresentano oggetti comuni usati dagli amministratori di directory. Eseguire il mapping delle proprietà delle meta-interfacce alle proprietà supportate dal servizio directory. I client ADSI che programmano le interfacce del servizio Active Directory ottengono l'accesso al servizio directory non appena il provider viene installato e il sistema viene riavviato.

Se il servizio directory supporta una rappresentazione dello schema, il supporto delle interfacce di gestione dello schema rende lo spazio dei nomi direttamente accessibile ai browser del servizio directory. Pubblicando le funzionalità tramite lo schema, i client possono eseguire query online sul servizio directory e sfruttare i servizi offerti. A causa della disponibilità dello schema online e del vantaggio dell'interfaccia COM, è possibile continuare a rendere disponibili nuove funzionalità per il software client supportando al tempo stesso le versioni di livello inferiore.

 

 




