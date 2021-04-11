---
title: Ascolto degli eventi della barra multifunzione
description: Il Framework della barra multifunzione di Windows usa l'infrastruttura Event Tracing for Windows (ETW) per consentire agli sviluppatori di apprendere il modo in cui gli utenti interagiscono con la barra multifunzione dell'applicazione.
ms.assetid: F29A8E41-C902-410E-BD28-653E078320E9
keywords:
- Barra multifunzione di Windows, eventi
- Barra multifunzione, eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcbfb2c6417c1423cb785b6b80de4396146535c2
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "104339447"
---
# <a name="listening-for-ribbon-events"></a>Ascolto degli eventi della barra multifunzione

Il Framework della barra multifunzione di Windows usa l'infrastruttura [Event Tracing for Windows (ETW)](../etw/event-tracing-portal.md) per consentire agli sviluppatori di apprendere il modo in cui gli utenti interagiscono con la barra multifunzione dell'applicazione.

## <a name="introduction"></a>Introduzione

Il meccanismo degli eventi della barra multifunzione è progettato in modo che il Framework segnali gli eventi dell'interfaccia utente della barra multifunzione all'applicazione, in modo da poter monitorare le attività degli utenti, apprendere i modelli di interazione e valutare le tendenze Queste informazioni possono essere usate per ottimizzare l'esperienza utente per le iterazioni future dell'app della barra multifunzione.

L'utilizzo degli eventi del Framework della barra multifunzione prevede quanto segue:

1.  L'applicazione Ribbon deve registrare un listener di [Event Tracing for Windows (ETW)](../etw/event-tracing-portal.md) per ricevere le notifiche degli eventi della barra multifunzione dal framework della barra multifunzione.
2.  Il Framework della barra multifunzione attiva i callback degli eventi dell'interfaccia utente della barra multifunzione in fase di esecuzione, se l'applicazione ha registrato un listener di [Event Tracing for Windows (ETW)](../etw/event-tracing-portal.md) .

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
<td>Menu applicazione aperto</td>
<td>Verbo evento<br/></td>
</tr>
<tr class="even">
<td>Menu applicazione chiuso</td>
<td>Verbo evento<br/></td>
</tr>
<tr class="odd">
<td>Menu (Regular o Gallery) aperto</td>
<td>ID comando<br/> Nome comando<br/> Verbo evento<br/>
<blockquote>
[!Note]<br />
Gli eventi del menu QAT non sono esposti.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Menu (Regular o Gallery) chiuso</td>
<td>ID comando<br/> Nome comando<br/> Verbo evento<br/>
<blockquote>
[!Note]<br />
Gli eventi del menu QAT non sono esposti.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>Comando</td>
<td>ID comando<br/> Nome comando<br/> Verbo evento<br/> Uno dei percorsi degli eventi seguenti:
<ul>
<li>RIBBON</li>
<li>QUICKACCESSTOOLBAR</li>
<li>APPLICATIONMENU</li>
<li>CONTEXTPOPUP</li>
</ul>
<br/> ID comando padre<br/> Nome del comando padre<br/> Uno dei metodi Invoke seguenti:
<ul>
<li>Clicca</li>
<li>SUGGERIMENTO tasto</li>
<li>TASTIERA</li>
<li>TOCCO</li>
</ul>
<br/>
<blockquote>
[!Note]<br />
Le raccolte di elementi e le caselle combinate includono l'indice dell'elemento selezionato, ma non includono valori stringa e Integer. Gli Spinner non includono il valore integer.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Barra multifunzione ridotta a icona</td>
<td>Verbo evento<br/></td>
</tr>
<tr class="odd">
<td>Barra multifunzione espansa (pulsante di espansione selezionato o tocco aggiunto)</td>
<td>Verbo evento<br/></td>
</tr>
<tr class="even">
<td>Modalità applicazione cambiata</td>
<td>Verbo evento<br/> ID modalità (valore impostato tramite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes"><strong>Semodes</strong></a>)<br/>
<blockquote>
[!Note]<br />
L'applicazione è responsabile della decompressione di questo Integer per determinare le modalità impostate.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>Descrizione comando visualizzata</td>
<td>Verbo evento<br/> ID comando padre<br/> Nome del comando padre<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guide per gli sviluppatori di Windows Ribbon Framework](windowsribbon-guides-entry.md)
</dt> <dt>

[Dichiarazione di comandi e controlli con markup della barra multifunzione](./windowsribbon-schema.md)
</dt> <dt>

[Linee guida sull'esperienza utente della barra multifunzione](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[Processo di progettazione della barra multifunzione](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

