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

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Il [riepilogo dei tipi di elemento](summary-of-element-types.md) illustra i vari elementi che costituiscono un documento PrintCapabilities. Questa sezione fornisce un elenco di controllo che gli autori di documenti PrintCapabilities possono usare per creare un documento PrintCapabilities che descrive un dispositivo.

1.  Identificare tutti gli attributi del dispositivo che contribuiscono alla configurazione del dispositivo. Per ogni attributo di dispositivo di questo tipo, determinare se deve essere rappresentato come costrutto Feature/Option o come costrutto di parametro.

2.  Per ogni funzionalità del dispositivo, determinare se può essere rappresentata da una funzionalità definita nelle parole chiave dello schema di stampa. In caso contrario, sarà necessario introdurre una nuova funzionalità definita privatamente (e un attributo del nome corrispondente).

    -   Per le istanze di funzionalità definite da parole chiave dello schema di stampa, identificare ognuno degli stati disponibili su cui questa funzionalità può essere impostata. Ogni stato corrisponde a un'opzione dell'istanza della funzionalità. Determinare quali di questi stati corrispondono alle istanze dell'opzione print schema-defined associate a questa funzionalità e quali stati richiedono un'istanza option personalizzata. [L'argomento Definizioni](option-definitions.md) di opzioni presenta informazioni su come costruire nuove istanze di Option e su come derivare nuove istanze option da istanze option esistenti.

    -   Per le istanze di funzionalità non standard, identificare le caratteristiche che possono essere usate per distinguere un'opzione da un'altra. Rappresentare ogni caratteristica di questo tipo in base a un elemento ScoredProperty e, in ogni istanza di Option, assegnare a ogni ScoredProperty un valore specifico per tale opzione. Assicurarsi che siano disponibili elementi ScoredProperty sufficienti in modo che ogni opzione per una determinata funzionalità sia univoca. Le istanze di funzionalità e opzioni non standard sono per loro natura non portabili. Ciò significa che un altro driver non sarà in grado di trovare funzionalità o opzioni equivalenti per trovare una corrispondenza con una funzionalità o un'opzione non standard specificata nel PrintTicket creato dal driver.

3.  Determinare se un elemento Option deve contenere elementi ParameterRef. Per altre informazioni, vedere [Costrutti di parametro ed](parameter-constructs.md) [elementi di riferimento ai parametri.](parameter-reference-elements.md)

4.  Per i parametri, determinare se una delle istanze ParameterDef definite nelle parole chiave dello schema di stampa è una corrispondenza adeguata. In tal caso, copiare l'istanza ParameterDef dalle parole chiave dello schema di stampa e modificare il valore di ogni istanza di proprietà modificabile in modo che sia più adatta. Se nessuna delle istanze di ParameterDef nelle parole chiave dello schema di stampa è una corrispondenza adeguata, creare la propria istanza di ParameterDef. Per altre informazioni, vedere [Parametri nel documento PrintCapabilities.](parameters-in-the-printcapabilities-document.md)

5.  Assicurarsi che tutte le istanze Property e ScoredProperty richieste dal documento Print Schema Keywords siano presenti nel documento PrintCapabilities e che siano inizializzate correttamente.

6.  Aggiungere altre istanze di proprietà e sottoproprietà in base alle esigenze. È possibile introdurre istanze di proprietà definite privatamente se esistono aspetti del dispositivo che è necessario caratterizzare che non sono coperti dalle istanze di proprietà definite nelle parole chiave dello schema di stampa.

7.  Osservare la convenzione dello spazio dei nomi per gli attributi del nome. Questo vale per gli attributi dei nomi definiti privatamente e per quelli definiti nelle parole chiave dello schema di stampa.

8.  Gli elementi figlio dello stesso tipo di elemento non possono essere annidati fino a una profondità superiore a 10 elementi. Questa regola si applica in modo indipendente a ogni tipo di elemento che può essere definito.

Si noti che le funzionalità di stampa documentare il contenuto XML DEVE essere codificato usando UTF-8 o UTF-16.

Si noti che il set di istanze Feature, Option e ParameterDef segnalate non deve cambiare, indipendentemente dello snapshot. Anche le istanze scoredProperty che costituiscono ogni istanza option e il valore assegnato a ogni elemento ScoredProperty non devono essere modificate. Lo stesso vale per le istanze Property che costituiscono ogni istanza ParameterDef.

Per un elenco di istanze di proprietà aggiuntive che devono essere fornite per definire completamente i costrutti e i parametri feature/option, vedere [ParameterDef](parameterdef.md) e [ParameterInit.](parameterinit.md) Ad esempio, ogni funzionalità deve specificare il proprio comportamento dell'interfaccia utente, in particolare se è possibile selezionare esattamente una o più istanze option per ogni funzionalità contemporaneamente. Il documento Parole chiave dello schema di stampa definisce queste istanze property, in cui devono essere visualizzate all'interno del documento PrintCapabilities e quali istanze value definite nelle parole chiave dello schema di stampa sono disponibili.

Il provider PrintCapabilities è responsabile dell'emissione del valore appropriato per tutte le istanze di proprietà dipendenti dalla configurazione. Ad esempio, se la frequenza di stampa dipende sia dalla modalità colore che dalla risoluzione usata, il provider PrintCapabilities deve prendere nota delle impostazioni di risoluzione e della modalità colore specificate nel PrintTicket fornito dal client e deve segnalare il valore appropriato per la frequenza di stampa. Si noti che ogni istanza scoredProperty deve essere a valore singolo. L'istanza Value non può cambiare quando viene modificata la configurazione del dispositivo.

Si noti anche che le istanze di proprietà definite nelle parole chiave dello schema di stampa devono essere visualizzate nel percorso specificato. Non possono essere visualizzati in posizioni arbitrarie all'interno di un documento PrintCapabilities. Le istanze di proprietà definite privatamente possono essere visualizzate ovunque, anche come sottoproprietà all'interno di istanze di proprietà definite da schema.

Si noti che un conflitto funzionale tra le impostazioni è definito come due elementi dello schema di stampa non in conflitto che hanno una funzione simile ma sono funzionalità diverse. Ad esempio, JobDuplexAllDocumentsContiguously e DocumentDuplex; entrambi rappresentano la funzione duplex del dispositivo, ma differiscono nell'applicazione della funzione, uno si applica all'intero processo in modo contiguo e uno ai documenti. Nel caso in cui siano specificati due elementi di questo tipo, la precedenza è determinata dal producer PrintCapabilities e dal consumer PrintTicket. È responsabilità del producer PrintCapabilities indicare correttamente i vincoli tra gli elementi in conflitto tramite l'attributo "constrained". Gli elementi nello schema di stampa pubblico che presentano questo conflitto semantico vengono identificati nella relativa definizione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



