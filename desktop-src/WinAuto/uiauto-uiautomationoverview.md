---
title: Cenni preliminari su automazione interfaccia utente
description: Automazione interfaccia utente Microsoft è un Framework di accessibilità per Windows.
ms.assetid: 99610542-761c-432d-a4ac-4cd3812577a8
keywords:
- Automazione interfaccia utente, informazioni
- Automazione interfaccia utente, accessibilità
- Automazione interfaccia utente, componenti
- Automazione interfaccia utente, API provider
- Automazione interfaccia utente, API client
- Automazione interfaccia utente, file di intestazione
- Automazione interfaccia utente, modello
- components
- accessibilità
- API provider
- API client
- file di intestazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20ea29b0abd4c6ed791ae3195f36a0f8184c8596
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/11/2020
ms.locfileid: "104398519"
---
# <a name="ui-automation-overview"></a>Cenni preliminari su automazione interfaccia utente

Automazione interfaccia utente Microsoft è un Framework di accessibilità per Windows. Consente l'accesso a livello di codice alla maggior parte degli elementi dell'interfaccia utente sul desktop. Consente ai prodotti di Assistive Technology, quali utilità per la lettura dello schermo, di fornire informazioni sull'interfaccia utente agli utenti finali e di modificare l'interfaccia utente per mezzo di input standard. Automazione interfaccia utente consente inoltre l'interazione degli script di test automatizzati con l'interfaccia utente.

Automazione interfaccia utente era disponibile per la prima volta in Windows XP come parte del Framework Microsoft .NET. Anche se in quel momento è stata pubblicata anche un'API C++ non gestita, l'utilità delle funzioni client era limitata a causa di problemi di interoperabilità. Per Windows 7, l'API è stata riscritta nell'Component Object Model (COM).

> [!Note]  
> Sebbene le funzioni della libreria introdotte nella versione precedente dell'automazione dell'interfaccia utente siano ancora documentate, non devono essere utilizzate nelle nuove applicazioni.

 

Le applicazioni client di automazione interfaccia utente possono essere scritte con la garanzia che funzioneranno su più framework di controllo di Microsoft Windows. Il nucleo di automazione interfaccia utente maschera le eventuali differenze nei framework sottostanti le varie parti dell'interfaccia utente. Ad esempio, la proprietà **Content** di un pulsante Windows Presentation Foundation (WPF), la proprietà **Caption** di un pulsante Microsoft Win32 e la proprietà **ALT** di un'immagine HTML sono tutte mappate a una singola proprietà, **Name**, nella visualizzazione di automazione interfaccia utente.

Automazione interfaccia utente offre funzionalità complete nei sistemi operativi Windows XP, Windows Server 2003 e versioni successive.

I provider di automazione interfaccia utente sono componenti che implementano il supporto di automazione interfaccia utente sui controlli e offrono supporto per le applicazioni client Microsoft Active Accessibility, tramite un servizio di bridging incorporato.

> [!Note]  
> Automazione interfaccia utente non Abilita la comunicazione tra processi avviati da utenti diversi tramite il comando **Esegui come** .

 

In questo argomento sono contenute le sezioni seguenti.

