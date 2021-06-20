---
description: Informazioni su come costruire un PrintTicket generico, nel caso in cui il documento PrintCapabilities per il dispositivo non sia disponibile.
ms.assetid: 1f991b6b-8443-4234-ad46-dc4220e34c5c
title: Creazione di un printticket generico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69e611205663138b9cc3c0d3cd315c2c19d2d7e6
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409524"
---
# <a name="creating-a-generic-printticket"></a>Creazione di un printticket generico

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Se il documento PrintCapabilities per il dispositivo non è disponibile o se il dispositivo di destinazione è sconosciuto, è necessario costruire un PrintTicket generico. Poiché non esiste alcun documento PrintCapabilities che fornisce un set di elementi Feature e Option o parametri, le istanze supportate di questi tipi di elementi devono essere ottenute direttamente dalle parole chiave dello schema di stampa.

I passaggi illustrati nell'elenco seguente devono essere usati quando si crea un PrintTicket generico.

1.  Creare un documento XML vuoto contenente la radice PrintTicket. Assegnare un prefisso dello spazio dei nomi allo spazio dei nomi Dello schema di stampa. Specificare la versione dello schema.

2.  Esaminare le istanze di Funzionalità nelle parole chiave dello schema di stampa e determinare quali di queste si desidera definire in PrintTicket. Aggiungere queste istanze di funzionalità a PrintTicket. Quando si trasferisce una funzionalità secondaria, è necessario trasferire la funzionalità padre e mantenere la relazione padre-figlio tra la funzionalità e la funzionalità secondaria in PrintTicket.

    Per ogni istanza di funzionalità che si trasferisce, determinare quali istanze di Opzione sono applicabili a PrintTicket. Da questo set di istanze option trasferire ogni intera istanza di Option così come viene visualizzata nello schema di stampa e quindi rimuovere tutte le istanze property presenti, con la possibile eccezione di quelle che hanno significato per PrintTicket. Mantenere tutte le istanze scoredProperty, assicurando di conservarne la posizione. sono una parte intrinseca della definizione di opzione.

3.  È anche possibile aggiungere istanze property a qualsiasi scoredProperty. Gli elementi proprietà sono applicabili solo se il provider PrintTicket ne supporta in modo esplicito l'utilizzo. Ogni provider deve documentare lo scopo e l'uso di tutte le istanze property supportate. Poiché non si ha idea del provider che eelaborare PrintTicket, è possibile aggiungere solo le istanze Property supportate in modo esplicito dal provider PrintTicket di sistema.

4.  Se le parole chiave dello schema di stampa impostano la proprietà SelectionType su PickMany per una particolare funzionalità, è possibile selezionare più di un'opzione per tale funzionalità, a condizione che l'opzione designata come IdentityOption non sia una di quelle selezionate. IdentityOption nello schema di stampa ha lo stesso effetto dell'opzione Nessuno nei file PPD Postscript e Nei file GPD Unidrv. funge da no-op.

5.  Esaminare le parole chiave dello schema di stampa per le istanze ParameterDef che devono essere inizializzate in PrintTicket. Per ogni istanza parameterdef di questo tipo, selezionare il valore da usare nell'istanza ParameterInit in PrintTicket. Questo valore deve essere del tipo di dati corretto, deve rientrare nell'intervallo definito nell'istanza ParameterDef e deve soddisfare tutti gli altri requisiti specificati nell'istanza ParameterDef. Usare un'istanza ParameterInit per inizializzare il parametro sul valore selezionato.

    Se si sviluppa un componente dell'interfaccia utente, progettare i metodi di generazione di PrintTicket in modo che gli utenti possano immettere il valore per l'elemento ParameterInit. Inoltre, il metodo di immissione dell'interfaccia utente deve osservare e rispettare eventuali restrizioni di input specificate dall'elemento ParameterDef associato.

6.  Esaminare il contenuto di ogni istanza di Opzione visualizzata in PrintTicket per le occorrenze di ParameterRef. Se un'istanza ParameterInit corrispondente non è già presente in PrintTicket, seguire il passaggio precedente per creare un'istanza ParameterInit in PrintTicket. Lo scopo di questa istanza ParameterInit è inizializzare il parametro a cui fa riferimento l'istanza parameterRef.

7.  Tenere presente che il dispositivo che elabora il processo potrebbe non supportare tutte le funzionalità specificate in PrintTicket. Tenere presente anche che una funzionalità denominata potrebbe essere supportata, ma un'opzione specificata di tale funzionalità potrebbe non essere . Le stesse avvertenze si applicano ai parametri. Anche se un dispositivo supporta un parametro denominato, il valore specificato nell'istanza ParameterInit potrebbe non essere compreso nell'intervallo valido per il dispositivo.

8.  Esaminare le parole chiave dello schema di stampa per le istanze property che devono essere presenti in PrintTicket. Aggiungere un'istanza Property per ognuna di queste proprietà a PrintTicket e specificare un valore appropriato usando il tipo di elemento Value. Assicurarsi che le istanze property si trovino correttamente all'interno di PrintTicket. Assicurarsi di consultare lo schema PrintTicket anziché lo schema PrintCapabilities.

9.  Esaminare le istanze facoltative di Property definite nello schema PrintTicket. Se sono presenti istanze property di questo tipo che devono essere presenti in PrintTicket, crearle in PrintTicket.

10. Gli elementi figlio dello stesso tipo di elemento non possono annidare fino a una profondità superiore a 10 elementi. Questa regola si applica in modo indipendente a ogni tipo di elemento che può essere definito.

> [!Note]  
> Il contenuto XML PrintTicket DEVE essere codificato usando UTF-8 o UTF-16.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



