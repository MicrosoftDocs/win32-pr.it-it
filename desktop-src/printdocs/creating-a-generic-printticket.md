---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 1f991b6b-8443-4234-ad46-dc4220e34c5c
title: Creazione di un oggetto PrintTicket generico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c34281eda82a48ea0ac4077248547522ddc305ea
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320872"
---
# <a name="creating-a-generic-printticket"></a>Creazione di un oggetto PrintTicket generico

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Se il documento PrintCapabilities per il dispositivo non è disponibile o se il dispositivo di destinazione è sconosciuto, è necessario creare un oggetto PrintTicket generico. Poiché non esiste un documento PrintCapabilities che fornisce un set di elementi Feature e Option, o parametri, le istanze supportate di questi tipi di elemento devono essere ottenute direttamente dalle parole chiave Print Schema.

Quando si crea un oggetto PrintTicket generico, è necessario usare i passaggi illustrati nell'elenco seguente.

1.  Creare un documento XML vuoto contenente la radice PrintTicket. Assegnare un prefisso dello spazio dei nomi allo spazio dei nomi dello schema di stampa. Specificare la versione dello schema.

2.  Esaminare le istanze della funzionalità nelle parole chiave dello schema di stampa e determinare quale di questi si desidera definire nel PrintTicket. Aggiungere queste istanze della funzionalità al PrintTicket. Quando si trasferisce una funzionalità secondaria, è necessario trasferire la funzionalità padre e mantenere la relazione padre-figlio tra la funzionalità e la sottofunzionalità del PrintTicket.

    Per ogni istanza di funzionalità trasferita, determinare le istanze delle opzioni applicabili al PrintTicket. Da questo set di istanze di opzioni, trasferire ogni intera istanza di opzione come appare nello schema di stampa, quindi rimuovere tutte le istanze di proprietà presenti, con la possibile eccezione di quelle che hanno significato per l'oggetto PrintTicket. Mantenere tutte le istanze di ScoredProperty, assicurandosi di conservarne la posizione; si tratta di una parte intrinseca della definizione dell'opzione.

3.  È anche possibile aggiungere istanze di proprietà a qualsiasi ScoredProperty. Gli elementi Property sono applicabili solo se il provider PrintTicket ne supporta in modo esplicito l'utilizzo. Ogni provider deve documentare lo scopo e l'utilizzo di tutte le istanze di proprietà supportate. Poiché non si ha idea del provider che elaborerà l'oggetto PrintTicket, potrebbe essere necessario accodare solo le istanze di proprietà supportate in modo esplicito dal provider PrintTicket del sistema.

4.  Se le parole chiave dello schema di stampa impostano la proprietà SelectionType su PickMany per una particolare funzionalità, è possibile selezionare più di un'opzione per tale funzionalità, a condizione che l'opzione designata come IdentityOption non sia una di quelle selezionate. IdentityOption nello schema di stampa ha lo stesso effetto dell'opzione None nei file PPD di PostScript e nei file Unidrv GPD; funge da no-op.

5.  Esaminare le parole chiave dello schema di stampa per le istanze di ParameterDef che devono essere inizializzate nel PrintTicket. Per ogni istanza di ParameterDef di questo tipo, selezionare il valore da utilizzare nell'istanza di ParameterInit nel PrintTicket. Questo valore deve essere del tipo di dati corretto, deve rientrare nell'intervallo definito nell'istanza di ParameterDef e deve soddisfare tutti gli altri requisiti specificati nell'istanza di ParameterDef. Utilizzare un'istanza di ParameterInit per inizializzare il parametro sul valore selezionato.

    Se si sviluppa un componente dell'interfaccia utente, progettare i metodi di generazione PrintTicket in modo che gli utenti possano immettere il valore per l'elemento ParameterInit. Inoltre, il metodo di immissione dell'interfaccia utente deve osservare e rispettare le restrizioni di input specificate dall'elemento ParameterDef associato.

6.  Esaminare il contenuto di ogni istanza di opzione visualizzata nel PrintTicket per le occorrenze di ParameterRef. Se un'istanza di ParameterInit corrispondente non è già presente nel PrintTicket, seguire il passaggio precedente per creare un'istanza di ParameterInit nel PrintTicket. Lo scopo di questa istanza di ParameterInit è inizializzare il parametro a cui fa riferimento l'istanza di ParameterRef.

7.  Tenere presente che il dispositivo che elabora il processo potrebbe non supportare tutte le funzionalità specificate in PrintTicket. Tenere presente inoltre che una funzionalità denominata potrebbe essere supportata, ma è possibile che un'opzione specificata della funzionalità non sia. Le stesse avvertenze si applicano ai parametri. Anche se un dispositivo supporta un parametro denominato, il valore specificato nell'istanza di ParameterInit potrebbe non essere compreso nell'intervallo valido per il dispositivo.

8.  Esaminare le parole chiave dello schema di stampa per le istanze di proprietà che devono essere presenti nel PrintTicket. Aggiungere un'istanza di proprietà per ognuno di essi all'oggetto PrintTicket e fornire un valore appropriato per tale istanza usando il tipo di elemento value. Verificare che le istanze delle proprietà si trovino correttamente all'interno dell'oggetto PrintTicket. Assicurarsi di consultare lo schema PrintTicket invece dello schema PrintCapabilities.

9.  Esaminare le istanze di proprietà facoltative definite nello schema PrintTicket. Se sono presenti istanze di queste proprietà che devono essere presenti nel PrintTicket, crearle nel PrintTicket.

10. Gli elementi figlio dello stesso tipo di elemento potrebbero non annidarsi a una profondità superiore a 10 elementi. Questa regola si applica in modo indipendente a ogni tipo di elemento che è possibile definire.

> [!Note]  
> Il contenuto XML di PrintTicket deve essere codificato con UTF-8 o UTF-16.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



