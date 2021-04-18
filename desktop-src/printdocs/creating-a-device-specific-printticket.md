---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 487f294f-dfe0-48f8-9077-06c55c3af8f1
title: Creazione di un Device-Specific PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d31644f25f231f7121e2e492bc3f41a81b82d0b4
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106321057"
---
# <a name="creating-a-device-specific-printticket"></a>Creazione di un Device-Specific PrintTicket

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un oggetto PrintTicket specifico del dispositivo è destinato a un determinato dispositivo e pertanto non è generalmente portabile tra più dispositivi.

I passaggi illustrati nell'elenco seguente devono essere usati quando si crea un oggetto PrintTicket specifico del dispositivo.

1.  Ottenere un documento PrintCapabilities contenente solo le istanze della funzionalità pertinenti per il dispositivo. Richiedere un documento PrintCapabilities predefinito. Non è necessario specificare un oggetto PrintTicket di input perché gli attributi del dispositivo (istanze e parametri delle funzionalità e delle opzioni) usati per costruire l'oggetto PrintTicket sono indipendenti dalla configurazione.

2.  Creare un documento XML vuoto contenente la radice PrintTicket. Assegnare un prefisso dello spazio dei nomi allo spazio dei nomi dello schema di stampa e assegnare i prefissi per tutti gli altri spazi dei nomi che verranno utilizzati dal PrintTicket. Specificare la versione dello schema PrintTicket.

3.  È possibile definire le impostazioni nel PrintTicket per tutte le funzionalità e l'istanza di ParameterDef segnalate nel documento PrintCapabilities o solo quelle di interesse. Se all'interfaccia PrintTicket viene presentato un oggetto PrintTicket parziale, vengono automaticamente fornite le impostazioni predefinite per le istanze ParameterDef e feature omesse durante la convalida PrintTicket.

4.  Esaminare il documento PrintCapabilities per le istanze di funzionalità e determinare quale di questi si desidera definire nel PrintTicket. Aggiungere queste istanze della funzionalità al PrintTicket, ma non trasferire il contenuto delle istanze della funzionalità al PrintTicket. Se si trasferisce una funzionalità secondaria, è necessario trasferire anche la funzionalità padre e la relazione padre-figlio deve essere mantenuta nell'oggetto PrintTicket.

    Per ogni funzionalità trasferita, determinare le istanze delle opzioni applicabili al PrintTicket. Trasferire l'intera opzione come definito nel documento PrintCapabilities, quindi rimuovere tutte le istanze di proprietà presenti. Le istanze di proprietà vengono utilizzate all'interno di documenti PrintCapabilities, ma non svolgono alcuna funzione nell'oggetto PrintTicket. Mantenere tutte le istanze di ScoredProperty, assicurandosi di conservarne la posizione; si tratta di una parte intrinseca della definizione dell'opzione.

5.  È anche possibile aggiungere istanze di proprietà a qualsiasi istanza di ScoredProperty. Le istanze di proprietà vengono utilizzate solo se il provider PrintTicket ne supporta in modo esplicito l'utilizzo. Ogni provider deve documentare lo scopo e l'utilizzo di tutte le istanze di proprietà supportate. Si noti che durante la convalida tutte le istanze di proprietà contenute in un'istanza di opzione vengono rimosse, a meno che lo spazio dei nomi della proprietà non venga riconosciuto dal provider PrintCapabilities o PrintTicket di destinazione e un'opzione candidata venga trovata nel documento PrintCapabilities le cui istanze ScoredProperty corrispondono perfettamente a quelle definite nell'opzione di riferimento.

6.  Se le parole chiave dello schema di stampa impostano la proprietà SelectionType su PickMany per una particolare funzionalità, è possibile selezionare più di un'opzione per tale funzionalità, a condizione che l'opzione designata come IdentityOption non sia una di quelle selezionate. IdentityOption nello schema di stampa ha lo stesso effetto dell'opzione None nei file PPD di PostScript e nei file Unidrv GPD; funge da no-op.

7.  Esaminare il documento PrintCapabilities per le istanze di ParameterDef da impostare nel PrintTicket. Per ogni istanza di ParameterDef di questo tipo, selezionare un valore da utilizzare nell'istanza di ParameterInit nel PrintTicket. Questo valore deve essere del tipo di dati corretto e deve rientrare nell'intervallo definito nell'istanza di ParameterDef e deve soddisfare tutti gli altri requisiti specificati nell'istanza di ParameterDef. Utilizzare un'istanza di ParameterInit per inizializzare il parametro sul valore selezionato.

8.  Esaminare il contenuto di ogni istanza di opzione visualizzata nel PrintTicket per le occorrenze di istanze di ParameterRef. Se un'istanza di ParameterInit corrispondente non è già presente nel PrintTicket, seguire il passaggio precedente per creare un'istanza di ParameterInit nel PrintTicket. Lo scopo di questa istanza di ParameterInit è inizializzare il parametro a cui fa riferimento l'istanza di ParameterRef.

9.  Tenere presente che i conflitti di vincolo possono impedire al dispositivo di applicare la configurazione specificata nel PrintTicket. Se necessario, il processo di convalida modifica la configurazione definita nel PrintTicket a una che è priva di conflitti.

10. Esaminare le parole chiave dello schema di stampa per le istanze di proprietà che devono essere presenti nel PrintTicket. Aggiungere un'istanza di proprietà al PrintTicket per ogni richiesta e fornire un valore appropriato per tale istanza usando il tipo di elemento value. Verificare che le istanze delle proprietà si trovino correttamente all'interno dell'oggetto PrintTicket.

11. Esaminare le istanze di proprietà facoltative nello schema PrintTicket. Se sono presenti istanze di queste proprietà che devono essere presenti nel PrintTicket, crearle nel PrintTicket.

12. È anche possibile aggiungere istanze di proprietà definite privatamente a livello di radice o a qualsiasi funzionalità, opzione o istanza di proprietà. Si noti tuttavia che queste istanze di proprietà definite privatamente vengono rimosse durante la convalida, a meno che lo spazio dei nomi a cui appartengono non sia riconosciuto dal provider PrintCapabilities o PrintTicket di destinazione. Inoltre, le istanze di proprietà visualizzate in un punto qualsiasi all'interno di un'istanza di opzione vengono rimosse durante la convalida, a meno che il documento PrintCapabilities non contenga un'opzione che rappresenta una corrispondenza perfetta. Due istanze delle opzioni rappresentano una corrispondenza perfetta se ogni ScoredProperty in un'istanza di opzione ha un ScoredProperty corrispondente nell'altro e i valori delle istanze ScoredProperty sono gli stessi. Consultare lo schema privato del provider PrintTicket per un elenco di istanze di proprietà private riconosciute e dei relativi utilizzi.

13. Gli elementi figlio dello stesso tipo di elemento potrebbero non annidarsi a una profondità superiore a 10 elementi. Questa regola si applica in modo indipendente a ogni tipo di elemento che è possibile definire.

> [!Note]  
> Il contenuto XML di PrintTicket deve essere codificato con UTF-8 o UTF-16.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



