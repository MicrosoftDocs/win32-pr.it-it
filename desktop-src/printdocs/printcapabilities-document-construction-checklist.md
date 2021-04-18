---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 4b8fa1a4-6461-4722-861b-354f206b2a73
title: Elenco di controllo per la costruzione di documenti PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0f730a426bb787104e08f879ecccd357fd3102b
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320883"
---
# <a name="printcapabilities-document-construction-checklist"></a>Elenco di controllo per la costruzione di documenti PrintCapabilities

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Il [Riepilogo dei tipi di elemento](summary-of-element-types.md) illustra i vari elementi che costituiscono un documento PrintCapabilities. In questa sezione viene fornito un elenco di controllo che gli autori dei documenti PrintCapabilities possono utilizzare per creare un documento PrintCapabilities che descrive un dispositivo.

1.  Identificare tutti gli attributi del dispositivo che contribuiscono alla configurazione del dispositivo. Per ogni attributo del dispositivo di questo tipo, determinare se deve essere rappresentato come costrutto di funzionalità/opzione o come costrutto di parametro.

2.  Per ogni funzionalità del dispositivo, determinare se può essere rappresentata da una funzionalità definita nelle parole chiave Print Schema. In caso contrario, sarà necessario introdurre una nuova funzionalità definita privatamente e un attributo del nome corrispondente.

    -   Per le istanze di funzionalità definite dalle parole chiave dello schema di stampa, identificare ciascuno degli stati disponibili su cui è possibile impostare questa funzionalità. Ogni stato corrisponde a un'opzione dell'istanza della funzionalità. Determinare quali di questi stati corrispondono alle istanze di opzioni definite dallo schema di stampa associate a questa funzionalità e quali stati richiedono un'istanza di opzione personalizzata. Nell'argomento [definizioni di opzioni](option-definitions.md) vengono fornite informazioni su come costruire nuove istanze di opzioni e su come derivare nuove istanze di opzioni da istanze di opzioni esistenti.

    -   Per le istanze di funzionalità non standard, identificare le caratteristiche che possono essere utilizzate per distinguere un'opzione da un'altra. Rappresentare ciascuna caratteristica da un elemento ScoredProperty e in ogni istanza di Option assegnare a ogni ScoredProperty un valore specifico di tale opzione. Verificare che siano presenti sufficiente elementi ScoredProperty in modo che ogni opzione per una determinata funzionalità sia univoca. Le istanze della funzionalità e delle opzioni non standard sono per natura non portabile. Ovvero, un altro driver non sarà in grado di trovare funzionalità o opzioni equivalenti per la corrispondenza di una funzionalità o di un'opzione non standard specificata nel PrintTicket creato dal driver.

3.  Determinare se un'opzione deve contenere elementi ParameterRef. Per altre informazioni, vedere [costrutti di parametri](parameter-constructs.md) ed [elementi di riferimento ai parametri](parameter-reference-elements.md).

4.  Per i parametri, determinare se una delle istanze di ParameterDef definite nelle parole chiave di Print Schema è una corrispondenza adeguata. In tal caso, copiare l'istanza di ParameterDef dalle parole chiave dello schema di stampa e modificare il valore di ogni istanza di proprietà modificabile per la soluzione migliore. Se nessuna delle istanze di ParameterDef nelle parole chiave di Print Schema è una corrispondenza adeguata, creare un'istanza di ParameterDef personalizzata. Per ulteriori informazioni, vedere [parametri nel documento PrintCapabilities](parameters-in-the-printcapabilities-document.md).

5.  Verificare che tutte le istanze di proprietà e ScoredProperty richieste dal documento parole chiave di Stampa schema siano presenti nel documento PrintCapabilities e che siano inizializzate correttamente.

6.  Aggiungere altre istanze di proprietà e sottoproprietà nel modo desiderato. È possibile introdurre istanze di proprietà definite privatamente se sono presenti aspetti del dispositivo che è necessario caratterizzare che non sono coperti dalle istanze di proprietà definite nelle parole chiave dello schema di stampa.

7.  Osservare la convenzione dello spazio dei nomi per gli attributi del nome. Questo vale per gli attributi di nome definiti privatamente e per quelli definiti nelle parole chiave Print Schema.

8.  Gli elementi figlio dello stesso tipo di elemento potrebbero non annidarsi a una profondità superiore a 10 elementi. Questa regola si applica in modo indipendente a ogni tipo di elemento che è possibile definire.

Si noti che il contenuto XML del documento sulle funzionalità di stampa deve essere codificato con UTF-8 o UTF-16.

Si noti che il set di funzionalità, opzioni e istanze di ParameterDef segnalate non devono essere modificate, indipendentemente dallo snapshot. Anche le istanze di ScoredProperty che compongono ogni istanza di opzione e il valore assegnato a ogni elemento ScoredProperty non devono essere modificate. Lo stesso vale per le istanze di proprietà che costituiscono ogni istanza di ParameterDef.

Per un elenco di istanze di proprietà aggiuntive che devono essere fornite per definire completamente i costrutti e i parametri delle funzionalità/opzioni, vedere [ParameterDef](parameterdef.md) e [ParameterInit](parameterinit.md). Ogni funzionalità, ad esempio, deve specificare il proprio comportamento dell'interfaccia utente, in particolare se è possibile selezionare una o più istanze di opzione per ogni funzionalità in una sola volta. Il documento parole chiave di Print Schema definisce queste istanze di proprietà, dove devono essere visualizzate all'interno del documento PrintCapabilities e quali istanze di valore definite nelle parole chiave dello schema di stampa sono disponibili.

Il provider PrintCapabilities è responsabile della creazione del valore appropriato per tutte le istanze delle proprietà dipendenti dalla configurazione. Se, ad esempio, la frequenza di stampa dipende sia dalla modalità colore che dalla risoluzione utilizzata, il provider PrintCapabilities deve prendere nota della modalità di colore e delle impostazioni di risoluzione specificate nell'oggetto PrintTicket fornito dal client e deve indicare il valore appropriato per la velocità di stampa. Si noti che ogni istanza di ScoredProperty deve essere a valore singolo. l'istanza del valore non può essere modificata quando viene modificata la configurazione del dispositivo.

Si noti inoltre che le istanze di proprietà definite nelle parole chiave Print Schema devono essere visualizzate nella posizione specificata. Non possono essere visualizzati in posizioni arbitrarie all'interno di un documento PrintCapabilities. Le istanze di proprietà definite privatamente possono essere visualizzate in qualsiasi punto, anche come sottoproprietà all'interno delle istanze di proprietà definite dallo schema.

Si noti che un conflitto funzionale tra le impostazioni viene definito come due elementi dello schema di stampa non in conflitto che hanno una funzione simile ma sono funzionalità diverse. Un esempio è JobDuplexAllDocumentsContiguously e DocumentDuplex; entrambi rappresentano la funzione duplex del dispositivo, ma si differenziano per l'applicazione della funzione, uno applicato all'intero processo in modo contiguo e uno ai documenti. Nel caso in cui vengano specificati due elementi di questo tipo, la precedenza viene determinata dal Producer PrintCapabilities e dall'utente PrintTicket. È responsabilità del Producer PrintCapabilities indicare correttamente i vincoli tra gli elementi in conflitto tramite l'attributo "vincolato". Gli elementi nello schema di stampa pubblico che presentano questo conflitto semantico sono identificati nella definizione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



