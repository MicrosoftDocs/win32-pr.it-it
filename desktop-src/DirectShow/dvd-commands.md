---
description: Comandi DVD
ms.assetid: 1204c73e-c3de-4488-8ee3-e76edbf72da0
title: Comandi DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d02f9c0b6a50b6d7eb67832286ee980b0faf69460621a46caf98089efc24b19c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117820585"
---
# <a name="dvd-commands"></a>Comandi DVD

I comandi di spostamento e riproduzione dei DVD sono definiti in una sezione della specifica DVD denominata Annex J, motivo per cui la documentazione di DirectShow spesso fa riferimento ai "comandi Annex J". I nomi specificati in Annex J non sono tuttavia sempre molto intuitivi, quindi DirectShow usa nomi che potrebbero essere più facili da comprendere.

Nella tabella seguente sono elencati i comandi Annex J e i relativi DirectShow equivalenti.



| Comando Annex J                                                                           | Descrizione                                                                  | Metodo IDvdControl2                                                                           |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| Riproduzione \_ titolo                                                                               | Riprodurre un titolo.                                                                | [**PlayTitle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playtitle)                                                   |
| PTT \_ Play                                                                                 | Riprodurre un capitolo in un titolo.                                                   | [**PlayChapterInTitle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playchapterintitle)                                 |
| Riproduzione \_ temporale                                                                                | Riprodurre un titolo a partire da un'ora specificata.                                 | [**PlayAtTimeInTitle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playattimeintitle)                                   |
| Interrompere                                                                                      | Arrestare la riproduzione.                                                               | [**Fermare**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stop)                                                             |
| GoUp                                                                                      | Tornare da un sottomenu al menu padre.                                    | [**ReturnFromSubmenu**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-returnfromsubmenu)                                   |
| Ricerca \_ temporale                                                                              | Riprodurre in un'ora specificata all'interno del titolo corrente.                           | [**PlayAtTime**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playattime)                                                 |
| Ricerca \_ PTT                                                                               | Riprodurre un capitolo all'interno del titolo corrente.                                     | [**PlayChapter**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playchapter)                                               |
| Ricerca \_ prevPG                                                                            | Passare all'inizio del capitolo precedente e riprendere la riproduzione.                 | [**PlayPrevChapter**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playprevchapter)                                       |
| TopPG \_ Search                                                                             | Passare all'inizio del capitolo corrente e riprendere la riproduzione.                  | [**ReplayChapter**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-replaychapter)                                           |
| NextPG \_ Search                                                                            | Passare all'inizio del capitolo successivo e riprendere la riproduzione.                     | [**PlayNextChapter**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playnextchapter)                                       |
| Forward \_ Scan                                                                             | Riproduci in avanti con una velocità di riproduzione specificata. La velocità di riproduzione predefinita è 1,0. | [**PlayForwards**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playforwards)                                             |
| Analisi \_ all'indietro                                                                            | Riprodurre all'indietro con una velocità di riproduzione specificata.                                  | [**PlayBackwards**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playbackwards)                                           |
| Chiamata di \_ menu                                                                                | Visualizzare un menu.                                                                 | [**ShowMenu**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-showmenu)                                                     |
| Riprendi                                                                                    | Tornare da un menu e riprendere la riproduzione.                                      | [**Riprendi**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-resume)                                                         |
| Selezione \_ del pulsante \_ superiore, selezione del pulsante \_ \_ inferiore, selezione del pulsante \_ \_ sinistro, selezione del pulsante \_ destro \_ | Selezionare un pulsante la cui posizione è relativa al pulsante attualmente selezionato. | [**SelectButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectbutton)                                             |
| Pulsante \_ Attiva                                                                          | Attivare il pulsante selezionato.                                                | [**ActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activatebutton)                                         |
| Selezione \_ e attivazione dei \_ \_ pulsanti                                                             | Selezionare e attivare un pulsante.                                                | [**SelectAndActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectandactivatebutton)                       |
| Ancora \_ disattivata                                                                                | Riprendere la riproduzione quando si visualizza un'immagine ancorata.                               | [**StillOff**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff)                                                     |
| \_Sospendi in data                                                                                 | Sospendere la riproduzione.                                                              | [**Sospendi**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-pause)                                                           |
| \_Sospendi                                                                                | Riprendere la riproduzione dallo stato sospeso.                                       | [**Sospendi**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-pause)                                                           |
| Selezione \_ lingua \_ menu                                                                    | Selezionare la lingua per i menu.                                               | [**SelectDefaultMenuLanguage**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectdefaultmenulanguage)                   |
| Modifica \_ del flusso \_ audio                                                                     | Impostare il flusso audio.                                                        | [**SelectAudioStream**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectaudiostream)                                   |
| Modifica del flusso \_ immagine \_ secondaria                                                               | Impostare il flusso dell'immagine secondaria; abilita o disabilita la visualizzazione delle immagini secondarie.             | [**SelectSubpictureStream**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectsubpicturestream)                         |
| Modifica \_ dell'angolo                                                                             | Impostare l'angolo della fotocamera.                                                        | [**SelectAngle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectangle)                                               |
| Selezione \_ livello \_ genitori                                                                   | Impostare il livello dei genitori.                                                      | [**SelectParentalLevel**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectparentallevel)                               |
| Selezione \_ paese genitori \_                                                                 | Impostare il paese/area geografica per la gestione dei genitori.                              | [**SelezionareParentalCountry**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectparentalcountry)                           |
| Modifica \_ della modalità audio presentazione \_ \_ \_ audio                                                | Impostare la modalità di combinazione audio per il mixer audio.                                       | [**SelectKaraokeAudioPresentationMode**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectkaraokeaudiopresentationmode) |
| Modifica \_ della modalità di presentazione \_ \_ video                                                         | Impostare la modalità proporzioni su widescreen, letterbox o pan scan.             | [**SelectVideoModePreference**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectvideomodepreference)                   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Applicazioni DVD](dvd-applications.md)
</dt> </dl>

 

 



