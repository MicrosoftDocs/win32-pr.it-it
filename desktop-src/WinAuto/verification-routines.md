---
title: Routine di verifica
description: Questa sezione descrive le routine di verifica che possono essere eseguite da controllo dell'accessibilità dell'interfaccia utente per testare l'implementazione dell'accessibilità di un'applicazione.
ms.assetid: 0ff38f83-5741-4c0e-a070-a8385f95eba3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78eea821a4c918078c6390e33fa7046de1452f76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330215"
---
# <a name="verification-routines"></a>Routine di verifica

Questa sezione descrive le routine di verifica che possono essere eseguite da controllo dell'accessibilità dell'interfaccia utente per testare l'implementazione dell'accessibilità di un'applicazione.



<table>
<thead>
<tr class="header">
<th>Category</th>
<th>Routine</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><strong>Coerenza</strong>$ {Remove} $<br />
</td>
<td><strong>ScreenReader</strong></td>
<td>Compila tutti gli elementi visibili nella destinazione di verifica e li visualizza in un controllo ListView nell'ordine in cui un'operazione di lettura dello schermo standard li annuncia a un utente.</td>
</tr>
<tr class="even">
<td><strong>UiaScreenReader</strong></td>
<td>Uguale a <strong>ScreenReader</strong>, ma per le implementazioni di UIA.</td>

</tr>
<tr class="odd">
<td rowspan="2"><strong>Spostamento</strong>di $ {Remove} $<br />
</td>
<td><strong>CheckTreeDepth</strong></td>
<td>Invia i caratteri di tabulazione (o MAIUSC + TAB) come input alla destinazione di verifica per verificare che l'interfaccia utente della destinazione non sia eccessivamente complessa o inaccessibile mediante la navigazione da tastiera standard.</td>
</tr>
<tr class="even">
<td><strong>CheckTabbingUia</strong></td>
<td>Invia i caratteri di tabulazione (o MAIUSC + TAB) come input alla destinazione di verifica per confermare che tutti gli elementi attivabili nell'interfaccia utente sono raggiungibili in modo ordinato e logico utilizzando la navigazione da tastiera standard.</td>

</tr>
<tr class="odd">
<td rowspan="5"><strong>Proprietà</strong>$ {Remove} $<br />
</td>
<td><strong>CheckRole</strong></td>
<td>Conferma che ogni elemento attivabile nell'interfaccia utente segnala un ruolo di MSAA logico valido e che il controllo ha un valore come richiesto da tale ruolo.</td>
</tr>
<tr class="even">
<td><strong>CheckState</strong></td>
<td>Conferma che ogni elemento attivabile nell'interfaccia utente segnala uno stato MSAA logico valido.</td>

</tr>
<tr class="odd">
<td><strong>Elaborazioni nomecontrollo</strong></td>
<td>Conferma che ogni elemento attivabile nell'interfaccia utente segnala un nome di MSAA logico valido.</td>

</tr>
<tr class="even">
<td><strong>CheckAccessKeys</strong></td>
<td>Conferma che le chiavi di accesso assegnate agli elementi nella destinazione di verifica sono univoche all'interno della destinazione di verifica.</td>

</tr>
<tr class="odd">
<td><strong>CheckBoundingRect</strong></td>
<td>Conferma che ogni elemento attivabile nell'interfaccia utente dispone di un rettangolo di delimitazione che può essere utilizzato come destinazione per l'hit testing.</td>

</tr>
<tr class="even">
<td rowspan="2"><strong>Albero</strong>$ {Remove} $<br />
</td>
<td><strong>CheckParentChild</strong></td>
<td>Le relazioni padre e figlio nell'albero degli elementi sono coerenti e prevedibili.</td>
</tr>
<tr class="odd">
<td><strong>CheckOrphanChildren</strong></td>
<td>Conferma che ogni elemento attivabile nell'interfaccia utente segnala un padre MSAA valido.</td>

</tr>
<tr class="even">
<td rowspan="6"><strong>Proprietà UIA</strong>$ {Remove} $<br />
</td>
<td><strong>CheckNameUIA</strong></td>
<td>Conferma che ogni elemento attivabile nell'interfaccia utente segnala un nome di UIA logico valido.</td>
</tr>
<tr class="odd">
<td><strong>CheckTreeDepthUIA</strong></td>
<td>Invia i caratteri di tabulazione (o MAIUSC + TAB) come input alla destinazione di verifica per confermare che gli elementi dell'interfaccia utente nell'interfaccia utente della destinazione non sono eccessivamente complessi o inaccessibili tramite la navigazione da tastiera standard.</td>

