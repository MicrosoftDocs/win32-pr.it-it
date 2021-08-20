---
description: Codici di notifica degli eventi DVD
ms.assetid: c028918e-aba2-49b2-a6ce-c620ab38b558
title: Codici di notifica degli eventi DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 717c260c84a1038860ee04f46db6224025b7709c3ad039e7625a48ae6359cc05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119686451"
---
# <a name="dvd-event-notification-codes"></a>Codici di notifica degli eventi DVD

Questa sezione elenca i codici di notifica degli eventi per la riproduzione e la navigazione dei DVD in DirectShow.

Per informazioni sulla ricezione di eventi in DirectShow, vedere [Notifica di eventi in DirectShow](event-notification-in-directshow.md).

Per altri codici evento non DVD, vedere [Codici di notifica degli eventi](event-notification-codes.md).



| Codice di notifica degli eventi                                                        | Descrizione                                                                                                                                                               |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EC \_ DVD \_ ANGLE \_ CHANGE**](ec-dvd-angle-change.md)                          | Segnala che il numero di angoli disponibili è cambiato o che il numero di angolo corrente è cambiato.                                                                      |
| [**EC \_ DVD \_ ANGLES \_ AVAILABLE**](ec-dvd-angles-available.md)                  | Indica se è in corso la riproduzione di un blocco angolare ed è possibile eseguire modifiche all'angolo.                                                                                      |
| [**MODIFICA DEL \_ FLUSSO AUDIO DI EC DVD \_ \_ \_**](ec-dvd-audio-stream-change.md)           | Segnala che il numero del flusso audio corrente è stato modificato per il titolo principale.                                                                                                  |
| [**EC \_ DVD \_ BeginNavigationCommands**](ec-dvd-beginnavigationcommands.md)     | Inviato all'avvio di un set di comandi di navigazione DVD.                                                                                                                  |
| [**PULSANTE \_ DVD EC ATTIVATO \_ \_ \_ AUTOMATICAMENTE**](ec-dvd-button-auto-activated.md)       | Segnala che un pulsante di menu è stato attivato automaticamente in base alle istruzioni sul disco.                                                                                 |
| [**MODIFICA DEL \_ PULSANTE DVD \_ \_ EC**](ec-dvd-button-change.md)                        | Segnala che il numero di pulsanti disponibili è cambiato o che il numero del pulsante attualmente selezionato è cambiato.                                                         |
| [**EC \_ DVD \_ CHAPTER \_ AUTOSTOP**](ec-dvd-chapter-autostop.md)                  | Indica che la riproduzione è stata arrestata come risultato di una chiamata al metodo [**IDvdControl2::P layChaptersAutoStop.**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playchaptersautostop)                    |
| [**EC \_ DVD \_ CHAPTER \_ START**](ec-dvd-chapter-start.md)                        | Segnala che lo strumento di navigazione DVD ha avviato la riproduzione di un nuovo capitolo nel titolo corrente.                                                                                    |
| [**AVVIO \_ DI EC DVD \_ \_ CMD**](ec-dvd-cmd-start.md)                                | Segnala l'inizio di un comando specifico.                                                                                                                              |
| [**EC \_ DVD \_ CMD \_ END**](ec-dvd-cmd-end.md)                                    | Segnala che un comando specifico è stato completato.                                                                                                                          |
| [**EC \_ DVD \_ CURRENT \_ HMSF \_ TIME**](ec-dvd-current-hmsf-time.md)               | Segnala l'ora corrente in [**\_ formato DVD HMSF \_ TIMECODE**](/windows/win32/api/strmif/ns-strmif-dvd_hmsf_timecode) all'inizio di ogni unità oggetto video (VOBU).                                   |
| [**ORA \_ CORRENTE DEL DVD \_ \_ EC**](ec-dvd-current-time.md)                          | Segnala l'inizio di ogni VOBU.                                                                                                                                      |
| [**DISCO \_ DVD \_ EC \_ ESPULSO**](ec-dvd-disc-ejected.md)                          | Segnala che un disco è stato espulso dall'unità.                                                                                                                      |
| [**EC \_ DVD \_ DISC \_ INSERTED**](ec-dvd-disc-inserted.md)                        | Segnala che un disco è stato inserito nell'unità.                                                                                                                     |
| [**MODIFICA DEL \_ DOMINIO DEL DVD \_ \_ EC**](ec-dvd-domain-change.md)                        | Indica il nuovo dominio dello strumento di navigazione DVD.                                                                                                                                 |
| [**ERRORE \_ DEL DVD \_ EC**](ec-dvd-error.md)                                         | Segnala una condizione di errore DVD.                                                                                                                                            |
| [**Modifica \_ \_ GPRM del DVD \_ EC**](ec-dvd-gprm-change.md)                            | Inviato quando il valore di un registro di parametri generali (GPRM) cambia.                                                                                                       |
| [**MODALITÀ \_ EC DVD PER TUTTO IL \_ \_ DVD**](ec-dvd-karaoke-mode.md)                          | Indica che lo strumento di navigazione ha iniziato a riprodurre o ha terminato la riproduzione dei dati relativi al karaoke.                                                                                   |
| [**EC \_ DVD \_ NavigationCommand**](ec-dvd-navigationcommand.md)                 | Inviato quando lo strumento [di navigazione DVD](dvd-navigator-filter.md) elabora un comando di navigazione DVD.                                                                               |
| [**EC \_ DVD \_ NO \_ FP \_ PGC**](ec-dvd-no-fp-pgc.md)                               | Indica che il disco DVD non ha un \_ PGC FP (First Play Program Chain).                                                                                           |
| [**EC \_ DVD \_ PARENTAL \_ LEVEL \_ CHANGE**](ec-dvd-parental-level-change.md)       | Segnala che il livello genitoriale del contenuto creato sta per cambiare.                                                                                               |
| [**MODIFICA DELLA \_ VELOCITÀ DI RIPRODUZIONE DEI DVD \_ \_ \_ EC**](ec-dvd-playback-rate-change.md)         | Indica che è stata avviata una modifica della velocità di riproduzione e che la nuova frequenza è nel parametro .                                                                            |
| [**RIPRODUZIONE \_ DI DVD EC \_ \_ ARRESTATA**](ec-dvd-playback-stopped.md)                  | Indica che la riproduzione è stata arrestata. Lo strumento di navigazione DVD ha completato la riproduzione del titolo e non ha trovato altre istruzioni di diramazione per la riproduzione successiva. |
| [**EC \_ DVD \_ PLAYPERIOD \_ AUTOSTOP**](ec-dvd-playperiod-autostop.md)            | Indica che lo strumento di navigazione ha terminato la riproduzione del segmento specificato in una chiamata a PlayPeriodInTitleAutoStop.                                                           |
| [**EC \_ DVD \_ PROGRAM \_ CELL \_ CHANGE**](ec-dvd-program-cell-change.md)           | Inviato quando cambia il numero di programma DVD o il numero di cella.                                                                                                                  |
| [**EC \_ DVD \_ PROGRAM \_ CHAIN \_ CHANGE**](ec-dvd-program-chain-change.md)         | Inviato quando la catena di programmi corrente (PGC) cambia.                                                                                                                            |
| [**Modifica \_ \_ SPRM del DVD \_ EC**](ec-dvd-sprm-change.md)                            | Inviato quando il valore di un registro dei parametri di sistema (SPRM) cambia.                                                                                                        |
| [**EC \_ DVD \_ STILL \_ OFF**](ec-dvd-still-off.md)                                | Segnala la fine di qualsiasi oggetto ancorato.                                                                                                                                             |
| [**EC \_ DVD \_ STILL \_ ON**](ec-dvd-still-on.md)                                  | Segnala l'inizio di qualsiasi ancora.                                                                                                                                       |
| [**EC \_ DVD \_ SUBPICTURE \_ STREAM \_ CHANGE**](ec-dvd-subpicture-stream-change.md) | Segnala che il numero di flusso dell'immagine secondaria corrente è stato modificato per il titolo principale.                                                                                             |
| [**MODIFICA \_ DEL SET DI TITOLI DEL DVD \_ \_ \_ EC**](ec-dvd-title-set-change.md)                 | Inviato quando cambia il set di titoli video (VTS) corrente.                                                                                                                          |
| [**MODIFICA DEL \_ TITOLO DEL DVD \_ \_ EC**](ec-dvd-title-change.md)                          | Indica quando cambia il numero del titolo corrente.                                                                                                                          |
| [**EC \_ DVD \_ VALID \_ UOPS \_ CHANGE**](ec-dvd-valid-uops-change.md)               | Segnala che il set disponibile di [**metodi di interfaccia IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) è stato modificato.                                                                     |
| [**OFFSET \_ \_ VOBU DEL \_ DVD EC**](ec-dvd-vobu-offset.md)                            | Inviato quando lo strumento [di navigazione DVD](dvd-navigator-filter.md) analizza un pacchetto PCI.                                                                                              |
| [**Timestamp \_ \_ VOBU DEL \_ DVD EC**](ec-dvd-vobu-timestamp.md)                      | Inviato quando lo strumento [di navigazione DVD](dvd-navigator-filter.md) analizza un pacchetto PCI.                                                                                              |
| [**AVVISO \_ DI EC DVD \_**](ec-dvd-warning.md)                                     | Segnala una condizione di avviso DVD.                                                                                                                                          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti e GUID](constants-and-guids.md)
</dt> </dl>

 

 



