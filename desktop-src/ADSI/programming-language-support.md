---
title: Supporto del linguaggio di programmazione
description: È possibile scrivere applicazioni client ADSI in molte lingue.
ms.assetid: 47460d57-936d-4c5f-8ff6-a4d9d60d0b68
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4946f05806a6e24ff466d08dc141aadf9c995e5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855265"
---
# <a name="programming-language-support"></a>Supporto del linguaggio di programmazione

È possibile scrivere applicazioni client ADSI in molte lingue. Per la maggior parte delle attività amministrative, ADSI definisce le interfacce e gli oggetti accessibili da linguaggi conformi all'automazione. Ad esempio, il sistema di sviluppo Microsoft Visual Basic, Microsoft Visual Basic Scripting Edition (VBScript) e Java, nonché più prestazioni ed efficienza, ad esempio C e C++.

Una semplice integrazione con le pagine Active Server e VBScript semplifica la scrittura di applicazioni Internet che accedono ai servizi directory. Per l'integrazione con OLE DB applicazioni, ADSI fornisce un provider OLE DB supportando un subset di OLE DB interfacce di query. Il provider OLE DB supporta l'accesso in sola lettura ai Active Directory.

Per le applicazioni Internet, l'utilizzo di script in file di Active Server pagina (ASP) può creare e modificare oggetti ADSI nel server e visualizzare i risultati in una pagina Web. In Microsoft Management Console gli snap-in di amministrazione dei servizi directory possono utilizzare ADSI per trovare i servizi directory di interesse. In breve, le interfacce del servizio Active Directory possono fornire l'accesso a un set di servizi directory ampio e diversificato, inclusi quelli non ancora compilati.

Per l'accesso alle strutture che usano le API tradizionali, l'architettura ADSI definisce le interfacce di basso livello che non supportano l'automazione accessibili da linguaggi come C e C++. Queste interfacce sono poco più dei wrapper COM per i protocolli di rete per un servizio directory.

La scrittura di codice nelle interfacce pubblicate consente all'applicazione di raggiungere i servizi directory per tutti i provider ADSI installati e di integrare i dati risultanti. Con le modifiche minime o minime apportate al codice, l'applicazione può continuare ad accedere ai servizi directory aggiuntivi nella rete quando vengono installati nuovi provider ADSI.

Nella figura seguente viene illustrato il modo in cui ADSI si inserisce in un ambiente di applicazione. Indipendentemente dal fatto che l'applicazione sia scritta in Visual Basic, C/C++, VBScript, sistema di sviluppo Microsoft JScript o come applicazione Web con Active Server pagine, Active Directory interfacce del servizio forniscono un accesso pulito e facile da utilizzare ai servizi directory sottostanti senza dover utilizzare le API di rete native.

![supporto ADSI per i linguaggi di programmazione](images/ds2layr.png)

Come illustrato nella figura precedente, i client che non supportano l'automazione possono accedere a tutte le interfacce ADSI, incluse le interfacce COM pure con la convenzione di denominazione **IDirectoryXXX** e le interfacce com di automazione con la convenzione di denominazione **IADsXXX**. Poiché i client richiedono prevalentemente le informazioni dei servizi directory, il modello di query flessibile ADSI tramite OLE DB e [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) è efficace.

 

 