</tr>
<tr class="even">
<td><strong>CheckStateUIA</strong></td>
<td>Conferma che ogni elemento attivabile nell'interfaccia utente segnala uno stato UIA logico valido.</td>

</tr>
<tr class="odd">
<td><strong>CheckAccessKeysUIA</strong></td>
<td>Conferma che gli elementi di pari livello non hanno lo stesso accesso e/o il tasto di scelta rapida.</td>

</tr>
<tr class="even">
<td><strong>CheckBoundingRectUIA</strong></td>
<td>Conferma che ogni elemento UIA attivabile nell'interfaccia utente dispone di un rettangolo di delimitazione che può essere usato come destinazione per l'hit testing.</td>

</tr>
<tr class="odd">
<td><strong>CheckControlTypeUIA</strong></td>
<td>Conferma che ogni elemento attivabile nell'interfaccia utente segnala un tipo di controllo UIA logico valido.</td>

</tr>
<tr class="even">
<td rowspan="3"><strong>Albero UIA</strong>$ {Remove} $<br />
</td>
<td><strong>CheckNavigateUia</strong></td>
<td>Conferma che il TreeWalker di interfaccia di interfaccia di stato può spostarsi tra gli elementi figlio di un elemento.</td>
</tr>
<tr class="odd">
<td><strong>CheckOrphanChildrenUia</strong></td>
<td>Conferma che ogni elemento attivabile nell'interfaccia utente segnala un elemento padre dell'elemento del controllo dell'associazione valido.</td>

</tr>
<tr class="even">
<td><strong>CheckSiblingsUia</strong></td>
<td>Conferma che gli elementi di pari livello non hanno lo stesso nome: coppie ControlType, né lo stesso AutomationId.</td>

</tr>
<tr class="odd">
<td>$ {ROWSPAN9} $<strong>aria Web VERIFICATIONS</strong>$ {Remove} $<br />
</td>
<td><strong>CheckARIARole</strong></td>
<td>Conferma che tutti gli elementi hanno un ruolo ARIA valido. Il tag HTML associato e il ruolo ARIA sono elementi informativi con ruoli non validi contrassegnati come errori.</td>
</tr>
<tr class="even">
<td><strong>CheckLabel</strong></td>
<td>Conferma che ogni elemento con il ruolo di input, pulsante, immagine o punto di riferimento dispone di un'etichetta.</td>

</tr>
<tr class="odd">
<td><strong>CheckRangeControls</strong></td>
<td>Conferma che i controlli intervallo con dispositivo di scorrimento o indicatore di stato hanno attributi ARIA corretti definiti.</td>

</tr>
<tr class="even">
<td><strong>CheckContainerRole</strong></td>
<td>Conferma che un elemento o almeno uno dei relativi elementi figlio ha definito OnKeyDown/OnKeyPress.</td>

</tr>
<tr class="odd">
<td><strong>CheckLayoutTable</strong></td>
<td>Conferma che un layout di tabella contiene un riepilogo/aria-describedby inclusi.</td>

</tr>
<tr class="even">
<td><strong>CheckGridStructure</strong></td>
<td>Conferma che un elemento non tabella con il ruolo Grid ha una struttura di Grid>Row>GridCell con attributi associati.</td>

</tr>
<tr class="odd">
<td><strong>CheckDataTable</strong></td>
<td>Conferma le proprietà delle tabelle di dati.</td>

</tr>
<tr class="even">
<td><strong>CheckActiveDescendants</strong></td>
<td>Conferma le proprietà degli elementi con un discendente attivo definito.</td>

</tr>
<tr class="odd">
<td><strong>CheckElementsWithClickHandler</strong></td>
<td>Conferma l'indice di tabulazione degli elementi con gestori di clic.</td>

</tr>
<tr class="even">
<td rowspan="3"><strong>Verifiche Web</strong>$ {Remove} $<br />
</td>
<td><strong>CheckHtml (Web)</strong></td>
<td>Conferma varie caratteristiche HTML, ad esempio intestazioni, nomi, frame e titoli.</td>
</tr>
<tr class="odd">
<td><strong>CheckName (Web)</strong></td>
<td>Conferma le caratteristiche del nome, ad esempio la lunghezza, i caratteri non validi e l'inclusione del ruolo.</td>

</tr>
<tr class="even">
<td><strong>CheckRole (Web)</strong></td>
<td>Conferma i ruoli non validi, i ruoli che devono avere valori e/o ruoli non implementati.</td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Verifica dell'accessibilità dell'interfaccia utente](ui-accessibility-checker.md)
</dt> </dl>

 

 




