---
description: Eventi MSWebDVD
ms.assetid: e43ea4ad-8ebe-4096-a9f3-a8f618b46877
title: Eventi MSWebDVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f363f15c35cbfe61a3ab1ff3703a31307785481
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303738"
---
# <a name="mswebdvd-events"></a>Eventi MSWebDVD

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

> [!Note]  
> Questa API è deprecata. Per informazioni sulla riproduzione e l'esplorazione dei DVD in DirectShow, vedere [applicazioni DVD](dvd-applications.md).

 

Il MSWebDVD Microsoft® ActiveX® Control invia una notifica all'applicazione quando si verificano vari tipi di eventi interni o quando vengono rilevate determinate informazioni sul disco.

La maggior parte degli eventi si riferisce ai controlli dell'operazione utente (UOP). Gli autori di DVD possono codificare il disco in modo che qualsiasi comando DVD, ad esempio **PlayForwards**, **pause**, **ShowMenu** e così via, possa essere disabilitato in qualsiasi momento. Ad esempio, la maggior parte dei dischi non consente agli utenti di eseguire rapidamente o visualizzare un menu mentre è in corso la riproduzione dell'avviso FBI. Al termine dell'avviso, il disco consente le operazioni seguenti. Gestendo gli eventi UOP, l'applicazione può aggiornare l'interfaccia utente per mostrare all'utente quali comandi sono attualmente consentiti dal disco. Il modo più comune per eseguire questa operazione è la disabilitazione di un pulsante. Se, ad esempio, l'applicazione ha ricevuto un evento PlayForwards con **bEnabled** impostato su **false**, è possibile disabilitare il pulsante Riproduci. Quando è stato ricevuto l'evento con **bEnabled** impostato su **true**, è possibile abilitare di nuovo il pulsante.

Esistono tre eventi che non si riferiscono ai controlli UOP. L'evento **DVDNotify** notifica all'applicazione molti tipi diversi di eventi correlati a DVD, che vengono identificati nel parametro *eventCode* . Alcuni eventi contengono informazioni aggiuntive nei parametri *param1* e *param2* . L'evento **ReadyStateChange** notifica all'applicazione le modifiche apportate alla proprietà ReadyState di mswebdvd, che è una proprietà comune a tutti i controlli ActiveX. L'evento **UpdateOverlay** viene inviato alle applicazioni solo se ospita mswebdvd in modalità senza finestra. Le applicazioni devono rispondere a questo evento solo se visualizzano i pulsanti a virgola mobile sul rettangolo video in modalità schermo intero.



| Event                                                                  | Descrizione                                                                           |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [**ChangeCurrentAngle**](changecurrentangle.md)                       | Inviato quando il disco Abilita o Disabilita la modifica dell'angolo.                            |
| [**ChangeCurrentAudioStream**](changecurrentaudiostream.md)           | Inviato quando il disco Abilita o Disabilita la modifica del flusso audio.                     |
| [**ChangeCurrentSubpictureStream**](changecurrentsubpicturestream.md) | Inviato quando il comando **ChangeCurrentSubpictureStream** è stato abilitato o disabilitato. |
| [**DVDNotify**](dvdnotify.md)                                         | Notifica a un'applicazione di molti eventi DVD e istruzioni per i dischi diversi.           |
| [**PauseOn**](pauseon.md)                                             | Inviato quando il comando **Sospendi** è stato abilitato o disabilitato.                         |
| [**PlayAtTime**](playattime.md)                                       | Inviato quando il comando **PlayAtTime** è stato abilitato o disabilitato.                    |
| [**PlayAtTimeInTitle**](playattimeintitle.md)                         | Inviato quando il comando **PlayAtTimeInTitle** è stato abilitato o disabilitato.             |
| [**PlayBackwards**](playbackwards.md)                                 | Inviato quando il comando **PlayBackwards** è stato abilitato o disabilitato.                 |
| [**PlayChapter**](playchapter.md)                                     | Inviato quando il comando **PlayChapter** è stato abilitato o disabilitato.                   |
| [**PlayChapterInTitle**](playchapterintitle.md)                       | Inviato quando il comando **PlayChapterInTitle** è stato abilitato o disabilitato.            |
| [**PlayForwards**](playforwards.md)                                   | Inviato quando il comando **PlayForwards** è stato abilitato o disabilitato.                  |
| [**PlayNextChapter**](playnextchapter.md)                             | Inviato quando il comando **PlayNextChapter** è stato abilitato o disabilitato.               |
| [**PlayPrevChapter**](playprevchapter.md)                             | Inviato quando il comando **PlayPrevChapter** è stato abilitato o disabilitato.               |
| [**PlayTitle**](playtitle.md)                                         | Inviato quando il comando **PlayTitle** è stato abilitato o disabilitato.                     |
| [**ReadyStateChange**](readystatechange.md)                           | Inviato quando la proprietà **ReadyState** del controllo mswebdvd è stata modificata.            |
| [**ReplayChapter**](replaychapter.md)                                 | Inviato quando il comando **ReplayChapter** è stato abilitato o disabilitato.                 |
| [**Riprendi**](resume.md)                                               | Inviato quando il comando **Resume** è stato abilitato o disabilitato.                        |
| [**ReturnFromSubmenu**](returnfromsubmenu.md)                         | Inviato quando il comando **ReturnFromSubmenu** è stato abilitato o disabilitato.             |
| [**SelectOrActivatButton**](selectoractivatbutton.md)                 | Inviato quando il disco Abilita o Disabilita la selezione o l'attivazione dei pulsanti di menu.   |
| [**ShowMenu**](showmenu.md)                                           | Inviato quando il disco Abilita o Disabilita la visualizzazione di un menu.                         |
| [**StillOff**](stilloff.md)                                           | Inviato quando il comando **StillOff** è stato abilitato o disabilitato.                      |
| [**Interrompere**](stop.md)                                                   | Inviato quando il comando di **arresto** è stato abilitato o disabilitato.                          |
| [**UpdateOverlay**](updateoverlay.md)                                 | Inviato quando la superficie sovrapposta è stata spostata o ridimensionata o la chiave di colore è cambiata. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetto MSWebDVD](mswebdvd-object.md)
</dt> </dl>

 

 



