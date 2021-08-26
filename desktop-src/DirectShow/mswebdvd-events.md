---
description: Eventi MSWebDVD
ms.assetid: e43ea4ad-8ebe-4096-a9f3-a8f618b46877
title: Eventi MSWebDVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e61a37eda7b8c2ebafc704d96195cc9e92e70fbd9d8bfda4aa7c971cd890e41c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042711"
---
# <a name="mswebdvd-events"></a>Eventi MSWebDVD

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

> [!Note]  
> Questa API è deprecata. Per informazioni sulla riproduzione e l'esplorazione di DVD in DirectShow, vedere [Applicazioni DVD](dvd-applications.md).

 

Il controllo Microsoft MSWebDVD ® ActiveX® notifica all'applicazione quando si verificano vari tipi di eventi interni o quando vengono rilevati determinati dati sul disco.

La maggior parte degli eventi riguarda i controlli UOP (User Operation). Gli autori di DVD possono codificare il disco in modo che qualsiasi comando DVD (ad esempio **PlayForwards,** **Pause,** **ShowMenu** e così via) possa essere disabilitato in qualsiasi momento. Ad esempio, la maggior parte dei dischi non consentirà agli utenti di inoltrare o visualizzare rapidamente un menu durante la riproduzione dell'avviso DISOB. Al termine dell'avviso, il disco consente queste operazioni. Gestendo gli eventi UOP, l'applicazione può aggiornare l'interfaccia utente per mostrare all'utente quali comandi sono attualmente consentiti dal disco. Il modo più comune per eseguire questa operazione è disabilitare un pulsante. Ad esempio, se l'applicazione ha ricevuto un evento PlayForwards con **bEnabled** impostato su **FALSE,** è possibile disabilitare il pulsante Riproduci. Quando ha ricevuto l'evento **con bEnabled** impostato su **TRUE,** è possibile abilitare nuovamente il pulsante.

Esistono tre eventi che non sono correlati ai controlli UOP. **L'evento DVDNotify** notifica all'applicazione molti tipi diversi di eventi correlati a DVD, identificati nel *parametro EventCode.* Alcuni eventi hanno informazioni aggiuntive nei *parametri Param1* e *Param2.* **L'evento ReadyStateChange** notifica all'applicazione le modifiche apportate alla proprietà MSWebDVD ReadyState, che è una proprietà comune a tutti ActiveX controllo. **L'evento UpdateOverlay** viene inviato alle applicazioni solo se ospita MSWebDVD in modalità senza finestra. Le applicazioni devono rispondere a questo evento solo se visualizzano pulsanti mobili sul rettangolo video in modalità schermo intero.



| Event                                                                  | Descrizione                                                                           |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [**ChangeCurrentAngle**](changecurrentangle.md)                       | Inviato quando il disco abilita o disabilita la modifica dell'angolo.                            |
| [**ChangeCurrentAudioStream**](changecurrentaudiostream.md)           | Inviato quando il disco abilita o disabilita la modifica del flusso audio.                     |
| [**ChangeCurrentSubpictureStream**](changecurrentsubpicturestream.md) | Inviato quando il **comando ChangeCurrentSubpictureStream** è stato abilitato o disabilitato. |
| [**DVDNotify**](dvdnotify.md)                                         | Notifica a un'applicazione molti eventi DVD e istruzioni su disco diversi.           |
| [**PauseOn**](pauseon.md)                                             | Inviato quando il **comando Sospendi** è stato abilitato o disabilitato.                         |
| [**PlayAtTime**](playattime.md)                                       | Inviato quando il **comando PlayAtTime** è stato abilitato o disabilitato.                    |
| [**PlayAtTimeInTitle**](playattimeintitle.md)                         | Inviato quando il **comando PlayAtTimeInTitle** è stato abilitato o disabilitato.             |
| [**PlayBackwards**](playbackwards.md)                                 | Inviato quando il **comando PlayBackwards** è stato abilitato o disabilitato.                 |
| [**PlayChapter**](playchapter.md)                                     | Inviato quando il **comando PlayChapter** è stato abilitato o disabilitato.                   |
| [**PlayChapterInTitle**](playchapterintitle.md)                       | Inviato quando il **comando PlayChapterInTitle** è stato abilitato o disabilitato.            |
| [**PlayForwards**](playforwards.md)                                   | Inviato quando il **comando PlayForwards** è stato abilitato o disabilitato.                  |
| [**PlayNextChapter**](playnextchapter.md)                             | Inviato quando il **comando PlayNextChapter** è stato abilitato o disabilitato.               |
| [**PlayPrevChapter**](playprevchapter.md)                             | Inviato quando il **comando PlayPrevChapter** è stato abilitato o disabilitato.               |
| [**PlayTitle**](playtitle.md)                                         | Inviato quando il **comando PlayTitle** è stato abilitato o disabilitato.                     |
| [**ReadyStateChange**](readystatechange.md)                           | Inviato quando la **proprietà ReadyState** del controllo MSWebDVD viene modificata.            |
| [**ReplayChapter**](replaychapter.md)                                 | Inviato quando il **comando ReplayChapter** è stato abilitato o disabilitato.                 |
| [**Riprendi**](resume.md)                                               | Inviato quando il **comando Resume** è stato abilitato o disabilitato.                        |
| [**ReturnFromSubmenu**](returnfromsubmenu.md)                         | Inviato quando il **comando ReturnFromSubmenu** è stato abilitato o disabilitato.             |
| [**SelectOrActivatButton**](selectoractivatbutton.md)                 | Inviato quando il disco abilita o disabilita la selezione o l'attivazione dei pulsanti di menu.   |
| [**ShowMenu**](showmenu.md)                                           | Inviato quando il disco abilita o disabilita la visualizzazione di un menu.                         |
| [**StillOff**](stilloff.md)                                           | Inviato quando il **comando StillOff** è stato abilitato o disabilitato.                      |
| [**Fermare**](stop.md)                                                   | Inviato quando il **comando Arresta** è stato abilitato o disabilitato.                          |
| [**UpdateOverlay**](updateoverlay.md)                                 | Inviato quando la superficie di sovrimpressione è stata spostata o ridimensionata o la relativa chiave di colore è stata modificata. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetto MSWebDVD](mswebdvd-object.md)
</dt> </dl>

 

 



