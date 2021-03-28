---
description: A partire da Windows XP, il pannello di controllo supporta la categorizzazione degli elementi del pannello di controllo. Gli elementi sono registrati per essere visualizzati in una o più categorie. Non è possibile creare nuove categorie.
title: Assegnazione delle categorie del pannello di controllo
ms.topic: article
ms.date: 05/31/2018
ms.assetid: e189b57d-c066-4f28-b1d5-3e05d6c6eeb2
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: bade62cda23c2d2f66ffdfd70f3f555a243f3efc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977407"
---
# <a name="assigning-control-panel-categories"></a>Assegnazione delle categorie del pannello di controllo

A partire da Windows XP, il pannello di controllo supporta la categorizzazione degli elementi del pannello di controllo. Gli elementi sono registrati per essere visualizzati in una o più categorie. Non è possibile creare nuove categorie.

Per registrare un elemento del pannello di controllo in una o più categorie, aggiungere i valori come illustrato nella sezione registrazione elemento del pannello di controllo [eseguibile](registering-control-panel-items.md) o [registrazione elemento](registering-control-panel-items.md) del pannello di controllo di registrazione degli [elementi del pannello di controllo](registering-control-panel-items.md), a seconda dei casi.



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
<td>&quot;Tutti gli elementi del pannello di controllo&quot;</td>
<td>&quot;Opzioni aggiuntive&quot;
<blockquote>
[!Note]<br />
In questa categoria vengono visualizzati tutti gli elementi del pannello di controllo che non specificano un ID categoria.
</blockquote>
<br/></td>
<td>&quot;Altre opzioni del pannello di controllo&quot;
<blockquote>
[!Note]<br />
In questa categoria vengono visualizzati tutti gli elementi del pannello di controllo che non specificano un ID categoria.
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
<td>Non più utilizzata. Tutti gli elementi che si aggiungono solo alla categoria 4 vengono visualizzati nella categoria 2 (hardware e suono).</td>
<td>Non più utilizzata. Tutti gli elementi che si aggiungono solo alla categoria 4 vengono visualizzati nella categoria 2 (hardware e suono).</td>
<td>&quot;Suoni, sintesi vocale e dispositivi audio&quot;</td>
</tr>
<tr class="even">
<td>5</td>
<td>&quot;Sistema e sicurezza&quot;</td>
<td>&quot;Sistema e manutenzione&quot;</td>
<td>&quot;Prestazioni e manutenzione&quot;</td>
</tr>
<tr class="odd">
<td>6</td>
<td>&quot;Clock, lingua e area&quot;</td>
<td>&quot;Clock, lingua e area&quot;</td>
<td>&quot;Data, ora, lingua e opzioni internazionali&quot;</td>
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
Quando non si è connessi a un dominio, questo è denominato &quot; account utente e sicurezza della famiglia &quot; .
</blockquote>
<br/></td>
<td>&quot;Account utente&quot;
<blockquote>
[!Note]<br />
Quando non si è connessi a un dominio, questo è denominato &quot; account utente e sicurezza della famiglia &quot; .
</blockquote>
<br/></td>
<td>&quot;Account utente&quot;</td>
</tr>
<tr class="odd">
<td>10</td>
<td>Non più utilizzata. Gli elementi registrati in questa categoria vengono visualizzati nella categoria 5 (sistema e sicurezza).</td>
<td>&quot;Sicurezza&quot;</td>
<td>&quot;Centro sicurezza&quot;
<blockquote>
[!Note]<br />
Disponibile solo in Windows XP Service Pack 2 (SP2) o versioni successive.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>11</td>
<td>Non più utilizzata. Gli elementi registrati in questa categoria vengono visualizzati nella categoria 0 (tutti gli elementi del pannello di controllo).</td>
<td>&quot;PC portatile&quot;
<blockquote>
[!Note]<br />
Questa categoria è visibile solo nei PC portatili.
</blockquote>
<br/></td>
<td>Non usato.</td>
</tr>
</tbody>
</table>



 

In Windows XP le categorie **aggiungere o rimuovere programmi** e **account utente** funzionano in modo diverso rispetto ad altre categorie nel pannello di controllo. Quando uno o più elementi vengono aggiunti a una di queste due categorie, il collegamento associato nel pannello di controllo apre una pagina di categoria. Gli elementi registrati vengono visualizzati nella parte inferiore della pagina sotto l'intestazione "oppure selezionare un'icona del pannello di controllo". Quando non viene registrato alcun elemento per una di queste categorie, il collegamento associato nel pannello di controllo richiama direttamente l'elemento Windows standard per quella categoria. In Windows Vista e versioni successive, la categoria **programmi** e la categoria **account utente** non dispongono di questa proprietà.

La categoria **Centro sicurezza** , disponibile solo in Windows XP SP2, è anche in qualche modo non standard. Se si fa clic su questa categoria, viene visualizzata la pagina **Centro sicurezza** in una nuova finestra. Gli elementi registrati per il **Centro sicurezza** vengono visualizzati nella parte inferiore della pagina sotto l'intestazione **Gestisci impostazioni di sicurezza per:**. Fare clic su un'icona per aprire l'elemento del pannello di controllo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Elementi del pannello di controllo](control-panel-applications.md)
</dt> <dt>

[Linee guida sull'esperienza utente](user-experience-guidelines.md)
</dt> <dt>

[Registrazione degli elementi del pannello di controllo](registering-control-panel-items.md)
</dt> <dt>

[Uso di CPLApplet](using-cplapplet.md)
</dt> <dt>

[Elaborazione del messaggio del pannello di controllo](message-processing.md)
</dt> <dt>

[Esecuzione degli elementi del pannello di controllo](executing-control-panel-items.md)
</dt> <dt>

[Estensione degli elementi del pannello di controllo di sistema](extending-system-control-panel-items.md)
</dt> <dt>

[Creazione di collegamenti alle attività ricercabili per un elemento del pannello di controllo](creating-searchable-task-links.md)
</dt> <dt>

[Accesso al pannello di controllo in modalità provvisoria in Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 




