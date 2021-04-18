---
title: Appendice un riferimento A elementi dell'interfaccia utente supportati
description: Questa appendice contiene informazioni sugli elementi dell'interfaccia utente forniti dal sistema esposti da Microsoft Active Accessibility in Windows 95, Windows 98, Microsoft Windows NT, Windows 2000, Windows XP e Windows 2000 Server.
ms.assetid: 5d0a81d8-5d36-4c33-bb8c-abcb8b00166e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f75cd4251ed7d75d9aa6a2d83387a51a8b157e9
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "106299340"
---
# <a name="appendix-a-supported-user-interface-elements-reference"></a>Appendice A: informazioni di riferimento sugli elementi dell'interfaccia utente supportati

Questa appendice contiene informazioni sugli elementi dell'interfaccia utente forniti dal sistema esposti da Microsoft Active Accessibility in Windows 95, Windows 98, Microsoft Windows NT, Windows 2000, Windows XP e Windows 2000 Server. Questo supporto consente alle utilità client di ottenere informazioni sugli elementi dell'interfaccia utente forniti dal sistema nelle applicazioni che non implementano Microsoft Active Accessibility.

Oleacc.dll supporta i controlli definiti negli elementi User32.dll, Comctl32.dll e dell'interfaccia utente di Windows. In particolare, supporta i seguenti tipi di elementi dell'interfaccia utente (elencati in base al nome della classe di Windows).



| Nome classe Windows                   | Tipo di elemento dell'interfaccia utente                                         | Aggiornamenti di Windows Vista                                                                                                                                                                                                |
|--------------------------------------|---------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ListBox                              | Caselle di riepilogo                                              | nessuno                                                                                                                                                                                                                 |
| Pulsante                               | Pulsanti di comando, pulsanti di opzione, pulsanti di controllo, caselle di gruppo | I pulsanti dividi possono avere zero o più elementi figlio.                                                                                                                                                                        |
| Static                               | Etichette                                                  | nessuno                                                                                                                                                                                                                 |
| Modifica                                 | Caselle di testo                                              | nessuno                                                                                                                                                                                                                 |
| ComboBox                             | Caselle combinate, elenchi a discesa                            | nessuno                                                                                                                                                                                                                 |
| ScrollBar                            | Barre di scorrimento                                             | [**Evento \_ L'oggetto \_ CONTENTSCROLLED**](event-constants.md) è un nuovo evento per il controllo con funzionalità di scorrimento senza includere una barra di scorrimento standard come parte del controllo. |
| \#32768                              | Menu utente                                              | nessuno                                                                                                                                                                                                                 |
| \#32770                              | Finestre di dialogo utente                                       | nessuno                                                                                                                                                                                                                 |
| \#32771                              | Finestra Alt-Tab                                          | Disponibile solo in modalità classica.                                                                                                                                                                                      |
| \_statusbar32 msctls                  | Barre di stato                                             | nessuno                                                                                                                                                                                                                 |
| \_progress32 msctls                   | Indicatori di stato                                           | Le nuove opzioni relative ai colori per le barre di stato non sono esposte da Microsoft Active Accessibility o da proprietà di automazione interfaccia utente Microsoft                                                                                         |
| \_hotkey32 msctls                     | Controlli tasto di scelta                                        | nessuno                                                                                                                                                                                                                 |
| \_trackbar32 msctls                   | TrackBar, dispositivi di scorrimento                                      | nessuno                                                                                                                                                                                                                 |
| \_updown32 msctls                     | Controlli di scorrimento o di selezione                                | nessuno                                                                                                                                                                                                                 |
| SysAnimate32                         | Controllo Animation                                       | nessuno                                                                                                                                                                                                                 |
| SysTabControl32                      | Controllo Tab                                             | nessuno                                                                                                                                                                                                                 |
| SysHeader32                          | Intestazioni visualizzazione elenco                                       | nessuno                                                                                                                                                                                                                 |
| SysListView32                        | Controlli visualizzazione elenco                                      | nessuno                                                                                                                                                                                                                 |
| SysTreeView32                        | Controlli di visualizzazione albero                                      | nessuno                                                                                                                                                                                                                 |
| SysDateTimePick32 (versioni 5 e 6) | Selezione data e ora                                 | La versione 6 di questo controllo in Windows Vista dispone di un'implementazione di [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) nativa.                                                                                                           |
| SysIPAddress32                       | Controlli degli indirizzi IP                                     | nessuno                                                                                                                                                                                                                 |
| descrizioni comandi \_ class32                    | Descrizioni comandi                                                | nessuno                                                                                                                                                                                                                 |
| ToolbarWindow32                      | Barre degli strumenti                                                | nessuno                                                                                                                                                                                                                 |
| RichEdit, RichEdit20A, RichEdit20W   | Campi di testo                                             | nessuno                                                                                                                                                                                                                 |
| SysMonthCal32 (versioni 5 e 6)     | Calendario mensile                                          | La versione 6 di questo controllo in Windows Vista dispone di un'implementazione di [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) nativa.                                                                                                           |



 

Sebbene il supporto per gli elementi dell'interfaccia utente fornita dal sistema venga fornito da Microsoft Active Accessibility in Microsoft Windows NT 4,0 con Service Pack 4, questo supporto è limitato.

In questa appendice sono elencate le proprietà e i metodi di [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) supportati da Microsoft Active Accessibility per ogni elemento dell'interfaccia utente. Laddove applicabile, la documentazione elenca anche il [winEvents](winevents-infrastructure.md) che l'elemento dell'interfaccia utente attiva e include informazioni aggiuntive sulle proprietà e i metodi supportati. Sono inoltre incluse informazioni sui ruoli oggetto e i relativi metodi e proprietà **IAccessible** supportati.

Questi dettagli possono aiutare gli sviluppatori client a evitare di effettuare chiamate non necessarie a metodi e proprietà non supportati. Queste informazioni consentono inoltre agli sviluppatori del server di individuare le proprietà e i metodi che i controlli personalizzati devono supportare e quali WinEvents devono essere attivati dai relativi controlli.

Utilizzare le informazioni contenute in questa appendice come guida. È consigliabile utilizzare gli strumenti di Microsoft Active Accessibility per verificare il comportamento previsto per gli elementi dell'interfaccia utente o i ruoli degli oggetti.

Per altre informazioni, vedere i seguenti argomenti:

-   [Come Active Accessibility espone gli elementi dell'interfaccia utente](how-active-accessibility-exposes-user-interface-elements.md)
-   [Riferimento all'elemento dell'interfaccia utente](user-interface-element-reference.md)

 

 




