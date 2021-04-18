---
description: Codici di notifica degli eventi DVD
ms.assetid: c028918e-aba2-49b2-a6ce-c620ab38b558
title: Codici di notifica degli eventi DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e15172e8eba3da048e7c7704a90d7992fa21714a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304016"
---
# <a name="dvd-event-notification-codes"></a>Codici di notifica degli eventi DVD

Questa sezione elenca i codici di notifica degli eventi per la riproduzione e la navigazione in DVD in DirectShow.

Per informazioni sulla ricezione di eventi in DirectShow, vedere [notifica degli eventi in DirectShow](event-notification-in-directshow.md).

Per altri codici evento non DVD, vedere [codici di notifica degli eventi](event-notification-codes.md).



| Codice di notifica degli eventi                                                        | Descrizione                                                                                                                                                               |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ Modifica angolo DVD \_ EC**](ec-dvd-angle-change.md)                          | Segnala che il numero di angoli disponibili è stato modificato o che il numero dell'angolo corrente è stato modificato.                                                                      |
| [**\_angoli DVD \_ EC \_ disponibili**](ec-dvd-angles-available.md)                  | Indica se un blocco angolo viene riprodotto e le modifiche dell'angolo possono essere eseguite.                                                                                      |
| [**\_ \_ \_ Modifica flusso audio DVD \_ EC**](ec-dvd-audio-stream-change.md)           | Segnala che il numero di flusso audio corrente è stato modificato per il titolo principale.                                                                                                  |
| [**\_BeginNavigationCommands DVD \_ EC**](ec-dvd-beginnavigationcommands.md)     | Inviato quando viene avviato un set di comandi di spostamento su DVD.                                                                                                                  |
| [**\_pulsante DVD \_ EC \_ \_ attivato automaticamente**](ec-dvd-button-auto-activated.md)       | Segnala che un pulsante di menu è stato attivato automaticamente per istruzioni sul disco.                                                                                 |
| [**\_ \_ modifica pulsante DVD \_ EC**](ec-dvd-button-change.md)                        | Segnala che il numero di pulsanti disponibili è stato modificato o che il numero di pulsante attualmente selezionato è stato modificato.                                                         |
| [**autostop del \_ capitolo DVD EC \_ \_**](ec-dvd-chapter-autostop.md)                  | Indica che la riproduzione è stata arrestata in seguito a una chiamata al metodo [**IDVDControl2::P laychaptersautostop**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playchaptersautostop) .                    |
| [**\_inizio del \_ capitolo del DVD EC \_**](ec-dvd-chapter-start.md)                        | Segnala che il navigatore DVD ha avviato la riproduzione di un nuovo capitolo nel titolo corrente.                                                                                    |
| [**\_ \_ avvio cmd DVD \_ EC**](ec-dvd-cmd-start.md)                                | Segnala l'inizio di un determinato comando.                                                                                                                              |
| [**\_ \_ fine cmd DVD \_ EC**](ec-dvd-cmd-end.md)                                    | Segnala il completamento di un determinato comando.                                                                                                                          |
| [**\_ \_ \_ ora HMSF corrente del DVD EC \_**](ec-dvd-current-hmsf-time.md)               | Segnala l'ora corrente in formato [**DVD \_ HMSF \_ timecode**](/windows/win32/api/strmif/ns-strmif-dvd_hmsf_timecode) all'inizio di ogni unità di oggetti video (VOBU).                                   |
| [**\_ \_ ora corrente DVD \_ EC**](ec-dvd-current-time.md)                          | Segnala l'inizio di ogni VOBU.                                                                                                                                      |
| [**\_disco DVD \_ EC \_ rimosso**](ec-dvd-disc-ejected.md)                          | Segnala che un disco è stato espulso dall'unità.                                                                                                                      |
| [**\_disco DVD \_ EC \_ inserito**](ec-dvd-disc-inserted.md)                        | Segnala che è stato inserito un disco nell'unità.                                                                                                                     |
| [**\_ \_ Modifica dominio DVD \_ EC**](ec-dvd-domain-change.md)                        | Indica il nuovo dominio del navigatore DVD.                                                                                                                                 |
| [**\_errore DVD \_ EC**](ec-dvd-error.md)                                         | Segnala una condizione di errore DVD.                                                                                                                                            |
| [**\_ \_ Modifica GPRM DVD \_ EC**](ec-dvd-gprm-change.md)                            | Inviato quando viene modificato il valore di un registro parametri generale (GPRM).                                                                                                       |
| [**\_ \_ modalità Karaoke DVD \_ EC**](ec-dvd-karaoke-mode.md)                          | Indica che lo strumento di navigazione ha iniziato a riprodurre i dati del karaoke o ha terminato la riproduzione.                                                                                   |
| [**\_NavigationCommand DVD \_ EC**](ec-dvd-navigationcommand.md)                 | Inviato quando il [navigatore DVD](dvd-navigator-filter.md) elabora un comando di spostamento DVD.                                                                               |
| [**\_DVD EC \_ nessun \_ \_ PGC FP**](ec-dvd-no-fp-pgc.md)                               | Indica che il disco DVD non dispone di un \_ PGC FP (prima catena di programmi di riproduzione).                                                                                           |
| [**\_modifica a \_ livello padre \_ DVD \_ EC**](ec-dvd-parental-level-change.md)       | Segnala che il livello padre del contenuto creato sta per essere modificato.                                                                                               |
| [**\_modifica della \_ frequenza di riproduzione DVD \_ EC \_**](ec-dvd-playback-rate-change.md)         | Indica che è stata avviata una modifica della frequenza di riproduzione e che il nuovo tasso è nel parametro.                                                                            |
| [**\_riproduzione DVD \_ EC \_ arrestata**](ec-dvd-playback-stopped.md)                  | Indica che la riproduzione è stata arrestata. Il navigatore DVD ha completato la riproduzione del titolo e non ha trovato altre istruzioni di branching per la riproduzione successiva. |
| [**\_autostop \_ PLAYPERIOD DVD EC \_**](ec-dvd-playperiod-autostop.md)            | Indica che lo strumento di spostamento ha terminato la riproduzione del segmento specificato in una chiamata a PlayPeriodInTitleAutoStop.                                                           |
| [**\_ \_ \_ modifica cella programma DVD \_ EC**](ec-dvd-program-cell-change.md)           | Inviato quando il numero del programma DVD o il numero di cella cambia.                                                                                                                  |
| [**\_ \_ \_ modifica catena programma DVD \_ EC**](ec-dvd-program-chain-change.md)         | Inviato quando viene modificato il PGC (Current Program Chain).                                                                                                                            |
| [**\_ \_ Modifica SPRM DVD \_ EC**](ec-dvd-sprm-change.md)                            | Inviato quando viene modificato il valore di un registro di parametri di sistema (SPRM).                                                                                                        |
| [**\_DVD EC \_ ancora \_ disattivato**](ec-dvd-still-off.md)                                | Segnala la fine di qualsiasi ancora.                                                                                                                                             |
| [**\_DVD EC \_ ancora \_ acceso**](ec-dvd-still-on.md)                                  | Segnala l'inizio di qualsiasi ancora.                                                                                                                                       |
| [**\_ \_ Modifica flusso di sottoimmagine DVD EC \_ \_**](ec-dvd-subpicture-stream-change.md) | Segnala che il numero del flusso di sottoimmagine corrente è stato modificato per il titolo principale.                                                                                             |
| [**\_modifica del \_ set di titoli del DVD EC \_ \_**](ec-dvd-title-set-change.md)                 | Inviato quando cambia il set di titoli video corrente (VTS).                                                                                                                          |
| [**\_modifica del \_ titolo del DVD EC \_**](ec-dvd-title-change.md)                          | Indica quando cambia il numero del titolo corrente.                                                                                                                          |
| [**\_ \_ \_ modifica UOPs valida DVD \_ EC**](ec-dvd-valid-uops-change.md)               | Segnala che il set disponibile di metodi dell'interfaccia [**IDVDControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) è stato modificato.                                                                     |
| [**\_ \_ Offset VOBU DVD \_ EC**](ec-dvd-vobu-offset.md)                            | Inviato quando il [navigatore DVD](dvd-navigator-filter.md) analizza un pacchetto PCI.                                                                                              |
| [**\_ \_ Timestamp VOBU DVD \_ EC**](ec-dvd-vobu-timestamp.md)                      | Inviato quando il [navigatore DVD](dvd-navigator-filter.md) analizza un pacchetto PCI.                                                                                              |
| [**\_avviso di DVD EC \_**](ec-dvd-warning.md)                                     | Segnala una condizione di avviso DVD.                                                                                                                                          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti e GUID](constants-and-guids.md)
</dt> </dl>

 

 



