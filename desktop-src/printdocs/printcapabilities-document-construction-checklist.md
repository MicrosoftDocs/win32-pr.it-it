---
description: Questo articolo fornisce un elenco di controllo che gli autori di documenti PrintCapabilities possono usare per creare un documento PrintCapabilities che descrive un dispositivo.
ms.assetid: 4b8fa1a4-6461-4722-861b-354f206b2a73
title: Elenco di controllo per la costruzione di documenti PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a5284a480f73151750926d975535ea799457a1ce2cd4c14f197a4fc6519b646
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117867963"
---
# <a name="printcapabilities-document-construction-checklist"></a>Elenco di controllo per la costruzione di documenti PrintCapabilities

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Il [riepilogo dei tipi di elemento](summary-of-element-types.md) illustra i vari elementi che costituiscono un documento PrintCapabilities. In questa sezione viene fornito un elenco di controllo che gli autori di documenti PrintCapabilities possono usare per creare un documento PrintCapabilities che descrive un dispositivo.

1.  Identificare tutti gli attributi del dispositivo che contribuiscono alla configurazione del dispositivo. Per ogni attributo del dispositivo di questo tipo, determinare se deve essere rappresentato come costrutto feature/opzione o come costrutto di parametro.

2.  Per ogni funzionalità del dispositivo, determinare se può essere rappresentata da una funzionalità definita nelle parole chiave dello schema di stampa. In caso contrario, sarà necessario introdurre una nuova funzionalità definita privatamente (e un attributo del nome corrispondente).

    -   Per le istanze di funzionalità definite da parole chiave dello schema di stampa, identificare ognuno degli stati disponibili su cui è possibile impostare questa funzionalità. Ogni stato corrisponde a un'opzione dell'istanza della funzionalità. Determinare quali di questi stati corrispondono alle istanze dell'opzione print schema-defined associate a questa funzionalità e quali stati richiedono un'istanza option personalizzata. [L'argomento Definizioni](option-definitions.md) delle opzioni contiene informazioni su come costruire nuove istanze di Opzione e su come derivare nuove istanze di Opzione da istanze option esistenti.

    -   Per le istanze di funzionalità non standard, identificare le caratteristiche che possono essere usate per distinguere un'opzione da un'altra. Rappresentare ogni caratteristica di questo tipo da un elemento ScoredProperty e in ogni istanza di Opzione assegnare a ogni ScoredProperty un valore specifico di tale opzione. Assicurarsi che siano presenti elementi ScoredProperty sufficienti in modo che ogni opzione per una determinata funzionalità sia univoca. Le istanze Feature e Option non standard sono per loro natura non portabili. In altre informazioni, un altro driver non sarà in grado di trovare funzionalità o opzioni equivalenti in modo che corrispondano a una funzionalità o a un'opzione non standard specificata in PrintTicket creato dal driver.

3.  Determinare se un'opzione deve contenere elementi ParameterRef. Per altre informazioni, vedere [Costrutti di parametro ed](parameter-constructs.md) [Elementi di riferimento ai parametri](parameter-reference-elements.md).

4.  Per i parametri, determinare se una delle istanze ParameterDef definite nelle parole chiave dello schema di stampa è una corrispondenza adeguata. In tal caso, copiare l'istanza ParameterDef dalle parole chiave dello schema di stampa e modificare il valore di ogni istanza di Property modificabile per la scelta ottimale. Se nessuna delle istanze ParameterDef nelle parole chiave dello schema di stampa è una corrispondenza adeguata, creare un'istanza ParameterDef. Per altre informazioni, vedere [Parametri nel documento PrintCapabilities](parameters-in-the-printcapabilities-document.md).

5.  Assicurarsi che tutte le istanze Property e ScoredProperty richieste dal documento Print Schema Keywords siano presenti nel documento PrintCapabilities e che siano inizializzate correttamente.

6.  Aggiungere altre istanze di proprietà e sottoproprietà in base alle esigenze. È possibile introdurre istanze property definite privatamente se sono presenti aspetti del dispositivo che è necessario caratterizzare che non sono coperti dalle istanze property definite nelle parole chiave dello schema di stampa.

7.  Osservare la convenzione dello spazio dei nomi per gli attributi del nome. Questo vale per gli attributi del nome definiti privatamente e per quelli definiti nelle parole chiave dello schema di stampa.

8.  Gli elementi figlio dello stesso tipo di elemento non possono annidare fino a una profondità superiore a 10 elementi. Questa regola si applica in modo indipendente a ogni tipo di elemento che può essere definito.

Si noti che le funzionalità di stampa documentano che il contenuto XML DEVE essere codificato usando UTF-8 o UTF-16.

Si noti che il set di istanze Feature, Option e ParameterDef segnalate non deve cambiare, indipendentemente dalla snapshot. Anche le istanze scoredProperty che costituiscono ogni istanza di Option e il valore assegnato a ogni elemento ScoredProperty non devono cambiare. Lo stesso vale per le istanze Property che costituiscono ogni istanza di ParameterDef.

Per un elenco di istanze Property aggiuntive che devono essere fornite per definire completamente i costrutti e i parametri feature/option, vedere [ParameterDef](parameterdef.md) e [ParameterInit](parameterinit.md). Ad esempio, ogni funzionalità deve specificare il comportamento dell'interfaccia utente, in particolare se è possibile selezionare esattamente una o più istanze option per ogni funzionalità contemporaneamente. Il documento Parole chiave dello schema di stampa definisce queste istanze property, in cui devono essere visualizzate all'interno del documento PrintCapabilities e quali istanze Value definite nelle parole chiave dello schema di stampa sono disponibili.

Il provider PrintCapabilities è responsabile dell'emissione del valore appropriato per tutte le istanze property dipendenti dalla configurazione. Ad esempio, se la frequenza di stampa dipende sia dalla modalità colore che dalla risoluzione usata, il provider PrintCapabilities deve prendere nota della modalità colore e delle impostazioni di risoluzione specificate nell'oggetto PrintTicket fornito dal client e deve segnalare il valore appropriato per la frequenza di stampa. Si noti che ogni istanza scoredProperty deve essere a valore singolo. l'istanza Value non può cambiare quando cambia la configurazione del dispositivo.

Si noti anche che le istanze property definite nelle parole chiave dello schema di stampa devono essere visualizzate nella posizione specificata. Non possono essere visualizzati in posizioni arbitrarie all'interno di un documento PrintCapabilities. Le istanze Property definite privatamente possono essere visualizzate ovunque, anche come sottoproprietà all'interno di istanze property definite da schema.

Si noti che un conflitto funzionale tra le impostazioni viene definito come due elementi dello schema di stampa non in conflitto che hanno una funzione simile ma sono funzionalità diverse. Un esempio è JobDuplexAllDocumentsContiguously e DocumentDuplex. entrambi rappresentano la funzione duplex del dispositivo, ma differiscono nell'applicazione della funzione, una che si applica all'intero processo in modo contiguo e una ai documenti. Nel caso in cui siano specificati due elementi di questo tipo, la precedenza è determinata dal producer PrintCapabilities e dal consumer PrintTicket. È responsabilità del producer PrintCapabilities indicare correttamente i vincoli tra elementi in conflitto tramite l'attributo "constrained". Gli elementi nello schema di stampa pubblico che presentano questo conflitto semantico vengono identificati nella relativa definizione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



