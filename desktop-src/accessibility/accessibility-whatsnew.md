---
description: Vengono descritte le ultime novità e gli aggiornamenti di funzionalità, strumenti, documentazione ed esempi di accessibilità di Windows.
title: Novità di Windows Accessibility per sviluppatori
ms.topic: article
ms.date: 04/18/2019
ms.openlocfilehash: 44d8c453b09bc73e71006e132199c18b275860af
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483884"
---
# <a name="new-windows-accessibility-features-tools-documentation-and-samples-for-developers"></a>Nuove funzionalità di accessibilità di Windows, strumenti, documentazione ed esempi per gli sviluppatori

La piattaforma Windows viene costantemente aggiornata con nuove funzionalità di accessibilità e automazione per gli sviluppatori.

[Installare gli strumenti e l'SDK](https://developer.microsoft.com/windows/downloads/#_blank) in Windows 10. si è pronti per creare una nuova app di Windows universale o per esplorare il modo in cui è possibile usare il codice dell'app esistente in Windows.

Per ulteriori informazioni sugli strumenti più recenti disponibili per il test dell'implementazione dell'accessibilità delle applicazioni Windows e Web, vedere [test per l'accessibilità](accessibility-testwithuia.md).

## <a name="whats-new-for-windows-10-may-2019-update-version-1903"></a>Novità di Windows 10-aggiornamento 2019 maggio (versione 1903)

Le funzionalità, gli strumenti, le linee guida per gli sviluppatori, gli esempi e i video seguenti sono stati resi disponibili per l' [aggiornamento 2019 di Windows 10](https://blogs.windows.com/windowsexperience/2019/04/08/releasing-the-may-2019-update-to-the-release-preview-ring/#oTrOrMWFFgWJuCqO.97).

| Versione | Piattaforma | Funzionalità | Descrizione | Collegamento |
| --- | --- | --- | --- | --- |
| 1903 | Win32 | Automazione interfaccia utente supporta IAccessible2 | I client di automazione interfaccia utente possono ora accedere facilmente alle informazioni dai provider IAccessible2, ad esempio il browser Chrome. | n/d |
| 1903 | Piattaforma UWP | Visibilità della barra di scorrimento  | Barre di scorrimento nascoste automaticamente quando non si interagisce con. | [Proprietà UISettings. AutoHideScrollBars](/uwp/api/windows.ui.viewmanagement.uisettings.autohidescrollbars) |
| 1903 | Win32 | Automazione interfaccia utente supporta markup strutturato | È previsto, ma non limitato, l'analisi MathML. | n/d |

## <a name="whats-new-for-windows-10-october-2018-update-version-1809"></a>Novità per l'aggiornamento di Windows 10 ottobre 2018 (versione 1809)

Le funzionalità, gli strumenti, le linee guida per gli sviluppatori, gli esempi e i video seguenti sono stati resi disponibili per l' [aggiornamento di Windows 10 ottobre 2018](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/#R6DJStjqlIkK34BT.97).

| Versione | Piattaforma | Funzionalità | Descrizione | Collegamento |
| --- | --- | --- | --- | --- |
| 1809 | Win32 | Automazione interfaccia utente supporta gli eventi di modifica posizione testo attivo | I provider di automazione interfaccia utente possono impostare in modo esplicito una posizione iniziale all'interno di un intervallo di testo. I client Assistive Technology (AT) possono quindi trasferire questa posizione a un utente. Ad esempio, se un utente fa clic su un collegamento a un ancoraggio nella stessa pagina (collegamento a un segnalibro), la nuova posizione viene fornita all'indirizzo. | [Interfaccia IUIAutomation6](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation6) |
| 1809 | Win32 | Automazione interfaccia utente supporta la coalescenza degli eventi | Consente di migliorare le prestazioni tentando di rilevare, filtrare e ignorare gli eventi TextChanged di MSAA e UIA sequenziali duplicati generati da alcuni provider. | [Interfaccia IUIAutomation6](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation6) |
| 1809 | Win32 | Automazione interfaccia utente supporta il comportamento del ripristino della connessione | I messaggi da un client di automazione interfaccia utente a un provider vengono sospesi (per impostazione predefinita per due secondi) se il provider non risponde. In questo modo si riduce la frequenza dei timeout estesi e si riduce al minimo il sovraccarico di un provider non reattivo con eventi e richieste. | [Interfaccia IUIAutomation6](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation6) |
| 1809 | Piattaforma UWP | Servizi avanzati per la lettura dello schermo | Nei client conosce la posizione di lettura dello schermo udibile (controllo o contenuto) e la modalità di lettura. | [Classe ScreenReaderService](/uwp/api/windows.ui.accessibility.screenreaderservice) |
| 1809 | Win32, UWP | Automazione interfaccia utente supporta finestre di dialogo | I provider di automazione interfaccia utente possono contrassegnare gli elementi di UIA specificamente come finestre di dialogo. Gli enti ATs spesso presentano finestre di dialogo in modo diverso rispetto agli utenti.  | [IUIAutomationElement9](https://review.docs.microsoft.com/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement9)<br/><br/>[Classe ContentDialog](/uwp/api/windows.ui.xaml.controls.contentdialog) |
| 1809 |  Piattaforma UWP | Ridimensionamento del testo  | Ridimensiona le dimensioni del testo nelle applicazioni e nelle pagine Web. | [Evento UISettings. TextScaleFactorChanged](/uwp/api/windows.ui.viewmanagement.uisettings.textscalefactorchanged)<br/><br/>[Ridimensionamento del testo](/windows/uwp/design/input/text-scaling) |
