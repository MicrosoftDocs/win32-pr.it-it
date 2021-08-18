---
title: Supporto del linguaggio di programmazione
description: È possibile scrivere applicazioni client ADSI in molti linguaggi.
ms.assetid: 47460d57-936d-4c5f-8ff6-a4d9d60d0b68
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ebe355e3274821bf81a666380bfe70ca0f3f7b49e2bc9de10bf2aa4796b5288
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023304"
---
# <a name="programming-language-support"></a>Supporto del linguaggio di programmazione

È possibile scrivere applicazioni client ADSI in molti linguaggi. Per la maggior parte delle attività amministrative, ADSI definisce interfacce e oggetti accessibili da linguaggi conformi ad Automazione. Ad esempio, il sistema di sviluppo Microsoft Visual Basic, Microsoft Visual Basic Scripting Edition (VBScript) e Java, nonché linguaggi più efficienti ed efficienti come C e C++.

Una perfetta integrazione con Active Server e VBScript semplifica la scrittura di applicazioni Internet che accedono ai servizi directory. Per l'integrazione OLE DB applicazioni, ADSI fornisce un provider di OLE DB supportando un subset delle interfacce OLE DB query. Il provider OLE DB supporta l'accesso in sola lettura ad Active Directory.

Per le applicazioni Internet, l'uso di script in file ASP (Active Server Page) può creare e modificare oggetti ADSI nel server e visualizzare i risultati in una pagina Web. In Microsoft Management Console, gli snap-in di amministrazione del servizio directory possono usare ADSI per trovare i servizi directory di interesse. In breve, le interfacce del servizio Active Directory possono fornire l'accesso a un ampio e diversificato set di servizi directory, inclusi quelli non ancora compilati.

Per l'accesso alle strutture che usano API tradizionali, l'architettura ADSI definisce interfacce di basso livello che non supportano Automazione accessibili da linguaggi come C e C++. Queste interfacce sono poco più dei wrapper COM per i protocolli di rete per un servizio directory.

La scrittura di codice nelle interfacce pubblicate consente all'applicazione di raggiungere i servizi directory per tutti i provider ADSI installati e integrare i dati risultanti. Con poche o nessuna modifica al codice, l'applicazione può continuare ad accedere ad altri servizi directory nella rete quando vengono installati nuovi provider ADSI.

Nella figura seguente viene illustrato il modo in cui ADSI si inserisce in un ambiente applicativo. Indipendentemente dal fatto che l'applicazione sia scritta in Visual Basic, C/C++, VBScript, sistema di sviluppo Microsoft JScript o come applicazione Web tramite Active Server Pages, le interfacce del servizio Active Directory offrono un accesso pulito e facile da usare ai servizi directory sottostanti senza dover usare le API di rete native.

![Supporto di adsi per i linguaggi di programmazione](images/ds2layr.png)

Come illustrato nella figura precedente, i client che non supportano Automazione hanno accesso a tutte le interfacce ADSI, incluse entrambe le interfacce COM pure con la convenzione di denominazione **IDirectoryXXX** e le interfacce COM di automazione con la convenzione di denominazione **IADsXXX**. Poiché i client richiedono principalmente informazioni dai servizi directory, il modello di query flessibile ADSI tramite OLE DB [**e IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) è efficace.

 

 




