---
title: Modello a oggetti
description: Nella tabella seguente sono elencati i tipi di oggetto che possono essere modificati tramite i vari set di API forniti da Windows Filtering Platform (PAM).
ms.assetid: 6931583f-785c-4e27-b5e4-d185d23a54ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa90b4757a39617616c6f83b6b79fe322b2e64c8
ms.sourcegitcommit: 60ad94096619da5476f9bbcd4cc231b40b6f5358
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104046352"
---
# <a name="object-model"></a>Modello a oggetti

Nella tabella seguente sono elencati i tipi di oggetto che possono essere modificati tramite i vari set di API forniti da Windows Filtering Platform (PAM).



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
<td>Regola che governa la classificazione. Se le condizioni vengono soddisfatte, viene richiamata l'azione. <br/> Si tratta dell'oggetto più complesso esposto da WFP, poiché unisce tutti gli altri tipi di oggetto. <br/></td>
<td><ul>
<li>Matrice di condizioni</li>
<li>Azione (Consenti, blocca, callout)</li>
<li><a href="filter-weight-assignment.md">Weight</a></li>
<li>Context</li>
</ul></td>
<td>&quot;Blocca il traffico con una porta TCP maggiore di 1024.&quot; <br/> &quot;Callout agli ID per tutto il traffico non protetto.&quot;<br/></td>
</tr>
<tr class="even">
<td>Callout</td>
<td>Set di funzioni che partecipano al processo di classificazione.<br/> Consente di eseguire l'elaborazione di pacchetti personalizzati quando vengono soddisfatte determinate condizioni.<br/></td>
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
<li>Schema per i filtri che è possibile aggiungere al livello</li>
</ul></td>
<td>Livello trasporto in ingresso<br/></td>
</tr>
<tr class="even">
<td>Sottolivello</td>
<td>Sottocomponente di un livello, utilizzato nell' <a href="filter-arbitration.md">arbitro di filtro</a>.<br/></td>
<td><ul>
<li>Peso</li>
</ul></td>
<td>Sottolivello del tunnel IPsec<br/></td>
</tr>
<tr class="odd">
<td>Provider</td>
<td>Provider di criteri in cui è stata compilata una soluzione in WFP.<br/> Viene utilizzato esclusivamente per la gestione; non influisce sull'elaborazione dei pacchetti in fase di esecuzione.<br/></td>
<td><ul>
<li>ID</li>
<li>Nome del servizio</li>
</ul></td>
<td>Windows Firewall con sicurezza avanzata<br/> Applicazione di filtro URL di terze parti<br/></td>
</tr>
<tr class="even">
<td>Contesto del provider</td>
<td>BLOB di dati utilizzato da un provider di criteri per archiviare informazioni di contesto arbitrarie. <br/> Viene usato per passare le informazioni di configurazione personalizzate a un callout.<br/> Il modo più comune per usare le informazioni sul contesto consiste nel fare in modo che i filtri facciano riferimento a un contesto del provider. <br/></td>
<td><ul>
<li>ID</li>
<li>BLOB di dati</li>
</ul></td>
<td>IPsec archivia le impostazioni di autenticazione nel motore di filtro di base (BFE). La &quot; &quot; proprietà di contesto di un filtro indica le impostazioni di autenticazione da usare per il traffico descritto dal filtro.<br/> Lo shim di selezione della certificazione SSL archivia le informazioni di certificazione in un contesto del provider. <br/></td>
</tr>
</tbody>
</table>



 

I tipi di oggetti esposti dall'API PAM hanno una semantica coerente. Le azioni di aggiunta, enumerazione, sottoscrizione e così via sono simili per tutti i tipi di oggetto.

Ogni tipo di oggetto è rappresentato da una struttura di dati (ad esempio, [**FWPM \_ FILTER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter0)). Per ridurre al minimo il numero di strutture di dati diverse esposte dall'API Pam, viene utilizzata la stessa struttura di dati per l'aggiunta di nuovi oggetti e il recupero di quelli esistenti. In questo modo, possono essere presenti campi in ogni struttura di dati che vengono ignorati quando si aggiunge un nuovo oggetto perché questi campi sono compilati dal motore di filtro di base (BFE) e non dal chiamante. Ad esempio, una struttura di dati **FWPM \_ FILTER0** ha un campo **FilterId** che contiene il **LUID** **del FWPS FILTER0 \_ corrispondente.** Questo **LUID** viene assegnato da BFE e pertanto questo campo viene ignorato nella chiamata a [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione degli oggetti](object-management.md)
</dt> </dl>

 

 





