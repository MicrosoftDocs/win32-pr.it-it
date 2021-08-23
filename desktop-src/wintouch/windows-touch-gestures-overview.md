---
title: Windows Panoramica dei movimenti tocco
description: Questa sezione descrive i vari movimenti supportati da Windows Touch.
ms.assetid: b2fa11a7-9abb-4149-96e3-e8c663c29d4a
keywords:
- Windows Tocco, movimenti
- movimenti, informazioni
- Windows Tocco, supporto legacy
- movimenti, supporto legacy
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: f2a0f6229afe4ad0d894a1cc2d40489f5d8371de3d7c42cefdccde619119df75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119587256"
---
# <a name="windows-touch-gestures-overview"></a>Windows Panoramica dei movimenti tocco

Questa sezione descrive i vari movimenti supportati da Windows Touch.

## <a name="gestures-overview"></a>Cenni preliminari sui movimenti

Windows Il tocco consente diversi movimenti che supportano singoli e più contatti. L'immagine seguente illustra i vari movimenti supportati in Windows 7.

![illustrazione che mostra i movimenti supportati dal tocco di Windows in Windows 7](images/gestures.png)

> [!Note]  
> Alcuni riconoscitori sono più affidabili nell'interpretazione dei movimenti con più contatti quando i contatti sono più distanti l'uno dall'altro.

## <a name="legacy-support"></a>Supporto legacy

Per il supporto legacy, il gestore movimenti predefinito esegue il mapping di alcuni movimenti Windows messaggi usati nelle versioni precedenti di Windows. La tabella seguente illustra il mapping dei movimenti ai messaggi legacy.

| Movimento        | Descrizione  | Messaggi generati              |
|----------------|----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| Dettaglio            | Il movimento di panoramica viene mappato a usando la rotellina di scorrimento.                  | **WM_VSCROLL**<br/> **WM_HSCROLL**<br/>       |
| Premere e tenere premuto | Il movimento di pressione premuta viene mappato al clic con il pulsante destro del mouse.     | **WM_RBUTTONDOWN**<br/> **WM_RBUTTONUP**<br/> |
| Zoom           | Il movimento di zoom attiva messaggi simili a quando si tiene premuto CTRL e si ruota la rotellina del mouse per scorrere. | **WM_MOUSEWHEEL** con **MK_CONTROL** impostato in *lParam* |

## <a name="interpreting-windows-touch-gestures"></a>Interpretazione dei Windows tocco

Windows I movimenti di tocco possono essere interpretati dagli sviluppatori di applicazioni gestendo il messaggio WM_GESTURE [**dalla**](wm-gesture.md) funzione WndProc di un'applicazione. Dopo la gestione di questo messaggio, è possibile recuperare una [**struttura GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) che descrive il movimento. La **struttura GESTUREINFO** avrà informazioni diverse che dipendono dal tipo di movimento.

La [**struttura GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) viene recuperata passando l'handle alla struttura di informazioni sui movimenti alla [**funzione GetGestureInfo.**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo)

I flag seguenti indicano i vari stati dei movimenti e vengono archiviati in *dwFlags*. 

| Nome        | Valore      | Descrizione                      |
|-------------|------------|----------------------------------|
| GF_BEGIN   | 0x00000001 | È in corso l'avvio di un movimento.           |
| GF_INERTIA | 0x00000002 | Un movimento ha attivato l'inerzia. |
| GF_END     | 0x00000004 | Un movimento è stato completato.          |

> [!Note]  
> La maggior parte delle applicazioni **deve ignorare GID_BEGIN** e **GID_END** e passarli [a DefWindowProc.](/windows/win32/api/winuser/nf-winuser-defwindowproca) Questi messaggi vengono usati dal gestore movimenti predefinito. Il comportamento dell'applicazione non è **definito quando** GID_BEGIN e **GID_END** vengono utilizzati da un'applicazione di terze parti.

La tabella seguente indica i vari identificatori per i movimenti. 

| Nome              | Valore | Descrizione                 |
|-------------------|-------|-----------------------------|
| GID_BEGIN        | 1     | È in corso l'avvio di un movimento.      |
| GID_END          | 2     | Un movimento sta terminando.        |
| GID_ZOOM         | 3     | Movimento di zoom.           |
| GID_PAN          | 4     | Movimento di panoramica.            |
| GID_ROTATE       | 5     | Movimento di rotazione.       |
| GID_TWOFINGERTAP | 6     | Movimento di tocco con due dita. |
| GID_PRESSANDTAP  | 7     | Movimento di pressione e tocco.  |

> [!Note]  
> Il **GID_PAN** ha un'inerzia incorporata. Alla fine di un movimento di panoramica, il sistema operativo crea altri messaggi di movimento di panoramica.

I membri della struttura [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) **ptsLocation** e **ullArguments** specificano un punto (usando la struttura **POINTS)** e informazioni aggiuntive sui movimenti a seconda del movimento. Nella tabella seguente sono elencati i valori associati a ogni tipo di movimento.

| ID movimento            | *ullArguments*                  | *ptsLocation*                       |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| **GID_ZOOM**         | Indica la distanza tra i due punti.            | Indica il centro dello zoom.   |
| **GID_PAN**          | Indica la distanza tra i due punti.            | Indica la posizione corrente della panoramica.                    |
| **GID_ROTATE**       | Indica l'angolo di rotazione se il flag **GF_BEGIN** è impostato. In caso contrario, si tratta della modifica dell'angolo dall'avvio della rotazione. Questo oggetto è firmato per indicare la direzione della rotazione. Usare le [**GID_ROTATE_ANGLE_FROM_ARGUMENT**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_from_argument) e [**GID_ROTATE_ANGLE_TO_ARGUMENT**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_to_argument) macro per ottenere e impostare il valore dell'angolo. | Indica il centro della rotazione, ovvero il punto stazionario intorno al quale è ruotato l'oggetto di destinazione. |
| **GID_TWOFINGERTAP** | Indica la distanza tra le due dita.           | Indica il centro delle due dita.                      |
| **GID_PRESSANDTAP**  | Indica il delta tra il primo dito e il secondo dito. Questo valore viene archiviato in **una struttura POINT** nei 32 bit inferiori del membro *ullArguments.*                        | Indica la posizione in cui si insedia il primo dito.   |

## <a name="related-topics"></a>Argomenti correlati

[Windows Movimenti tocco](guide-multi-touch-gestures.md)