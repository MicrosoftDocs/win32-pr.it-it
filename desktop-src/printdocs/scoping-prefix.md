---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 4bad85d7-a933-43fe-9d79-4835d92c82d6
title: Prefisso ambito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef74be192671124872e19e87973a266da4a09226
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "103886040"
---
# <a name="scoping-prefix"></a>Prefisso ambito

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un prefisso dell'ambito è un'etichetta testuale pre-aggiunta a una parola chiave dello schema per fornire un ambito contestuale. Ciò consente di attribuire un contesto specifico e ben riconosciuto alle parole chiave in modo predefinito. La funzionalità Print Schema, ParameterDef, ParameterInit e ParameterRef e gli elementi di parole chiave di proprietà a livello radice devono includere uno dei seguenti prefissi di ambito: "Job", "Document" o "Page".

## <a name="interpretation-of-the-scoping-prefix-with-printticket-content"></a>Interpretazione del prefisso di ambito con contenuto PrintTicket

L'oggetto PrintTicket può essere suddiviso in tre livelli di contenuto che rappresentano il processo di alto livello, i documenti del processo e le pagine di ogni documento. Questi livelli sono classificati in base alla specificità; il livello di processo è più generale, quindi il livello del documento e quindi il livello di pagina è più specifico. Un processo è costituito da uno o più documenti e un documento è costituito da una o più pagine.

## <a name="job-level-prefix"></a>Prefisso livello processo

Un ticket a livello di processo contiene tutte le impostazioni di formattazione del processo destinate a essere applicate a un intero processo. Tutti gli elementi con prefissi di ambito "Job", "Document" o "Page" sono consentiti in un ticket a livello di processo.

Le impostazioni con prefisso "Document" e "Page" specificate in un ticket a livello di processo verranno applicate automaticamente ai ticket del documento e a livello di pagina.

## <a name="document-level-prefix"></a>Prefisso a livello di documento

Il ticket a livello di documento incorpora le impostazioni di formattazione dei processi da applicare a uno o più documenti in un processo. Possono includere le impostazioni specificate in precedenza nel ticket a livello di processo. In un ticket a livello di documento sono consentiti solo elementi con prefissi di ambito "Document" o "Page".

Un ticket a livello di documento può contenere impostazioni con prefisso di documento specificate in precedenza dal ticket a livello di processo.

## <a name="page-level-prefix"></a>Prefisso a livello di pagina

Il ticket a livello di pagina incorpora le impostazioni di formattazione dei processi da applicare a una o più pagine di un processo, non limitato a un singolo documento. Possono includere le impostazioni specificate in precedenza nel ticket a livello di processo o di documento. In un ticket a livello di pagina sono consentiti solo elementi con prefisso di ambito "Page".

Un ticket a livello di pagina può contenere le impostazioni con prefisso "pagina" specificate in precedenza dal ticket a livello di processo e/o dal ticket a livello di documento.

## <a name="prefix-usage-within-a-printticket-or-print-capabilities-document"></a>Utilizzo di prefisso in un documento di funzionalità di stampa o PrintTicket

I documenti PrintTicket e PrintCapabilities non devono contenere più parole chiave che differiscono solo per il prefisso di ambito. Per un documento PrintCapabilities, ad esempio, non devono essere specificati sia JobInputBin che PageInputBin. Tuttavia, in un documento sulle funzionalità di stampa possono essere specificati sia JobDuplexAllDocumentsContiguously che DocumentDuplex, perché sono considerati funzionalità diverse, perché presentano un comportamento diverso. Questo esempio è valido anche per un singolo PrintTicket.

## <a name="prefix-conflict-management"></a>Gestione dei conflitti di prefisso

Un conflitto di parole chiave tra le impostazioni viene definito come, lo stesso elemento dello schema di stampa a livello radice indicato dall'attributo XML "Name", che viene visualizzato in ticket a più livelli. Se non si verifica alcun conflitto, è possibile che un elemento con ambito prefisso venga premuto o ereditato da un ticket più generale a un ticket più specifico. Se si verifica un conflitto, l'impostazione del ticket più specifico avrà la precedenza. Ovvero le impostazioni per pagina in un ticket a livello di pagina sostituiscono le impostazioni per pagina identiche in un documento o un ticket a livello di processo. Analogamente, le impostazioni del documento nel ticket a livello di documento hanno la precedenza sulle impostazioni dei documenti nel ticket a livello di processo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



