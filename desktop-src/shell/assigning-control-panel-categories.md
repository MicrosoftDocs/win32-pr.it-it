---
description: A Windows XP, Pannello di controllo supporta la categorizzazione Pannello di controllo elementi. Gli elementi vengono registrati per essere visualizzati in una o più categorie. Non è possibile creare nuove categorie.
title: Assegnazione di Pannello di controllo categorie
ms.topic: article
ms.date: 05/31/2018
ms.assetid: e189b57d-c066-4f28-b1d5-3e05d6c6eeb2
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 0d70854177baecf6261d550bc5ad37cf5319eed323ae9b17f5fd281118acd8b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119593631"
---
# <a name="assigning-control-panel-categories"></a>Assegnazione di Pannello di controllo categorie

A Windows XP, Pannello di controllo supporta la categorizzazione Pannello di controllo elementi. Gli elementi vengono registrati per essere visualizzati in una o più categorie. Non è possibile creare nuove categorie.

Per registrare un elemento Pannello di controllo in una o più categorie, aggiungere i valori come illustrato nella sezione Registrazione elemento eseguibile [Pannello di controllo](registering-control-panel-items.md) o REGISTRAZIONE ELEMENTO DLL Pannello di controllo di Registrazione elementi Pannello di controllo [,](registering-control-panel-items.md)in base [alle](registering-control-panel-items.md) esigenze.



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>ID della categoria</th>
<th>Nome categoria (Windows 7)</th>
<th>Nome categoria (Windows Vista)</th>
<th>Nome categoria (Windows XP)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0</td>
<td>&quot;Tutti Pannello di controllo elementi&quot;</td>
<td>&quot;Opzioni aggiuntive&quot;
<blockquote>
[!Note]<br />
Qualsiasi Pannello di controllo elemento che non specifica un ID categoria viene visualizzato in questa categoria.
</blockquote>
<br/></td>
<td>&quot;Altre Pannello di controllo opzioni&quot;
<blockquote>
[!Note]<br />
Qualsiasi Pannello di controllo elemento che non specifica un ID categoria viene visualizzato in questa categoria.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>1</td>
<td>&quot;Aspetto e personalizzazione&quot;</td>
<td>&quot;Aspetto e personalizzazione&quot;</td>
<td>&quot;Aspetto e temi&quot;</td>
</tr>
<tr class="odd">
<td>2</td>
<td>&quot;Hardware e audio&quot;</td>
<td>&quot;Hardware e audio&quot;</td>
<td>&quot;Stampanti e altro hardware&quot;</td>
</tr>
<tr class="even">
<td>3</td>
<td>&quot;Rete e Internet&quot;</td>
<td>&quot;Rete e Internet&quot;</td>
<td>&quot;Connessioni di rete e Internet&quot;</td>
</tr>
<tr class="odd">
<td>4</td>
<td>Non più utilizzata. Qualsiasi elemento che si aggiunge solo alla categoria 4 viene visualizzato nella categoria 2 (Hardware e suono).</td>
<td>Non più utilizzata. Qualsiasi elemento che si aggiunge solo alla categoria 4 viene visualizzato nella categoria 2 (Hardware e suono).</td>
<td>&quot;Suoni, voce e dispositivi audio&quot;</td>
</tr>
<tr class="even">
<td>5</td>
<td>&quot;Sistema e sicurezza&quot;</td>
<td>&quot;Sistema e manutenzione&quot;</td>
<td>&quot;Prestazioni e manutenzione&quot;</td>
</tr>
<tr class="odd">
<td>6</td>
<td>&quot;Orologio, lingua e area geografica&quot;</td>
<td>&quot;Orologio, lingua e area geografica&quot;</td>
<td>&quot;Opzioni relative a data, ora, lingua e impostazioni internazionali&quot;</td>
</tr>
<tr class="even">
<td>7</td>
<td>&quot;Ease of Access&quot;</td>
<td>&quot;Ease of Access&quot;</td>
<td>&quot;Opzioni di accessibilità&quot;</td>
</tr>
<tr class="odd">
<td>8</td>
<td>&quot;Programs&quot;</td>
<td>&quot;Programs&quot;</td>
<td>&quot;Installazione applicazioni&quot;</td>
</tr>
<tr class="even">
<td>9</td>
<td>&quot;Account utente&quot;
<blockquote>
[!Note]<br />
Quando non si è connessi a un dominio, si tratta di account &quot; utente e Family Safety &quot; .
</blockquote>
<br/></td>
<td>&quot;Account utente&quot;
<blockquote>
[!Note]<br />
Quando non si è connessi a un dominio, si tratta di account &quot; utente e Family Safety &quot; .
</blockquote>
<br/></td>
<td>&quot;Account utente&quot;</td>
</tr>
<tr class="odd">
<td>10</td>
<td>Non più utilizzata. Gli elementi registrati in questa categoria vengono visualizzati nella categoria 5 (Sistema e sicurezza).</td>
<td>&quot;Sicurezza&quot;</td>
<td>&quot;Centro sicurezza&quot;
<blockquote>
[!Note]<br />
Disponibile solo in Windows XP Service Pack 2 (SP2) o versione successiva.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>11</td>
<td>Non più utilizzata. Gli elementi registrati in questa categoria vengono visualizzati nella categoria 0 (Tutti Pannello di controllo elementi).</td>
<td>&quot;PC per dispositivi mobili&quot;
<blockquote>
[!Note]<br />
Questa categoria è visibile solo nei PC mobili.
</blockquote>
<br/></td>
<td>Non usato.</td>
</tr>
</tbody>
</table>



 

In Windows XP, le  categorie Installazione  applicazioni e Account utente funzionano in modo leggermente diverso rispetto ad altre categorie in Pannello di controllo. Quando uno o più elementi vengono aggiunti a una di queste due categorie, il collegamento associato in Pannello di controllo apre una pagina di categoria. Gli elementi registrati vengono visualizzati nella parte inferiore della pagina sotto l'intestazione "o Selezionare un'Pannello di controllo icona". Quando non viene registrato alcun elemento per una di queste categorie, il collegamento associato in Pannello di controllo richiama direttamente l'elemento Windows standard per tale categoria. In Windows Vista e versioni successive, la **categoria** Programmi e la **categoria Account** utente non hanno questa proprietà.

Anche **la categoria Del** Centro sicurezza, disponibile solo in Windows XP SP2, è in qualche modo non standard. Facendo clic su questa categoria si apre **la pagina Centro** sicurezza in una nuova finestra. Gli elementi registrati **per il Centro sicurezza** vengono visualizzati nella parte inferiore della pagina sotto l'intestazione Gestisci impostazioni di sicurezza **per:**. Facendo clic su un'icona si apre Pannello di controllo elemento.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pannello di controllo elementi](control-panel-applications.md)
</dt> <dt>

[Linee guida sull'esperienza utente](user-experience-guidelines.md)
</dt> <dt>

[Registrazione di Pannello di controllo elementi](registering-control-panel-items.md)
</dt> <dt>

[Uso di CPLApplet](using-cplapplet.md)
</dt> <dt>

[Pannello di controllo di messaggi](message-processing.md)
</dt> <dt>

[Esecuzione di Pannello di controllo elementi](executing-control-panel-items.md)
</dt> <dt>

[Estensione degli elementi Pannello di controllo sistema](extending-system-control-panel-items.md)
</dt> <dt>

[Creazione di collegamenti di attività ricercabili per un Pannello di controllo ricerca](creating-searchable-task-links.md)
</dt> <dt>

[Accesso al Pannello di controllo in Cassaforte in Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 




