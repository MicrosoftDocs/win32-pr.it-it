---
description: Un prefisso di ambito è un'etichetta testuale pre-aggiunta a una parola chiave dello schema per fornire un ambito contestuale, tra cui Job, Document e Page.
ms.assetid: 4bad85d7-a933-43fe-9d79-4835d92c82d6
title: Prefisso di ambito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2c027de94fda403eb58905e536d8c6256cb2d6c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404904"
---
# <a name="scoping-prefix"></a>Prefisso di ambito

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un prefisso di ambito è un'etichetta testuale pre-aggiunta a una parola chiave dello schema per fornire un ambito contestuale. In questo modo è possibile definire un contesto specifico e ben compreso per le parole chiave in modo predefinito. Funzionalità dello schema di stampa, ParameterDef, ParameterInit e ParameterRef e parola chiave Property a livello di radice Gli elementi DEVONO avere uno dei prefissi di ambito seguenti: "Job", "Document" o "Page".

## <a name="interpretation-of-the-scoping-prefix-with-printticket-content"></a>Interpretazione del prefisso di ambito con contenuto PrintTicket

PrintTicket può essere suddiviso in tre livelli di contenuto che rappresentano il processo di alto livello, i documenti nel processo e le pagine in ogni documento. Questi livelli vengono classificati in base alla specificità. il livello di processo è più generale, quindi il livello documento e quindi il livello di pagina è più specifico. Un processo è costituito da uno o più documenti e un documento è costituito da una o più pagine.

## <a name="job-level-prefix"></a>Prefisso a livello di processo

Un ticket a livello di processo contiene tutte le impostazioni di formattazione del processo da applicare a un intero processo. Tutti gli elementi con prefissi di ambito "Job", "Document" o "Page" sono consentiti in un ticket a livello di processo.

Le impostazioni con prefisso "Documento" e "Pagina" specificate in un ticket a livello di processo verranno applicate automaticamente ai ticket a livello di documento e di pagina.

## <a name="document-level-prefix"></a>Prefisso a livello di documento

Il ticket a livello di documento incorpora tutte le impostazioni di formattazione del processo da applicare a uno o più documenti in un processo. Possono includere le impostazioni specificate in precedenza nel ticket a livello di processo. Solo gli elementi con prefissi di ambito "Document" o "Page" sono consentiti in un ticket a livello di documento.

Un ticket a livello di documento può contenere impostazioni con prefisso Document specificate in precedenza dal ticket a livello di processo.

## <a name="page-level-prefix"></a>Prefisso a livello di pagina

Il ticket a livello di pagina incorpora tutte le impostazioni di formattazione del processo da applicare a una o più pagine di un processo (non solo a un singolo documento). Possono includere le impostazioni specificate in precedenza nel ticket a livello di processo o di documento. In un ticket a livello di pagina sono consentiti solo elementi con prefissi di ambito "Page".

Un ticket a livello di pagina può contenere impostazioni con prefisso "Pagina" specificate in precedenza dal ticket a livello di processo e/o dal ticket a livello di documento.

## <a name="prefix-usage-within-a-printticket-or-print-capabilities-document"></a>Utilizzo del prefisso all'interno di un documento sulle funzionalità di stampa o PrintTicket

I documenti PrintTicket e PrintCapabilities NON DEVONO contenere più parole chiave che differiscono solo per il prefisso di ambito. Ad esempio, un documento PrintCapabilities NON DEVE avere sia JobInputBin che PageInputBin specificati. Tuttavia, un documento di funzionalità di stampa può avere sia JobDuplexAllDocumentsContiguously che DocumentDuplex specificati perché sono considerate funzionalità diverse, in quanto presentano un comportamento diverso. Questo esempio è vero anche per un singolo PrintTicket.

## <a name="prefix-conflict-management"></a>Gestione dei conflitti dei prefissi

Un conflitto di parole chiave tra le impostazioni è definito come, lo stesso elemento dello schema di stampa a livello radice denotato dall'attributo XML "name", visualizzato in più ticket di livello. Se non si verifica alcun conflitto, è possibile eseguire il push verso il basso o ereditare un elemento con ambito prefisso da un ticket più generale a un ticket più specifico. In caso di conflitto, l'impostazione del ticket più specifico ha la precedenza. Ciò significa che le impostazioni per pagina in un ticket a livello di pagina sostituiscono le impostazioni identiche per pagina in un ticket a livello di documento o di processo. Analogamente, le impostazioni del documento nel ticket a livello di documento hanno la precedenza sulle impostazioni del documento nel ticket a livello di processo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



