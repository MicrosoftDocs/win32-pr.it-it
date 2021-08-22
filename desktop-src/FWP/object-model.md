---
title: Modello a oggetti
description: La tabella seguente elenca i tipi di oggetto che possono essere manipolati tramite i vari set di API forniti da Windows Filtering Platform (WFP).
ms.assetid: 6931583f-785c-4e27-b5e4-d185d23a54ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12acbb2ece5049a8c9bf19bb3796be88f4fed0fbba8d46d75b9d41e206522ce0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119255701"
---
# <a name="object-model"></a>Modello a oggetti

La tabella seguente elenca i tipi di oggetto che possono essere manipolati tramite i vari set di API forniti da Windows Filtering Platform (WFP).



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Tipo di oggetto</th>
<th>Descrizione</th>
<th>Proprietà di esempio</th>
<th>Esempio</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Filtra</td>
<td>Regola che regola la classificazione. Se le condizioni vengono soddisfatte, viene richiamata l'azione . <br/> Si tratta dell'oggetto più complesso esposto dal WFP perché riunisce tutti gli altri tipi di oggetto. <br/></td>
<td><ul>
<li>Matrice di condizioni</li>
<li>Azione (autorizzazione, blocco, callout)</li>
<li><a href="filter-weight-assignment.md">Weight</a></li>
<li>Contesto</li>
</ul></td>
<td>&quot;Bloccare il traffico con una porta TCP maggiore di 1024.&quot; <br/> &quot;Callout a IDS per tutto il traffico non protetto.&quot;<br/></td>
</tr>
<tr class="even">
<td>Callout</td>
<td>Set di funzioni che partecipano al processo di classificazione.<br/> Consente di eseguire l'elaborazione personalizzata dei pacchetti quando vengono soddisfatte determinate condizioni.<br/></td>
<td><ul>
<li>ID</li>
<li>Livello applicabile</li>
</ul></td>
<td>Driver NAT<br/></td>
</tr>
<tr class="odd">
<td>Livello</td>
<td>Contenitore di filtri nel motore di filtro. <br/> Rappresenta un punto specifico nell'elaborazione del traffico di rete in cui viene richiamato il motore di filtro.<br/></td>
<td><ul>
<li>Schema per i filtri che possono essere aggiunti al livello</li>
</ul></td>
<td>Livello trasporto in ingresso<br/></td>
</tr>
<tr class="even">
<td>Livello secondario</td>
<td>Componente secondario di un livello, utilizzato nell'arbitraggio <a href="filter-arbitration.md">dei filtri.</a><br/></td>
<td><ul>
<li>Peso</li>
</ul></td>
<td>Sottoprogetto Tunnel IPsec<br/></td>
</tr>
<tr class="odd">
<td>Provider</td>
<td>Provider di criteri che ha creato una soluzione in WFP.<br/> Viene usato esclusivamente per la gestione. non influisce sull'elaborazione dei pacchetti in fase di esecuzione.<br/></td>
<td><ul>
<li>ID</li>
<li>Nome del servizio</li>
</ul></td>
<td>Windows Firewall con sicurezza avanzata<br/> Applicazione di filtro URL di terze parti<br/></td>
</tr>
<tr class="even">
<td>Contesto del provider</td>
<td>BLOB di dati usato da un provider di criteri per archiviare informazioni di contesto arbitrarie. <br/> Viene usato per passare informazioni di configurazione personalizzate a un callout.<br/> Il modo più comune per usare le informazioni di contesto è fare in modo che i filtri fanno riferimento a un contesto del provider. <br/></td>
<td><ul>
<li>ID</li>
<li>BLOB di dati</li>
</ul></td>
<td>IPsec archivia le impostazioni di autenticazione nel Base Filtering Engine (BFE). La &quot; proprietà Context di un filtro indica le impostazioni di autenticazione da usare per il traffico descritto dal &quot; filtro.<br/> Lo shim di selezione della certificazione SSL archivierà le informazioni di certificazione in un contesto del provider. <br/></td>
</tr>
</tbody>
</table>



 

I tipi di oggetto esposti dall'API WFP hanno una semantica coerente. Le azioni di aggiunta, enumerazione, sottoscrizione e così via sono simili per tutti i tipi di oggetto.

Ogni tipo di oggetto è rappresentato da una struttura di dati , ad esempio [**FWPM \_ FILTER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter0). Per ridurre al minimo il numero di strutture di dati diverse esposte dall'API WFP, viene usata la stessa struttura di dati sia per l'aggiunta di nuovi oggetti che per il recupero di quelle esistenti. Di conseguenza, in ogni struttura di dati possono essere presenti campi che vengono ignorati quando si aggiunge un nuovo oggetto poiché questi campi vengono compilati dal Base Filtering Engine (BFE) e non dal chiamante. Ad esempio, una **struttura di dati FWPM \_ FILTER0** include un campo **filterId** che contiene il **LUID** del filtro **FWPS \_ FILTER0 corrispondente.** Questo **LUID** viene assegnato da BFE e pertanto questo campo viene ignorato nella chiamata a [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione oggetti](object-management.md)
</dt> </dl>

 

 





