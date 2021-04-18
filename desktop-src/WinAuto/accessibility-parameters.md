---
title: Parametri di accessibilità
description: Il sistema gestisce un set di parametri di accessibilità che indicano se l'utente ha particolari esigenze o preferenze che richiedono che le applicazioni modifichino il comportamento predefinito.
ms.assetid: efa289bb-5965-4002-93df-116ab2621efc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5f089b28d36ffa982ca6568996126a812263af9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300190"
---
# <a name="accessibility-parameters"></a>Parametri di accessibilità

Il sistema gestisce un set di parametri di accessibilità che indicano se l'utente ha particolari esigenze o preferenze che richiedono che le applicazioni modifichino il comportamento predefinito. L'utente controlla lo stato di questi parametri, in genere usando il centro di accesso facilitato nel pannello di controllo. Le applicazioni del pannello di controllo o altri programmi che consentono all'utente di personalizzare l'ambiente possono utilizzare la funzione [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) per impostare i parametri di accessibilità.

Se un utente modifica questi parametri, il pannello di controllo Invia il messaggio [**WM \_ SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) . Le applicazioni devono rispondere a questo messaggio e usare [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) per determinare lo stato dei parametri di accessibilità. Quando è abilitato un parametro di accessibilità, l'applicazione deve modificare l'interfaccia utente, se necessario, per soddisfare le preferenze dell'utente.

Windows supporta i seguenti parametri di accessibilità.



| Parametro                                                                    | Descrizione                                                                                                                                                                    |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [High contrast](high-contrast-parameter.md)                                 | Indica che le applicazioni devono fornire un contrasto elevato tra oggetti visivi in primo piano e in background.                                                                            |
| [Preferenza tastiera](keyboard-preference-parameter.md)                     | Indica che le applicazioni devono visualizzare le interfacce della tastiera che altrimenti sarebbero nascoste.                                                                                 |
| [Utilità per la lettura dello schermo](screen-reader-parameter.md)                                 | Indica che le applicazioni devono fornire informazioni testuali in situazioni in cui altrimenti le informazioni verranno presentate graficamente.                                     |
| [Mostra suoni (e flag Descrizione audio)](showsounds-parameter.md) | Indica che le applicazioni devono anche fornire un avviso o un segnale visivo quando usa un suono per trasmettere informazioni importanti o fornire una descrizione audio per gli elementi visivi. |
| [Animazione area client](client-area-animation.md)                           | Indica che le applicazioni devono rispettare le preferenze dell'utente per la visualizzazione dell'animazione nell'area client.                                                                       |
| [Durata messaggio](message-duration.md)                                     | Indica che le applicazioni che forniscono notifiche popup devono monitorare i flag relativi alla durata dei messaggi e modificare la lunghezza della notifica.                                  |



 

I parametri di sistema seguenti sono utili per le applicazioni di accessibilità. Per altre informazioni, vedere funzione [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) .



| Gruppo di parametri      | Parametro                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Parametri del desktop   | SPI \_ GETWORKAREA, SPI \_ SETWORKAREA                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Parametri di input     | SPI \_ GETKEYBOARDCUES, SPI \_ GETKEYBOARDDELAY, SPI \_ GETKEYBOARDPREF, SPI \_ GETKEYBOARDSPEED, SPI \_ GETMESSAGEDURATION, SPI \_ GetMouse, SPI \_ GETMOUSEHOVERHEIGHT, SPI \_ GETMOUSEHOVERTIME, SPI \_ GETMOUSEHOVERWIDTH, SPI \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ GETMOUSESPEED, SPI GETMOUSETRAILS, SPI GETSNAPTODEFBUTTON, SPI GETWHEELSCROLLLINES, SPI SETDOUBLECLICKTIME, SPI SETDOUBLECLKHEIGHT, SPI SETDOUBLECLKWIDTH, SPI SETKEYBOARDCUES, SPI SETKEYBOARDDELAY, SPI SETKEYBOARDPREF, SPI SETKEYBOARDSPEED, SPI SETMOUSEHOVERHEIGHT, SPI SETMOUSEHOVERTIME, SPI SETMOUSEHOVERWIDTH, SPI SETMOUSESPEED, SPI SETMOUSETRAILS, SPI SETSNAPTODEFBUTTON, SPI SETWHEELSCROLLLINES, SPI di SPI |
| Parametri degli effetti dell'interfaccia utente | SPI \_ GETMENUUNDERLINES, SPI \_ SETMENUUNDERLINES                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Parametri finestra    | SPI \_ GETCARETWIDTH, SPI \_ GETFOREGROUNDFLASHCOUNT, SPI \_ GETFOREGROUNDLOCKTIMEOUT, SPI \_ SETCARETWIDTH, SPI \_ SETDRAGHEIGHT, SPI \_ SETDRAGWIDTH, SPI \_ SETFOREGROUNDFLASHCOUNT \_ , SPI SETFOREGROUNDLOCKTIMEOUT                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sulle funzionalità di accessibilità di Windows](about-windows-accessibility-features.md)
</dt> </dl>

 

 