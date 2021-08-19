---
title: Appendice A Informazioni di riferimento Interfaccia utente elementi supportati
description: Questa appendice contiene informazioni sugli elementi dell'interfaccia utente forniti dal sistema esposti da Microsoft Active Accessibility in Windows 95, Windows 98, Microsoft Windows NT, Windows 2000, Windows XP e Windows 2000 Server.
ms.assetid: 5d0a81d8-5d36-4c33-bb8c-abcb8b00166e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e434eec9a480f46bb352dbd5b523b8b5c9cde6624c9d94372703d054e945bab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994371"
---
# <a name="appendix-a-supported-user-interface-elements-reference"></a>Appendice A: Informazioni di riferimento Interfaccia utente elementi supportati

Questa appendice contiene informazioni sugli elementi dell'interfaccia utente forniti dal sistema esposti da Microsoft Active Accessibility in Windows 95, Windows 98, Microsoft Windows NT, Windows 2000, Windows XP e Windows 2000 Server. Questo supporto consente alle utilità client di ottenere informazioni sugli elementi dell'interfaccia utente forniti dal sistema nelle applicazioni che non implementano Microsoft Active Accessibility.

Oleacc.dll supporta i controlli definiti in User32.dll, Comctl32.dll e Windows dell'interfaccia utente. In particolare, supporta i tipi seguenti di elementi dell'interfaccia utente (elencati Windows nome della classe).



| Windows classe                   | Tipo di elemento dell'interfaccia utente                                         | Windows Aggiornamenti di Vista                                                                                                                                                                                                |
|--------------------------------------|---------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ListBox                              | Caselle di riepilogo                                              | Nessuno                                                                                                                                                                                                                 |
| Button                               | Pulsanti di scelta, pulsanti di opzione, pulsanti di controllo, caselle di gruppo | I pulsanti di divisione possono avere zero o più elementi figlio.                                                                                                                                                                        |
| Statica                               | Etichette                                                  | Nessuno                                                                                                                                                                                                                 |
| Modifica                                 | Caselle di testo                                              | Nessuno                                                                                                                                                                                                                 |
| ComboBox                             | Caselle combinate, elenchi a discesa                            | Nessuno                                                                                                                                                                                                                 |
| ScrollBar                            | Barre di scorrimento                                             | [**EVENTO \_ OBJECT \_ CONTENTSCROLLED**](event-constants.md) è un nuovo evento per il controllo che dispone di funzionalità di scorrimento, ma non include una barra di scorrimento standard come parte del controllo. |
| \#32768                              | Menu UTENTE                                              | Nessuno                                                                                                                                                                                                                 |
| \#32770                              | Finestre di dialogo UTENTE                                       | Nessuno                                                                                                                                                                                                                 |
| \#32771                              | Finestra ALT+TAB                                          | Disponibile solo in modalità classica.                                                                                                                                                                                      |
| msctls \_ statusbar32                  | Barre di stato                                             | Nessuno                                                                                                                                                                                                                 |
| msctls \_ progress32                   | Barre di stato                                           | Le nuove opzioni di colore per le barre di stato non vengono esposte Microsoft Active Accessibility proprietà Automazione interfaccia utente Microsoft.                                                                                         |
| Tasto di scelta \_ rapida msctls32                     | Controlli dei tasti di scelta rapida                                        | Nessuno                                                                                                                                                                                                                 |
| msctls \_ trackbar32                   | Trackbar, dispositivi di scorrimento                                      | Nessuno                                                                                                                                                                                                                 |
| msctls \_ updown32                     | Controlli up-down o spin                                | Nessuno                                                                                                                                                                                                                 |
| SysAnimate32                         | Controllo Animation                                       | Nessuno                                                                                                                                                                                                                 |
| SysTabControl32                      | Controllo Tab                                             | Nessuno                                                                                                                                                                                                                 |
| SysHeader32                          | Intestazioni della visualizzazione elenco                                       | Nessuno                                                                                                                                                                                                                 |
| SysListView32                        | Controlli visualizzazione elenco                                      | Nessuno                                                                                                                                                                                                                 |
| SysTreeView32                        | Controlli di visualizzazione albero                                      | Nessuno                                                                                                                                                                                                                 |
| SysDateTimePick32 (versioni 5 e 6) | Selezione data e/o ora                                 | La versione 6 di questo controllo in Windows Vista ha [**un'implementazione nativa di IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)                                                                                                           |
| SysIPAddress32                       | Controlli degli indirizzi IP                                     | Nessuno                                                                                                                                                                                                                 |
| Classe \_ tooltips32                    | Le descrizioni comandi                                                | Nessuno                                                                                                                                                                                                                 |
| ToolbarWindow32                      | Barre degli strumenti                                                | Nessuno                                                                                                                                                                                                                 |
| RICHEDIT, RichEdit20A, RichEdit20W   | Campi di testo                                             | Nessuno                                                                                                                                                                                                                 |
| SysMonthCal32 (versioni 5 e 6)     | Calendario mensile                                          | La versione 6 di questo controllo in Windows Vista ha [**un'implementazione nativa di IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)                                                                                                           |



 

Sebbene il supporto per gli elementi dell'interfaccia utente forniti dal sistema sia fornito da Microsoft Active Accessibility in Microsoft Windows NT 4.0 con Service Pack 4, questo supporto è limitato.

Questa appendice elenca le [**proprietà e i metodi IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) supportati Microsoft Active Accessibility per ogni elemento dell'interfaccia utente. Se applicabile, la documentazione elenca anche gli [eventi WinEvent attivati](winevents-infrastructure.md) dall'elemento dell'interfaccia utente e include informazioni aggiuntive sulle proprietà e i metodi supportati. Include anche informazioni sui ruoli oggetto e sui relativi metodi **e proprietà IAccessible** supportati.

Questi dettagli consentono agli sviluppatori client di evitare di effettuare chiamate non necessarie a metodi e proprietà non supportati. Queste informazioni consentono inoltre agli sviluppatori server di conoscere le proprietà e i metodi che i controlli personalizzati devono supportare e quali WinEvent devono attivare i controlli.

Usare le informazioni contenute in questa appendice come guida. È consigliabile usare gli strumenti di Microsoft Active Accessibility per verificare il comportamento previsto per gli elementi dell'interfaccia utente o i ruoli oggetto.

Per altre informazioni, vedere i seguenti argomenti:

-   [Come Active Accessibility espone Interfaccia utente elementi](how-active-accessibility-exposes-user-interface-elements.md)
-   [Interfaccia utente riferimento all'elemento](user-interface-element-reference.md)

 

 




