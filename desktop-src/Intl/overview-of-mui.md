---
description: Questo argomento fornisce una panoramica concettuale della tecnologia MUI (Multilingual User Interface), il supporto della piattaforma che fornisce per l'abilitazione di esperienze utente multilingue e i vantaggi offerti dall'ecosistema Windows.
ms.assetid: ef828da8-61cd-43d9-a5fe-e09a1f8af5c7
title: Panoramica di MUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 674cb5e0fee4e7b8d3990a99f13f981c4a8c5803
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104570854"
---
# <a name="overview-of-mui"></a>Panoramica di MUI

Questo argomento fornisce una panoramica concettuale della tecnologia MUI (Multilingual User Interface), il supporto della piattaforma che fornisce per l'abilitazione di esperienze utente multilingue e i vantaggi offerti dall'ecosistema Windows.

In questa pagina:

-   [Necessità di elaborazione multilingue](#the-need-for-multilingual-computing)
-   [Il ruolo di MUI nell'abilitazione del calcolo multilingue](#the-role-of-mui-in-enabling-multilingual-computing)
-   [Concetti di base di MUI](#core-concepts-of-mui)
-   [Cronologia di MUI in Windows](#history-of-mui-in-windows)
-   [Vantaggi della tecnologia MUI](#benefits-of-mui-technology)

## <a name="the-need-for-multilingual-computing"></a>Necessità di elaborazione multilingue

Per trarre vantaggio dalle opportunità di crescita offerte dai mercati internazionali, le piattaforme e le applicazioni Microsoft supportano più lingue, culture e mercati che mai.

La lingua, le impostazioni cultura e le specifiche del mercato sono ancora estremamente rilevanti per gli utenti internazionali, nonostante le crescenti tendenze di globalizzazione. Il grafico a torta seguente mostra che i relatori non in lingua inglese costituiscono ancora il 91,5% della popolazione mondiale.

![grafico a torta con tre segmenti; quello con etichetta "lingua inglese 91,5%" è notevolmente più grande rispetto alle altre due combinazioni](images/overview-of-mui-fig1.gif)

In tutto il mondo sono presenti 193 paesi e oltre 6.900 linguaggi di vita noti attualmente in uso. L'inglese, nonostante il suo ruolo di linguaggio aziendale, viene parlato solo del 8,5% della popolazione del mondo come prima o secondo linguaggio. Per fornire informazioni Native al 94% della popolazione del mondo, è necessario che queste informazioni siano disponibili nella 347 (circa il 5%). dei linguaggi del mondo con almeno un milione di relatori. Ciò vale soprattutto per quanto le tendenze di globalizzazione hanno accresciuto le aspettative di questi utenti riguardo alla tecnologia e alla sua disponibilità nei propri mercati.

La necessità di localizzare il software in più lingue è aumentata nel corso degli anni e Microsoft offre ora Windows Vista e altri prodotti in più lingue che mai. Questa evoluzione è particolarmente chiara con Microsoft Windows, dal momento che non supporta 30 lingue con Windows 98 a quasi 100 con Windows Vista, come illustrato nel seguente grafico a barre.

![grafico a barre che mostra che il numero di lingue è molto più grande in Windows Vista rispetto a Windows 98 o Windows XP](images/overview-of-mui-fig2.gif)

*Figura 2: numero di lingue supportate dalle versioni di Microsoft Windows*

## <a name="the-role-of-mui-in-enabling-multilingual-computing"></a>Il ruolo di MUI nell'abilitazione del calcolo multilingue

Come illustrato nella sezione precedente, la [globalizzazione](glossary-for-understanding-mui.md) e la [localizzazione](glossary-for-understanding-mui.md) delle applicazioni sono diventati una necessità in un mondo integrato più a livello globale. In particolare, dato che sempre più aziende si trovano a livello globale, internamente o attraverso le loro reti aziendali, la necessità di applicazioni multilingue è in continua crescita. Sono quindi gli ostacoli che attualmente queste società devono affrontare nella distribuzione globale di queste applicazioni.

Per fornire supporto per più lingue per i sistemi operativi Windows, nonché per le applicazioni software create per la piattaforma Windows, sono necessarie nuove strategie che consentono di implementare tutti gli scenari principali con un sovraccarico minimo di progettazione.

La tecnologia MUI è destinata agli sviluppatori e agli ISV che mirano a creare e supportare applicazioni multilingue per la piattaforma Windows. MUI è anche di importanza fondamentale per gli OEM e le aziende, che possono usarlo per distribuire il sistema operativo Windows e aggiungere applicazioni a computer in linguaggi diversi tramite la distribuzione di un'unica immagine.

## <a name="core-concepts-of-mui"></a>Concetti di base di MUI

L'idea fondamentale della tecnologia MUI è [separare l'archiviazione delle risorse localizzabili dal codice sorgente dell'applicazione](mui-fundamental-concepts-explained.md), in modo da poter progettare un'applicazione multilingue come una combinazione di un file binario Core indipendente dalla lingua e un set di file di risorse localizzati specifici del linguaggio.

Una volta che il codice sorgente dell'applicazione viene archiviato separatamente dalle risorse localizzate, diventa semplice [caricare dinamicamente le risorse localizzate appropriate](mui-fundamental-concepts-explained.md) per un determinato contesto dell'applicazione in base a una logica che prende in considerazione le impostazioni a livello di sistema, utente e applicazione per la lingua dell'interfaccia utente.

Questi attributi fondamentali di MUI contribuiscono a semplificare gli scenari aziendali, ad esempio:

-   Un modello di localizzazione migliorato per l'interfaccia utente e il contenuto della guida, tramite la separazione fisica del codice sorgente dell'applicazione e le risorse localizzabili.
-   Trattare le risorse localizzabili come contenuto dinamico e caricarle in base alle impostazioni della lingua dell'interfaccia utente e alle preferenze di fallback. Questo consente scenari come:
    -   Passare da una lingua dell'interfaccia utente a un'altra in fase di esecuzione.
    -   Creazione di immagini di distribuzione singola a livello di area o globale che coprono un set di lingue per OEM e aziende.

## <a name="history-of-mui-in-windows"></a>Cronologia di MUI in Windows

Il livello di supporto disponibile per un'esperienza utente multilingue a livello di sistema operativo Windows e per lo sviluppo di applicazioni multilingue sulla piattaforma Windows si è evoluto nel tempo e nelle diverse versioni di Windows.

Le funzionalità supportate [prima di Windows Vista](evolution-of-mui-support-across-windows-versions.md) erano abbastanza semplici, con immagini di Windows in una sola lingua e un'opzione per l'aggiunta di interfacce utente multilingue in scenari specifici. Non è disponibile alcun supporto per gli sviluppatori per le applicazioni multilingue.

[Con Windows Vista](evolution-of-mui-support-across-windows-versions.md), Microsoft ha realizzato un investimento significativo in MUI e Windows Vista è stato creato da zero su una piattaforma MUI. Sebbene questo rappresenti un importante progresso nella strategia di localizzazione di Windows, poiché si tratta di una chiave fondamentale per Microsoft per fornire Windows in più lingue, è prima di tutto un ottimo vantaggio per gli utenti, gli sviluppatori e i clienti di Windows. Offre diversi vantaggi principali, ad esempio:

-   Sistema operativo indipendente dalla lingua con supporto incorporato per MUI.
-   Creazione di pacchetti, distribuzione e installazione configurabili per supportare scenari multilingue.
-   Distribuzione con un'unica immagine con più lingue.
-   Un modello di manutenzione migliorato in cui il codice eseguibile può essere aggiornato indipendentemente dalle risorse.
-   Supporto per gli sviluppatori per la creazione di applicazioni multilingue.

La tabella seguente fornisce una panoramica dettagliata del supporto della piattaforma Windows per MUI:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Category</th>
<th>Supporto</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Versioni di Windows supportate (solo supporto del sistema operativo)</td>
<td><ul>
<li>Windows 2000 Professional</li>
<li>Famiglia di server Windows 2000</li>
<li>Windows XP Professional</li>
<li>Windows XP Tablet PC Edition</li>
<li>Famiglia Windows Server 2003</li>
<li>Windows XP Embedded</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td>Versioni di Windows supportate (supporto per applicazioni del sistema operativo &)</td>
<td><ul>
<li>Windows Vista</li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td>Versioni di Windows non supportate</td>
<td><ul>
<li>Windows 9x</li>
<li>Windows me</li>
<li>Windows XP Home Edition</li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="benefits-of-mui-technology"></a>Vantaggi della tecnologia MUI

MUI influisca positivamente su più aspetti dell'ecosistema Windows:

-   [Vantaggi per gli sviluppatori](benefits-of-mui-explained.md): molti vantaggi sono offerti agli sviluppatori di applicazioni dalla disponibilità del supporto delle API MUI per creare applicazioni multilingue modellate in base agli stessi principi del supporto multilingue nel sistema operativo Windows di base. Questi vantaggi includono:
    -   Possibilità di fornire un'esperienza di visualizzazione della lingua coerente con i vantaggi offerti dal sistema operativo.
    -   Possibilità di estendere facilmente il supporto del linguaggio per un'applicazione.
    -   La possibilità di gestire e gestire facilmente l'applicazione.
    -   La possibilità di abilitare la distribuzione a immagine singola delle applicazioni da parte degli OEM.
-   [Vantaggi per le aziende](benefits-of-mui-explained.md): il vantaggio principale offerto da MUI per le aziende è la possibilità di implementare, supportare e gestire la stessa immagine multilingue in tutto il mondo con un'unica installazione. Un'altra vittoria significativa è la possibilità di supportare desktop multilingue che offrono un'interazione senza problemi agli utenti con preferenze di lingua diverse.
-   [Vantaggi per gli OEM](benefits-of-mui-explained.md): il vantaggio principale per gli OEM è la singola installazione di immagini abilitata da MUI, con supporto per più linguaggi, che consente una gestione più efficace dell'inventario. Gli OEM traggono vantaggio anche dal supporto MUI per lo sviluppo di applicazioni, in quanto consentono loro di fornire applicazioni a valore aggiunto sulle proprie immagini, sfruttando al contempo l'installazione di una singola immagine, purché queste applicazioni siano abilitate per MUI.

 

 