-   [Componenti di automazione interfaccia utente](#ui-automation-components)
-   [File di intestazione di automazione interfaccia utente](#ui-automation-header-files)
-   [Modello di automazione interfaccia utente](#ui-automation-model)
-   [Argomenti correlati](#related-topics)

## <a name="ui-automation-components"></a>Componenti di automazione interfaccia utente

Automazione interfaccia utente dispone di quattro componenti principali, come illustrato nella tabella seguente.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Componente</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>API provider</td>
<td>Set di interfacce COM implementate dai provider di automazione interfaccia utente. I provider di automazione interfaccia utente sono oggetti che forniscono informazioni sugli elementi dell'interfaccia utente e rispondono a input a livello di codice.</td>
</tr>
<tr class="even">
<td>API client</td>
<td>Set di interfacce COM che consentono alle applicazioni client di ottenere informazioni sull'interfaccia utente e di inviare input ai controlli.
<blockquote>
[!Note]<br />
Le funzioni descritte in <a href="uiauto-entry-cpfunctions.md">funzioni del pattern di controllo deprecate</a> e <a href="uiauto-entry-uianodefunctions.md">funzioni di nodo deprecate</a> sono deprecate. Al contrario, le applicazioni client devono usare le interfacce COM di automazione interfaccia utente descritte nelle <a href="uiauto-entry-uiautoclientinterfaces.md">interfacce degli elementi di automazione interfaccia utente per i client</a>.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>UIAutomationCore.dll</td>
<td>La libreria di runtime, talvolta denominata Core di automazione interfaccia utente, che gestisce la comunicazione tra provider e client.</td>
</tr>
<tr class="even">
<td>Oleacc.dll</td>
<td>La libreria di runtime per Microsoft Active Accessibility e gli oggetti proxy. La libreria fornisce anche oggetti proxy usati da Microsoft Microsoft Active Accessibility al proxy di automazione interfaccia utente per supportare i controlli Win32.</td>
</tr>
</tbody>
</table>



 

Esistono due modi per usare l'automazione dell'interfaccia utente: per creare il supporto per i controlli personalizzati tramite l'API del provider e per creare applicazioni client che usano il core di automazione interfaccia utente per comunicare e recuperare informazioni sugli elementi dell'interfaccia utente. In base allo stato attivo, è necessario fare riferimento a parti diverse della documentazione. Se è necessario creare supporto per i controlli personalizzati, vedere [la guida per programmatori del provider di automazione interfaccia utente](uiauto-providerportal.md). Se è necessario comunicare con o recuperare informazioni sugli elementi dell'interfaccia utente, vedere [Guida per programmatori client di automazione interfaccia utente](uiauto-clientportal.md).

## <a name="ui-automation-header-files"></a>File di intestazione di automazione interfaccia utente

L'API di automazione interfaccia utente è definita in diversi file di intestazione C/C++ inclusi in Windows Software Development Kit (SDK). I file di intestazione di automazione interfaccia utente sono descritti nella tabella seguente:



| File di intestazione           | Descrizione                                                                                                                                                                                                                                                                      |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| UIAutomationClient. h  | Definisce le interfacce e gli elementi di programmazione correlati utilizzati dai client di automazione interfaccia utente.                                                                                                                                                                                           |
| UIAutomationCore. h    | Definisce le interfacce e gli elementi di programmazione correlati utilizzati dai provider di automazione interfaccia utente.                                                                                                                                                                                         |
| UIAutomationCoreApi. h | Definisce le costanti generali, i GUID, i tipi di dati e le strutture usati dai provider e dai client di automazione interfaccia utente. Contiene inoltre le definizioni per le funzioni deprecate node e pattern di controllo.                                                                                    |
| UIAutomation. h        | Include tutti gli altri file di intestazione di automazione interfaccia utente. Poiché la maggior parte delle applicazioni di automazione interfaccia utente richiede elementi di tutti i file di intestazione di automazione interfaccia utente, è preferibile includere UIAutomation. h nei progetti dell'applicazione di automazione interfaccia utente anziché includere ogni singolo file. |



 

Se si sviluppa un'applicazione che usa l'API di automazione interfaccia utente, è necessario includere UIAutomation. h nel progetto. Se l'applicazione supporta Microsoft Active Accessibility, includere il file di intestazione oleacc. h. Anche le applicazioni di automazione interfaccia utente che usano GUID richiedono il file di intestazione INITGUID. h. Se necessario, è necessario includere Initguid. h prima di UIAutomation. h.

## <a name="ui-automation-model"></a>Modello di automazione interfaccia utente

Automazione interfaccia utente espone ogni elemento dell'interfaccia utente alle applicazioni client come oggetto rappresentato dall'interfaccia [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) . Gli elementi sono contenuti in una struttura ad albero, con il desktop come elemento radice. I client possono filtrare la visualizzazione non elaborata della struttura ad albero come visualizzazione controlli o visualizzazione contenuto. Queste visualizzazioni standard della struttura possono essere facilmente visualizzate usando l'applicazione di [ispezione](inspect-objects.md) inclusa nel Windows SDK. Le applicazioni possono inoltre creare visualizzazioni personalizzate.

Un elemento di automazione interfaccia utente espone le proprietà del controllo o dell'elemento dell'interfaccia utente che rappresenta. Una di queste proprietà è il tipo di controllo, che definisce l'aspetto e la funzionalità di base del controllo o dell'elemento dell'interfaccia utente come un'unica entità riconoscibile, ad esempio un pulsante o una casella di controllo. Per altre informazioni sui tipi di controllo, vedere [UI Automation Control types Overview](uiauto-controltypesoverview.md).

Inoltre, un elemento di automazione interfaccia utente espone uno o più pattern di controllo. Un pattern di controllo fornisce un set di proprietà specifiche di un particolare tipo di controllo. Un pattern di controllo espone anche metodi che consentono alle applicazioni client di ottenere altre informazioni sull'elemento e di fornire input all'elemento. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).

> [!Note]  
> Non esiste una corrispondenza uno-a-uno tra tipi di controllo e pattern di controllo. Un pattern di controllo può essere supportato da più tipi di controllo e un controllo può supportare più pattern di controllo, ognuno dei quali espone aspetti diversi del comportamento. Ad esempio, una casella combinata dispone di almeno due pattern di controllo: uno che rappresenta la possibilità di espansione e compressione e un altro che rappresenta il meccanismo di selezione. Tuttavia, un controllo può presentare un solo tipo di controllo.

 

Automazione interfaccia utente fornisce informazioni alle applicazioni client tramite gli eventi. A differenza di WinEvents, gli eventi di automazione interfaccia utente non sono basati su un meccanismo di trasmissione. I client di automazione interfaccia utente si registrano per le notifiche di eventi specifici e possono richiedere che le proprietà specifiche e le informazioni sui pattern di controllo vengano passate ai gestori eventi. Inoltre, un evento di automazione interfaccia utente contiene un riferimento all'elemento che lo ha generato. I provider possono migliorare le prestazioni generando eventi in modo selettivo, a seconda dei client in ascolto. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Cenni preliminari sugli eventi di automazione interfaccia utente](uiauto-eventsoverview.md)
</dt> </dl>

 

 





