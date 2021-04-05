---
title: Cenni preliminari sui movimenti tocco di Windows
description: In questa sezione vengono descritti i vari movimenti supportati da Windows Touch.
ms.assetid: b2fa11a7-9abb-4149-96e3-e8c663c29d4a
keywords:
- Windows Touch, movimenti
- movimenti, informazioni
- Windows Touch, supporto legacy
- movimenti, supporto legacy
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: 2290477aa8b26e937fe6d5f300ed1fea32872f5d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047034"
---
# <a name="windows-touch-gestures-overview"></a>Cenni preliminari sui movimenti tocco di Windows

In questa sezione vengono descritti i vari movimenti supportati da Windows Touch.

## <a name="gestures-overview"></a>Cenni preliminari sui movimenti

Windows Touch consente diversi movimenti che supportano contatti singoli e multipli. Nell'immagine seguente vengono illustrati i vari movimenti supportati in Windows 7.

![illustrazione che mostra i movimenti supportati da Windows Touch in Windows 7](images/gestures.png)

> [!Note]  
> Alcuni riconoscitori sono più affidabili per l'interpretazione dei movimenti con più contatti quando i contatti si distinguono tra loro.

## <a name="legacy-support"></a>Supporto legacy

Per il supporto legacy, il gestore movimenti predefinito esegue il mapping di alcuni movimenti ai messaggi di Windows utilizzati nelle versioni precedenti di Windows. Nella tabella seguente viene illustrata la modalità di mapping dei movimenti ai messaggi legacy.

| Movimento        | Descrizione  | Messaggi generati              |
|----------------|----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| Dettaglio            | Viene eseguito il mapping del movimento della panoramica all'utilizzo della rotellina di scorrimento.                  | **WM_VSCROLL**<br/> **WM_HSCROLL**<br/>       |
| Premere e tenere premuto | Viene eseguito il mapping del gesto premuto per fare clic con il pulsante destro del mouse.     | **WM_RBUTTONDOWN**<br/> **WM_RBUTTONUP**<br/> |
| Zoom           | Il movimento di zoom attiva i messaggi che sono simili a tenere premuto il tasto CTRL e a ruotare la rotellina del mouse per scorrere. | **WM_MOUSEWHEEL** con **MK_CONTROL** impostato in *lParam* |

## <a name="interpreting-windows-touch-gestures"></a>Interpretazione dei movimenti tocco di Windows

I movimenti tocco di Windows possono essere interpretati dagli sviluppatori di applicazioni gestendo il messaggio [**WM_GESTURE**](wm-gesture.md) dalla funzione WndProc di un'applicazione. Dopo la gestione di questo messaggio, è possibile recuperare una struttura [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) che descrive il movimento. La struttura **GESTUREINFO** avrà informazioni assorte che dipendono dal tipo di movimento.

La struttura [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) viene recuperata passando l'handle alla struttura delle informazioni sui movimenti alla funzione [**GetGestureInfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo) .

I flag seguenti indicano i vari stati dei movimenti e vengono archiviati in *dwFlags*. 

| Nome        | Valore      | Descrizione                      |
|-------------|------------|----------------------------------|
| GF_BEGIN   | 0x00000001 | Avvio di un movimento.           |
| GF_INERTIA | 0x00000002 | Un movimento ha attivato un'inerzia. |
| GF_END     | 0x00000004 | Un gesto è terminato.          |

> [!Note]  
> La maggior parte delle applicazioni deve ignorare i **GID_BEGIN** e **GID_END** e passarli a [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca). Questi messaggi vengono utilizzati dal gestore movimenti predefinito. Il comportamento dell'applicazione non è definito quando i messaggi di **GID_BEGIN** e di **GID_END** vengono utilizzati da un'applicazione di terze parti.

Nella tabella seguente vengono indicati i vari identificatori dei movimenti. 

| Nome              | Valore | Descrizione                 |
|-------------------|-------|-----------------------------|
| GID_BEGIN        | 1     | Avvio di un movimento.      |
| GID_END          | 2     | Un movimento sta per terminare.        |
| GID_ZOOM         | 3     | Movimento di zoom.           |
| GID_PAN          | 4     | Movimento di panoramica.            |
| GID_ROTATE       | 5     | Movimento di rotazione.       |
| GID_TWOFINGERTAP | 6     | Gesto di tocco con due dita. |
| GID_PRESSANDTAP  | 7     | Gesto da premere e toccare.  |

> [!Note]  
> Il movimento **GID_PAN** dispone di un'inerzia incorporata. Alla fine di un movimento di panoramica, i messaggi di movimento di panning aggiuntivi vengono creati dal sistema operativo.

I membri della struttura [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) **ptsLocation** e **ullArguments** specificano un punto (usando la struttura **Points** ) e informazioni aggiuntive sui movimenti a seconda del movimento. Nella tabella seguente sono elencati i valori associati a ogni tipo di movimento.

| ID movimento            | *ullArguments*                  | *ptsLocation*                       |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| **GID_ZOOM**         | Indica la distanza tra i due punti.            | Indica il centro dello zoom.   |
| **GID_PAN**          | Indica la distanza tra i due punti.            | Indica la posizione corrente del Pan.                    |
| **GID_ROTATE**       | Indica l'angolo di rotazione se si imposta il flag di **GF_BEGIN** . In caso contrario, si tratta della modifica dell'angolo dall'avvio della rotazione. Questo oggetto è firmato per indicare la direzione della rotazione. Usare le macro [**GID_ROTATE_ANGLE_FROM_ARGUMENT**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_from_argument) e [**GID_ROTATE_ANGLE_TO_ARGUMENT**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_to_argument) per ottenere e impostare il valore dell'angolo. | Indica il centro della rotazione che rappresenta il punto fisso in cui viene ruotato l'oggetto di destinazione. |
| **GID_TWOFINGERTAP** | Indica la distanza tra le due dita.           | Indica il centro delle due dita.                      |
| **GID_PRESSANDTAP**  | Indica il delta tra il primo dito e il secondo dito. Questo valore viene archiviato in una struttura **Point** nei bit 32 inferiori del membro *ullArguments* .                        | Indica la posizione in cui si arresta il primo dito.   |

## <a name="related-topics"></a>Argomenti correlati

[Movimenti tocco di Windows](guide-multi-touch-gestures.md)