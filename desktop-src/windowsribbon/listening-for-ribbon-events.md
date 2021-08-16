---
title: Ascolto di eventi della barra multifunzione
description: Il framework Windows ribbon usa l'infrastruttura ETW (Event Tracing for Windows) per consentire agli sviluppatori di apprendere come gli utenti interagiscono con la barra multifunzione dell'applicazione.
ms.assetid: F29A8E41-C902-410E-BD28-653E078320E9
keywords:
- Windows Barra multifunzione, eventi
- Barra multifunzione, eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9519553a40cd613085949d4650c2689e817f387e47e9ab4380b629464e90d2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118202971"
---
# <a name="listening-for-ribbon-events"></a>Ascolto di eventi della barra multifunzione

Il framework Windows barra multifunzione usa l'infrastruttura [ETW (Event Tracing for Windows)](../etw/event-tracing-portal.md) per consentire agli sviluppatori di apprendere come gli utenti interagiscono con la barra multifunzione dell'applicazione.

## <a name="introduction"></a>Introduzione

Il meccanismo degli eventi del framework della barra multifunzione è progettato in modo che il framework segnala gli eventi dell'interfaccia utente della barra multifunzione all'applicazione in modo da poter monitorare l'attività dell'utente, apprendere i modelli di interazione e valutare le tendenze di utilizzo. Queste informazioni possono essere usate per perfezionare l'esperienza utente per le iterazioni future dell'app della barra multifunzione.

L'uso degli eventi del framework della barra multifunzione implica quanto segue:

1.  L'applicazione della barra multifunzione deve registrare un listener [ETW (Event Tracing for Windows)](../etw/event-tracing-portal.md) per ricevere notifiche degli eventi della barra multifunzione dal framework della barra multifunzione.
2.  Il framework della barra multifunzione attiva i callback degli eventi dell'interfaccia utente della barra multifunzione in fase di esecuzione, se l'applicazione ha registrato un listener [ETW (Event Tracing for Windows).](../etw/event-tracing-portal.md)

## <a name="supported-events"></a>Eventi supportati

Gli eventi esposti alle applicazioni della barra multifunzione sono descritti nella tabella seguente. 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Evento</th>
<th>Report eventi</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Scheda attivata</td>
<td>ID comando<br/> Nome comando<br/> Verbo evento<br/></td>
</tr>
<tr class="even">
<td>Scheda contestuale attivata</td>
<td>ID comando<br/> Nome comando<br/> Verbo evento<br/></td>
</tr>
<tr class="odd">
<td>Menu dell'applicazione aperto</td>
<td>Verbo evento<br/></td>
</tr>
<tr class="even">
<td>Menu dell'applicazione chiuso</td>
<td>Verbo evento<br/></td>
</tr>
<tr class="odd">
<td>Menu (normale o raccolta) aperto</td>
<td>ID comando<br/> Nome comando<br/> Verbo evento<br/>
<blockquote>
[!Note]<br />
Gli eventi di menu di Domande e risposte non sono esposti.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Menu (normale o raccolta) chiuso</td>
<td>ID comando<br/> Nome comando<br/> Verbo evento<br/>
<blockquote>
[!Note]<br />
Gli eventi di menu di Domande e risposte non sono esposti.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>Comando</td>
<td>ID comando<br/> Nome comando<br/> Verbo evento<br/> Uno dei percorsi degli eventi seguenti:
<ul>
<li>Nastro</li>
<li>QUICKACCESSTOOLBAR</li>
<li>APPLICATIONMENU</li>
<li>CONTEXTPOPUP</li>
</ul>
<br/> ID comando padre<br/> Nome comando padre<br/> Uno dei metodi invoke seguenti:
<ul>
<li>Fare clic su</li>
<li>Keytip</li>
<li>Tastiera</li>
<li>tocco</li>
</ul>
<br/>
<blockquote>
[!Note]<br />
Le raccolte di elementi e le caselle combinate includono l'indice dell'elemento selezionato, ma non includono valori stringa e integer. Le frecce di selezione non includono il valore intero.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Barra multifunzione ridotta a icona</td>
<td>Verbo evento<br/></td>
</tr>
<tr class="odd">
<td>Barra multifunzione espansa (pulsante di espansione su cui è stato fatto clic o tocco aggiunto)</td>
<td>Verbo evento<br/></td>
</tr>
<tr class="even">
<td>Modalità applicazione cambiata</td>
<td>Verbo evento<br/> ID modalità (valore impostato tramite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes"><strong>SetModes)</strong></a><br/>
<blockquote>
[!Note]<br />
L'applicazione è responsabile della decompressione di questo numero intero per determinare quali modalità sono state impostate.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>Descrizione comando visualizzata</td>
<td>Verbo evento<br/> ID comando padre<br/> Nome comando padre<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Guide per gli sviluppatori del framework della barra multifunzione](windowsribbon-guides-entry.md)
</dt> <dt>

[Dichiarazione di comandi e controlli con markup della barra multifunzione](./windowsribbon-schema.md)
</dt> <dt>

[Linee guida per l'esperienza utente della barra multifunzione](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[Processo di progettazione della barra multifunzione](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

