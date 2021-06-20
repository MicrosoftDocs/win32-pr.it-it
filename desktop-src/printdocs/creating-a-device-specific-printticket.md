---
description: Informazioni sulla creazione di un PrintTicket specifico del dispositivo, destinato a un particolare dispositivo e portabile tra più dispositivi.
ms.assetid: 487f294f-dfe0-48f8-9077-06c55c3af8f1
title: Creazione di un Device-Specific PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 497b825bd875ada534c8c467cd18d90f2db9a2a7
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409547"
---
# <a name="creating-a-device-specific-printticket"></a>Creazione di un Device-Specific PrintTicket

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un PrintTicket specifico del dispositivo è destinato a un particolare dispositivo e pertanto non è generalmente portabile tra più dispositivi.

I passaggi illustrati nell'elenco seguente devono essere usati quando si crea un PrintTicket specifico del dispositivo.

1.  Ottenere un documento PrintCapabilities contenente solo le istanze di Funzionalità pertinenti per il dispositivo. Richiedere un documento PrintCapabilities predefinito. Non è necessario specificare un PrintTicket di input perché gli attributi del dispositivo (istanze e parametri Feature e Option) usati per costruire PrintTicket sono indipendenti dalla configurazione.

2.  Creare un documento XML vuoto contenente la radice PrintTicket. Assegnare un prefisso dello spazio dei nomi allo spazio dei nomi dello schema di stampa e assegnare prefissi per tutti gli altri spazi dei nomi che verranno usati da PrintTicket. Specificare la versione dello schema PrintTicket.

3.  È possibile definire le impostazioni in PrintTicket per ogni istanza di Feature e ParameterDef segnalata nel documento PrintCapabilities o solo per quelle di interesse. Se viene presentato un PrintTicket parziale all'interfaccia PrintTicket, vengono forniti automaticamente i valori predefiniti per le istanze Feature e ParameterDef omesse durante la convalida di PrintTicket.

4.  Esaminare il documento PrintCapabilities per le istanze di Funzionalità e determinare quali di queste si desidera definire nel PrintTicket. Aggiungere queste istanze di funzionalità a PrintTicket, ma non trasferire il contenuto delle istanze di Funzionalità a PrintTicket. Se si trasferisce una funzionalità secondaria, deve essere trasferita anche la funzionalità padre e la relazione padre-figlio deve essere mantenuta in PrintTicket.

    Per ogni funzionalità che si trasferisce, determinare quali istanze di Option sono applicabili a PrintTicket. Trasferire l'intera opzione come definito nel documento PrintCapabilities e quindi rimuovere tutte le istanze property presenti. Le istanze property vengono usate all'interno di documenti PrintCapabilities, ma non hanno alcun scopo in PrintTicket. Mantenere tutte le istanze scoredProperty, assicurando di conservarne la posizione. sono una parte intrinseca della definizione option.

5.  È anche possibile aggiungere istanze di Property a qualsiasi istanza scoredProperty. Le istanze di proprietà vengono usate solo se il provider PrintTicket ne supporta in modo esplicito l'uso. Ogni provider deve documentare lo scopo e l'uso di tutte le istanze di Property supportate. Si noti che durante la convalida, tutte le istanze property contenute in un'istanza Option vengono disattivate, a meno che lo spazio dei nomi della proprietà non sia riconosciuto dal provider PrintCapabilities o PrintTicket di destinazione e nel documento PrintCapabilities le cui istanze ScoredProperty corrispondano perfettamente a quelle definite nel riferimento Option.

6.  Se le parole chiave dello schema di stampa impostano la proprietà SelectionType su PickMany per una particolare funzionalità, è possibile selezionare più opzioni per tale funzionalità, purché l'opzione designata come IdentityOption non sia una di quelle selezionate. IdentityOption nello schema di stampa ha lo stesso effetto dell'opzione None nei file PPD Postscript e Unidrv GPD. viene utilizzato come non operativo.

7.  Esaminare il documento PrintCapabilities per le istanze ParameterDef che devono essere impostate in PrintTicket. Per ogni istanza di ParameterDef di questo tipo, selezionare un valore da usare nell'istanza ParameterInit in PrintTicket. Questo valore deve essere del tipo di dati corretto e deve rientrare nell'intervallo definito nell'istanza ParameterDef e deve soddisfare tutti gli altri requisiti specificati nell'istanza ParameterDef. Usare un'istanza ParameterInit per inizializzare il parametro sul valore selezionato.

8.  Esaminare il contenuto di ogni istanza option visualizzata in PrintTicket per le occorrenze delle istanze ParameterRef. Se un'istanza ParameterInit corrispondente non è già visualizzata in PrintTicket, seguire il passaggio precedente per creare un'istanza ParameterInit in PrintTicket. Lo scopo di questa istanza di ParameterInit è inizializzare il parametro a cui fa riferimento l'istanza parameterRef.

9.  Tenere presente che i conflitti di vincoli potrebbero impedire al dispositivo di applicare la configurazione specificata in PrintTicket. Se necessario, il processo di convalida modifica la configurazione definita in PrintTicket in una senza conflitti.

10. Esaminare le parole chiave dello schema di stampa per le istanze di proprietà che devono essere presenti in PrintTicket. Aggiungere un'istanza Property a PrintTicket per ogni richiesta e specificare un valore appropriato usando il tipo di elemento Value. Assicurarsi che le istanze di Property si trovino correttamente all'interno di PrintTicket.

11. Esaminare le istanze facoltative di Property nello schema PrintTicket. Se sono presenti istanze di proprietà di questo tipo che devono essere presenti in PrintTicket, crearle in PrintTicket.

12. È anche possibile aggiungere istanze di proprietà definite privatamente a livello di radice o a qualsiasi istanza di Funzionalità, Opzione o Proprietà. Si noti tuttavia che queste istanze di proprietà definite privatamente vengono disattivate durante la convalida, a meno che lo spazio dei nomi a cui appartengono non sia riconosciuto dal provider PrintCapabilities o PrintTicket di destinazione. Inoltre, le istanze di proprietà presenti in qualsiasi punto all'interno di un'istanza option vengono disattivate durante la convalida, a meno che il documento PrintCapabilities non contenga un'opzione che rappresenta una corrispondenza perfetta. Due istanze option sono una corrispondenza perfetta se ogni ScoredProperty in un'istanza Option ha una ScoredProperty corrispondente nell'altra e i valori delle istanze ScoredProperty sono gli stessi. Consultare lo schema privato del provider PrintTicket per un elenco delle istanze di proprietà private riconosciute e il relativo uso.

13. Gli elementi figlio dello stesso tipo di elemento non possono essere annidati fino a una profondità superiore a 10 elementi. Questa regola si applica in modo indipendente a ogni tipo di elemento che può essere definito.

> [!Note]  
> Il contenuto XML PrintTicket DEVE essere codificato usando UTF-8 o UTF-16.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



