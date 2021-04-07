---
description: Comandi DVD
ms.assetid: 1204c73e-c3de-4488-8ee3-e76edbf72da0
title: Comandi DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5bf06127ab3829ed6cdcbbb70c3b2c1d1b41cf0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747143"
---
# <a name="dvd-commands"></a>Comandi DVD

I comandi di navigazione e riproduzione DVD sono definiti in una sezione della specifica DVD denominata Annex J, motivo per cui la documentazione di DirectShow fa spesso riferimento a "Annex J Commands". Tuttavia, i nomi indicati nell'allegato J non sono sempre molto intuitivi, quindi DirectShow usa nomi che possono essere più facili da comprendere.

La tabella seguente elenca i comandi dell'allegato J e i rispettivi equivalenti DirectShow.



| Comando Annex J                                                                           | Descrizione                                                                  | Metodo IDvdControl2                                                                           |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| \_Riproduzione titolo                                                                               | Riprodurre un titolo.                                                                | [**PlayTitle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playtitle)                                                   |
| \_Riproduzione PTT                                                                                 | Riprodurre un capitolo in un titolo.                                                   | [**PlayChapterInTitle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playchapterintitle)                                 |
| Tempo di \_ riproduzione                                                                                | Riprodurre un titolo a partire da un'ora specificata.                                 | [**PlayAtTimeInTitle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playattimeintitle)                                   |
| Interrompere                                                                                      | Arresta la riproduzione.                                                               | [**Interrompere**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stop)                                                             |
| GoUp                                                                                      | Tornare da un sottomenu al menu padre.                                    | [**ReturnFromSubmenu**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-returnfromsubmenu)                                   |
| \_Ricerca ora                                                                              | Riproduci in un momento specifico all'interno del titolo corrente.                           | [**PlayAtTime**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playattime)                                                 |
| \_Ricerca PTT                                                                               | Riproduci un capitolo nel titolo corrente.                                     | [**PlayChapter**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playchapter)                                               |
| \_Ricerca PrevPG                                                                            | Passare all'inizio del capitolo precedente e riprendere la riproduzione.                 | [**PlayPrevChapter**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playprevchapter)                                       |
| \_Ricerca TopPG                                                                             | Passare all'inizio del capitolo corrente e riprendere la riproduzione.                  | [**ReplayChapter**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-replaychapter)                                           |
| \_Ricerca NextPG                                                                            | Passare all'inizio del capitolo successivo e riprendere la riproduzione.                     | [**PlayNextChapter**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playnextchapter)                                       |
| Analisi in diretta \_                                                                             | Riprodurre in base a una velocità di riproduzione specificata. La frequenza di riproduzione predefinita è 1,0. | [**PlayForwards**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playforwards)                                             |
| Analisi a ritroso \_                                                                            | Riprodurre le versioni precedenti a una velocità di riproduzione specificata.                                  | [**PlayBackwards**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playbackwards)                                           |
| Chiamata di menu \_                                                                                | Visualizzare un menu.                                                                 | [**ShowMenu**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-showmenu)                                                     |
| Riprendi                                                                                    | Tornare da un menu e riprendere la riproduzione.                                      | [**Riprendi**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-resume)                                                         |
| \_Pulsante superiore \_ selezionare, \_ pulsante inferiore \_ selezionare, \_ pulsante sinistro \_ selezionare, pulsante \_ destro \_ Seleziona | Consente di selezionare un pulsante la cui posizione è relativa al pulsante attualmente selezionato. | [**SelectButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectbutton)                                             |
| Pulsante \_ attiva                                                                          | Consente di attivare il pulsante selezionato.                                                | [**ActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activatebutton)                                         |
| Pulsante \_ Seleziona \_ e \_ attiva                                                             | Selezionare e attivare un pulsante.                                                | [**SelectAndActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectandactivatebutton)                       |
| Ancora \_ disattivato                                                                                | Riprendere la riproduzione quando si visualizza un'immagine ancora.                               | [**StillOff**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff)                                                     |
| Sospendi \_ in                                                                                 | Sospendere la riproduzione.                                                              | [**Sospendere**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-pause)                                                           |
| \_Sospendi                                                                                | Riprende la riproduzione dallo stato sospeso.                                       | [**Sospendere**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-pause)                                                           |
| \_Selezione lingua \_ menu                                                                    | Consente di selezionare la lingua dei menu.                                               | [**SelectDefaultMenuLanguage**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectdefaultmenulanguage)                   |
| \_Modifica flusso \_ audio                                                                     | Impostare il flusso audio.                                                        | [**SelectAudioStream**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectaudiostream)                                   |
| Modifica del flusso di immagini secondarie \_ \_                                                               | Imposta il flusso di sottoimmagine; consente di abilitare o disabilitare la visualizzazione delle immagini.             | [**SelectSubpictureStream**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectsubpicturestream)                         |
| \_Modifica angolo                                                                             | Imposta l'angolo della fotocamera.                                                        | [**SelectAngle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectangle)                                               |
| \_Selezione livello padre \_                                                                   | Imposta il livello padre.                                                      | [**SelectParentalLevel**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectparentallevel)                               |
| Selezione del \_ paese \_ padre                                                                 | Impostare il paese/area geografica per la gestione dei genitori.                              | [**SelectParentalCountry**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectparentalcountry)                           |
| \_Modifica della \_ \_ modalità presentazione audio karaoke \_                                                | Impostare la modalità di combinazione audio per karaoke.                                       | [**SelectKaraokeAudioPresentationMode**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectkaraokeaudiopresentationmode) |
| \_Modifica della \_ modalità \_ presentazione video                                                         | Impostare la modalità di proporzioni su widescreen, letterbox o Pan Scan.             | [**SelectVideoModePreference**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectvideomodepreference)                   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Applicazioni DVD](dvd-applications.md)
</dt> </dl>

 

 



