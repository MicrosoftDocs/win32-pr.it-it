---
description: Questo argomento offre una panoramica concettuale della tecnologia interfaccia utente multilingue (MUI), del supporto della piattaforma che offre per abilitare esperienze utente multilingue e dei vantaggi offerti all'ecosistema Windows globale.
ms.assetid: ef828da8-61cd-43d9-a5fe-e09a1f8af5c7
title: Panoramica di MUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42e4e92c9103b27b35be427a74174c644a285266
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625777"
---
# <a name="overview-of-mui"></a>Panoramica di MUI

Questo argomento offre una panoramica concettuale della tecnologia interfaccia utente multilingue (MUI), del supporto della piattaforma che offre per abilitare esperienze utente multilingue e dei vantaggi offerti all'ecosistema Windows globale.

In questa pagina:

-   [La necessità di un'elaborazione multilingue](#the-need-for-multilingual-computing)
-   [Ruolo di MUI nell'abilitazione del calcolo multilingue](#the-role-of-mui-in-enabling-multilingual-computing)
-   [Concetti di base di MUI](#core-concepts-of-mui)
-   [Cronologia di MUI in Windows](#history-of-mui-in-windows)
-   [Vantaggi della tecnologia MUI](#benefits-of-mui-technology)

## <a name="the-need-for-multilingual-computing"></a>La necessità di un'elaborazione multilingue

Per trarre vantaggio dalle opportunità di crescita offerte dai mercati internazionali, le piattaforme e le applicazioni Microsoft supportano più lingue, culture e mercati che mai.

Le lingue, le impostazioni cultura e le specifiche del mercato sono ancora estremamente rilevanti per gli utenti internazionali, nonostante l'aumento delle tendenze di globalizzazione. Il grafico a torta seguente mostra che i parlanti non inglesi costituiscono ancora il 91,5% della popolazione mondiale.

![grafico a torta con tre segmenti; quello con etichetta "parlanti non inglesi 91,5%" è notevolmente più grande degli altri due combinati](images/overview-of-mui-fig1.gif)

In tutto il mondo sono attualmente in uso 193 paesi e oltre 6.900 lingue viventi note. L'inglese, nonostante il ruolo di lingua aziendale del mondo, è parlato solo dall'8,5% della popolazione mondiale come prima o seconda lingua. Per fornire informazioni native al 94% della popolazione mondiale, queste informazioni devono essere disponibili nelle 347 (circa il 5%) delle lingue del mondo con almeno un milione di parlanti. Questo vale soprattutto perché le tendenze di globalizzazione hanno aumentato le aspettative di questi utenti in merito alla tecnologia e alla disponibilità nei propri mercati.

La necessità di localizzare il software in più lingue è aumentata nel corso degli anni e Microsoft offre ora Windows Vista e altri prodotti in più lingue che mai. Questa evoluzione è particolarmente chiara con Microsoft Windows, perché è passata dal supporto di 30 lingue con Windows 98 a quasi 100 con Windows Vista, come illustrato nel grafico a barre seguente.

![Grafico a barre che mostra che il numero di lingue è molto più grande in Windows Vista rispetto a Windows 98 o Windows XP](images/overview-of-mui-fig2.gif)

*Figura 2: Numero di lingue supportate da Microsoft Windows versioni*

## <a name="the-role-of-mui-in-enabling-multilingual-computing"></a>Ruolo di MUI nell'abilitazione del calcolo multilingue

Come illustrato nella sezione precedente, [](glossary-for-understanding-mui.md) la [globalizzazione](glossary-for-understanding-mui.md) e la localizzazione delle applicazioni sono diventate una necessità in un mondo più integrato a livello globale. In particolare, poiché sempre più aziende stanno passando a livello globale, internamente o tramite le reti aziendali, la necessità di applicazioni multilingue sta aumentando notevolmente. Sono quindi gli ostacoli che queste aziende devono affrontare attualmente nella distribuzione di queste applicazioni a livello globale.

Per offrire il supporto per più linguaggi per i sistemi operativi Windows, nonché per le applicazioni software create per la piattaforma Windows, sono necessarie nuove strategie che consentono l'implementazione di tutti gli scenari principali con un sovraccarico di progettazione minimo.

La tecnologia MUI è destinata agli sviluppatori e agli ISV che mirano a compilare e supportare applicazioni multilingue per la Windows piattaforma. MUI è anche di importanza fondamentale per gli OEM e le aziende, che possono sfruttarlo per distribuire il sistema operativo Windows e aggiungere applicazioni a computer in lingue diverse tramite la distribuzione di singole immagini.

## <a name="core-concepts-of-mui"></a>Concetti di base di MUI

L'idea fondamentale alla [](mui-fundamental-concepts-explained.md)base di MUI è separare l'archiviazione delle risorse localizzabili dal codice sorgente dell'applicazione, in modo da poter creare qualsiasi applicazione multilingue come combinazione di un file binario core indipendente dalla lingua e di un set di file di risorse localizzati specifici della lingua.

Dopo aver archiviato separatamente il codice sorgente [](mui-fundamental-concepts-explained.md) dell'applicazione dalle risorse localizzate, diventa facile caricare dinamicamente le risorse localizzate appropriate per un determinato contesto dell'applicazione in base a una logica che tiene conto delle impostazioni a livello di sistema, utente e applicazione per la lingua dell'interfaccia utente.

Questi attributi fondamentali di MUI facilitano gli scenari aziendali, ad esempio:

-   Un modello di localizzazione migliorato per l'interfaccia utente e il contenuto della Guida, tramite la separazione fisica del codice sorgente dell'applicazione e delle risorse localizzabili.
-   Trattando le risorse localizzabili come contenuto dinamico e caricandole in base alle impostazioni della lingua dell'interfaccia utente e alle preferenze di fallback. In questo modo si abilitano scenari come:
    -   Passaggio da una lingua dell'interfaccia utente a un'altra in fase di esecuzione.
    -   Creazione di immagini di distribuzione singola a livello di regione o in tutto il mondo che coprono un set di lingue per OEM e aziende.

## <a name="history-of-mui-in-windows"></a>Cronologia di MUI in Windows

Il livello di supporto disponibile per un'esperienza utente multilingue a livello di sistema operativo Windows e per lo sviluppo di applicazioni multilingue nella piattaforma Windows si è evoluto nel tempo e nelle diverse versioni di Windows.

La funzionalità supportata prima [di Windows Vista](evolution-of-mui-support-across-windows-versions.md) era piuttosto semplice, con immagini Windows a linguaggio singolo e un'opzione per aggiungere interfaccia utente multilingue Pack in scenari specifici. Non era disponibile alcun supporto per gli sviluppatori per le applicazioni multilingue.

[Con Windows Vista,](evolution-of-mui-support-across-windows-versions.md)Microsoft ha effettuato un investimento significativo in MUI e Windows Vista è stato creato da zero su una piattaforma MUI. Anche se questo rappresenta un importante passo avanti nella strategia di localizzazione di Windows, poiché è un importante strumento per consentire a Microsoft di fornire Windows in più lingue che mai, è prima di tutto un grande passo avanti per utenti, sviluppatori e clienti di Windows. Offre diversi vantaggi principali, ad esempio:

-   Sistema operativo indipendente dalla lingua con supporto incorporato per MUI.
-   Creazione di pacchetti, distribuzione e installazione configurabili per supportare scenari multilingue.
-   Distribuzione a immagine singola con più lingue.
-   Un modello di manutenzione migliorato in cui il codice eseguibile può essere aggiornato indipendentemente dalle risorse.
-   Supporto per gli sviluppatori per la creazione di applicazioni multilingue.

La tabella seguente offre una panoramica dettagliata del supporto Windows piattaforma per MUI:

<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Category</th>
<th>Supporto</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Versioni Windows supportate (solo supporto del sistema operativo)</td>
<td><ul>
<li>Windows 2000 Professional</li>
<li>Windows famiglia di server 2000</li>
<li>Windows XP Professional</li>
<li>Windows XP Tablet PC Edition</li>
<li>Windows Famiglia Server 2003</li>
<li>Windows XP Embedded</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td>Versioni Windows supportate (supporto delle applicazioni & sistema operativo)</td>
<td><ul>
<li>Windows Vista</li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td>Versioni di Windows non supportate</td>
<td><ul>
<li>Windows 9x</li>
<li>Windows Me</li>
<li>Windows XP Home Edition</li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="benefits-of-mui-technology"></a>Vantaggi della tecnologia MUI

MUI influisce in modo positivo su più aspetti dell'ecosistema Windows:

-   Vantaggi [per](benefits-of-mui-explained.md)gli sviluppatori: numerosi vantaggi sono offerti agli sviluppatori di applicazioni dalla disponibilità del supporto api MUI per creare applicazioni multilingue modellate sugli stessi principi del supporto multilingue nel sistema operativo Windows core. Questi vantaggi includono:
    -   La possibilità di offrire un'esperienza di lingua di visualizzazione coerente con ciò che offre il sistema operativo stesso.
    -   Possibilità di estendere facilmente il supporto linguistico per un'applicazione.
    -   Possibilità di gestire e gestire facilmente l'applicazione.
    -   Possibilità di abilitare la distribuzione di applicazioni a immagine singola da parte degli OEM.
-   [Vantaggi per le aziende:](benefits-of-mui-explained.md)il vantaggio principale che MUI offre alle aziende è la possibilità di implementare, supportare e mantenere la stessa immagine multilingue in tutto il mondo con una singola installazione. Un'altra vantaggia significativa è la possibilità di supportare desktop multilingue che offrono un'interazione facile con gli utenti con preferenze linguistiche diverse.
-   [Vantaggi per gli OEM:](benefits-of-mui-explained.md)il vantaggio principale per gli OEM è l'installazione a immagine singola abilitata da MUI, con il supporto per più lingue, che consente una gestione più efficace dell'inventario. Gli OEM traggono vantaggio anche dal supporto MUI per lo sviluppo di applicazioni, in quanto consentono loro di fornire applicazioni a valore aggiunto sulle immagini, traendo vantaggio dall'installazione di una singola immagine, purché queste applicazioni siano abilitate per MUI.

 

 




