---
title: Parametri di accessibilità
description: Il sistema gestisce un set di parametri di accessibilità che indicano se l'utente ha esigenze o preferenze speciali che richiedono alle applicazioni di modificare il comportamento predefinito.
ms.assetid: efa289bb-5965-4002-93df-116ab2621efc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a289162366f5d69c501ffbea55108167324c11a1c865184105afd587f36bcfd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118327789"
---
# <a name="accessibility-parameters"></a>Parametri di accessibilità

Il sistema gestisce un set di parametri di accessibilità che indicano se l'utente ha esigenze o preferenze speciali che richiedono alle applicazioni di modificare il comportamento predefinito. L'utente controlla lo stato di questi parametri, in genere usando Centro accessibilità in Pannello di controllo. Pannello di controllo applicazioni o altri programmi che consentono all'utente di personalizzare l'ambiente possono usare la [**funzione SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) per impostare i parametri di accessibilità.

Se un utente modifica questi parametri, il Pannello di controllo invia il [**messaggio WM \_ SETTINGCHANGE.**](/windows/desktop/winmsg/wm-settingchange) Le applicazioni devono rispondere a questo messaggio e [**usare SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) per determinare lo stato dei parametri di accessibilità. Quando un parametro di accessibilità è abilitato, l'applicazione deve modificare l'interfaccia utente, se necessario, per soddisfare le preferenze dell'utente.

Windows supporta i parametri di accessibilità seguenti.



| Parametro                                                                    | Descrizione                                                                                                                                                                    |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [High contrast](high-contrast-parameter.md)                                 | Indica che le applicazioni devono offrire un contrasto elevato tra gli oggetti visivi in primo piano e in background.                                                                            |
| [Preferenza della tastiera](keyboard-preference-parameter.md)                     | Indica che le applicazioni devono visualizzare le interfacce della tastiera che altrimenti verrebbero nascoste.                                                                                 |
| [Utilità per la lettura dello schermo](screen-reader-parameter.md)                                 | Indica che le applicazioni devono fornire informazioni testuali in situazioni in cui altrimenti presenterebbero le informazioni graficamente.                                     |
| [Mostra suoni (e flag di descrizione audio)](showsounds-parameter.md) | Indica che le applicazioni devono anche fornire un avviso visivo o un segnale acustico quando usa il suono per trasmettere informazioni importanti o fornire una descrizione audio per gli elementi visivi. |
| [Animazione dell'area client](client-area-animation.md)                           | Indica che le applicazioni devono rispettare le preferenze dell'utente per la visualizzazione dell'animazione nell'area client.                                                                       |
| [Durata del messaggio](message-duration.md)                                     | Indica che le applicazioni che forniscono notifiche popup devono monitorare i flag sulla durata dei messaggi e modificarne la lunghezza.                                  |



 

I parametri di sistema seguenti sono utili per le applicazioni di accessibilità. Per altre informazioni, vedere [**Funzione SystemParametersInfo.**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)



| Gruppo di parametri      | Parametro                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Parametri del desktop   | SPI \_ GETWORKAREA, SPI \_ SETWORKAREA                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Parametri di input     | SPI \_ GETKEYBOARDCUES, SPI \_ GETKEYBOARDDELAY, SPI \_ GETKEYBOARDPREF, SPI \_ GETKEYBOARDSPEED, SPI \_ GETMESSAGEDURATION, SPI \_ GETMOUSE, SPI \_ GETMOUSEHOVERHEIGHT, SPI \_ GETMOUSEHOVERTIME, SPI \_ GETMOUSEHOVERWIDTH, SPI \_ GETMOUSESPEED, SPI \_ GETMOUSETRAILS, SPI \_ GETSNAPTODEFBUTTON, SPI \_ GETWHEELSCROLLLINES, SPI \_ SETDOUBLECLICKTIME, SPI \_ SETDOUBLECLKHEIGHT, SPI \_ SETDOUBLECLKWIDTH, SPI \_ SETKEYBOARDCUES, SPI \_ SETKEYBOARDDELAY, SPI \_ SETKEYBOARDPREF, SPI \_ SETKEYBOARDSPEED, SPI \_ SETMOUSE, SPI \_ SETMOUSEHOVERHEIGHT, SPI \_ SETMOUSEHOVERTIME, SPI \_ SETMOUSEHOVERWIDTH, SPI \_ SETMOUSESPEED, SPI \_ SETMOUSETRAILS, SPI \_ SETSNAPTODEFBUTTON, SPI \_ SETWHEELSCROLLLINES |
| Parametri degli effetti dell'interfaccia utente | SPI \_ GETMENUUNDERLINES, SPI \_ SETMENUUNDERLINES                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Parametri della finestra    | SPI \_ GETCARETWIDTH, SPI \_ GETFOREGROUNDFLASHCOUNT, SPI \_ GETFOREGROUNDLOCKTIMEOUT, SPI \_ SETCARETWIDTH, SPI \_ SETDRAGHEIGHT, SPI \_ SETDRAGWIDTH, SPI \_ SETFOREGROUNDFLASHCOUNT, SPI \_ SETFOREGROUNDLOCKTIMEOUT                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sulle Windows di accessibilità](about-windows-accessibility-features.md)
</dt> </dl>

 

 