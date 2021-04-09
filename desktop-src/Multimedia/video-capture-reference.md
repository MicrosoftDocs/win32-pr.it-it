---
title: Informazioni di riferimento sull'acquisizione video
description: Informazioni di riferimento sull'acquisizione video
ms.assetid: 5356c575-2a59-4459-b4eb-76967deb6877
keywords:
- Video per Windows (VFW), Guida di riferimento all'acquisizione video
- VFW (video per Windows), Guida di riferimento all'acquisizione video
- AVICap, riferimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cef19834e244f6070a1d8bb3383dcac017e4d161
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044312"
---
# <a name="video-capture-reference"></a>Informazioni di riferimento sull'acquisizione video

In questa sezione vengono descritte le funzioni, le strutture, i messaggi e le macro associati alla classe della finestra AVICap. Questi elementi vengono raggruppati come indicato di seguito.

## <a name="basic-capture-operations"></a>Operazioni di acquisizione di base

-   [**capCreateCaptureWindow**](/windows/desktop/api/Vfw/nf-vfw-capcreatecapturewindowa)
-   [**interruzione di WM \_ Cap \_**](wm-cap-abort.md)
-   [**\_ \_ connessione driver WM \_ Cap**](wm-cap-driver-connect.md)
-   [**\_sequenza Cap \_ WM**](wm-cap-sequence.md)
-   [**arresto di WM \_ Cap \_**](wm-cap-stop.md)

## <a name="capture-windows"></a>Acquisisci Windows

-   [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus)
-   [**capGetDriverDescription**](/windows/desktop/api/Vfw/nf-vfw-capgetdriverdescriptiona)
-   [**\_ \_ connessione driver WM \_ Cap**](wm-cap-driver-connect.md)
-   [**\_disconnessione \_ driver WM Cap \_**](wm-cap-driver-disconnect.md)
-   [**\_stato di \_ get \_ Cap WM**](wm-cap-get-status.md)

## <a name="capture-drivers"></a>Driver di acquisizione

-   [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps)
-   [**\_ \_ \_ Caps Get driver \_ WM**](wm-cap-driver-get-caps.md)
-   [**\_ \_ \_ nome Get driver WM \_ Cap**](wm-cap-driver-get-name.md)
-   [**\_versione del \_ driver WM Cap \_ \_**](wm-cap-driver-get-version.md)
-   [**WM \_ Cap \_ get \_ AUDIOFORMAT**](wm-cap-get-audioformat.md)
-   [**WM \_ Cap \_ get \_ VIDEOFORMAT**](wm-cap-get-videoformat.md)
-   [**\_set di estremità WM \_ \_ AUDIOFORMAT**](wm-cap-set-audioformat.md)
-   [**\_set di estremità WM \_ \_ VIDEOFORMAT**](wm-cap-set-videoformat.md)

## <a name="capture-driver-preview-and-overlay-modes"></a>Modalità anteprima e sovrapposizione driver di acquisizione

-   [**\_ \_ sovrimpressione set Cap WM \_**](wm-cap-set-overlay.md)
-   [**\_ \_ Anteprima set WM \_ Cap**](wm-cap-set-preview.md)
-   [**\_set di estremità WM \_ \_ PREVIEWRATE**](wm-cap-set-previewrate.md)
-   [**\_scala del \_ set di estremità WM \_**](wm-cap-set-scale.md)
-   [**\_scorrimento del \_ set di estremità WM \_**](wm-cap-set-scroll.md)

## <a name="capture-driver-video-dialog-boxes"></a>Finestre di dialogo di acquisizione del video del driver

-   [**VIDEOCOMPRESSION di WM \_ Cap \_ DLG \_**](wm-cap-dlg-videocompression.md)
-   [**VIDEODISPLAY di WM \_ Cap \_ DLG \_**](wm-cap-dlg-videodisplay.md)
-   [**VIDEOFORMAT di WM \_ Cap \_ DLG \_**](wm-cap-dlg-videoformat.md)
-   [**VIDEOSOURCE di WM \_ Cap \_ DLG \_**](wm-cap-dlg-videosource.md)

## <a name="audio-format"></a>Formato audio

-   [**WM \_ Cap \_ get \_ AUDIOFORMAT**](wm-cap-get-audioformat.md)
-   [**\_set di estremità WM \_ \_ AUDIOFORMAT**](wm-cap-set-audioformat.md)

## <a name="video-capture-settings"></a>Impostazioni acquisizione video

-   [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms)
-   [**\_configurazione della sequenza WM Cap \_ get \_ \_**](wm-cap-get-sequence-setup.md)
-   [**\_configurazione della \_ sequenza di set \_ \_ di WM Cap**](wm-cap-set-sequence-setup.md)

## <a name="capture-file-and-buffers"></a>Acquisisci file e buffer

-   [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms)
-   [**\_ \_ ALLOCA file WM \_ Cap**](wm-cap-file-allocate.md)
-   [**file \_ di \_ \_ acquisizione Get \_ file \_ di WM Cap**](wm-cap-file-get-capture-file.md)
-   [**\_ \_ SaveAs file di WM Cap \_**](wm-cap-file-saveas.md)
-   [**\_file di \_ acquisizione del set di file WM Cap \_ \_ \_**](wm-cap-file-set-capture-file.md)

## <a name="directly-using-capture-data"></a>Usando direttamente i dati di acquisizione

-   [**\_sequenza Cap \_ WM \_ nofile**](wm-cap-sequence-nofile.md)

## <a name="capture-from-mci-device"></a>Acquisisci dal dispositivo MCI

-   [**SET di WM \_ Cap \_ set \_ MCI \_**](wm-cap-set-mci-device.md)

## <a name="manual-frame-capture"></a>Acquisizione frame manuale

-   [**\_ \_ singolo frame WM \_ Cap**](wm-cap-single-frame.md)
-   [**\_ \_ \_ chiusura singolo frame \_ WM Cap**](wm-cap-single-frame-close.md)
-   [**\_apertura del \_ singolo \_ frame WM Cap \_**](wm-cap-single-frame-open.md)

## <a name="still-image-capture"></a>Acquisizione di Still-Image

-   [**copia di modifica di WM \_ Cap \_ \_**](wm-cap-edit-copy.md)
-   [**\_ \_ SAVEDIB file WM \_ Cap**](wm-cap-file-savedib.md)
-   [**\_frame di \_ cattura WM Cap \_**](wm-cap-grab-frame.md)
-   [**\_NOSTOP \_ frame di cattura WM Cap \_ \_**](wm-cap-grab-frame-nostop.md)

## <a name="advanced-capture-options"></a>Opzioni di acquisizione avanzate

-   [**\_set di \_ file WM Cap \_ \_ INFOCHUNK**](wm-cap-file-set-infochunk.md)
-   [**WM \_ Cap \_ ottenere \_ \_ i dati utente**](wm-cap-get-user-data.md)
-   [**\_set di \_ \_ dati utente \_ di WM Cap**](wm-cap-set-user-data.md)

## <a name="working-with-palettes"></a>Utilizzo delle tavolozze

-   [**copia di modifica di WM \_ Cap \_ \_**](wm-cap-edit-copy.md)
-   [**CREAZIONE di un PAL di WM \_ Cap \_ \_**](wm-cap-pal-autocreate.md)
-   [**WM \_ Cap \_ PAL \_ MANUALCREATE**](wm-cap-pal-manualcreate.md)
-   [**PAL di WM \_ Cap \_ \_ aperto**](wm-cap-pal-open.md)
-   [**di WM \_ Cap \_ PAL \_ Incolla**](wm-cap-pal-paste.md)
-   [**\_ \_ salvataggio PAL WM \_ Cap**](wm-cap-pal-save.md)

## <a name="yielding-to-other-applications"></a>Cedendo ad altre applicazioni

-   [**\_configurazione della sequenza WM Cap \_ get \_ \_**](wm-cap-get-sequence-setup.md)
-   [**\_rendimento di \_ \_ callback set di estremità \_ WM**](wm-cap-set-callback-yield.md)
-   [**\_configurazione della \_ sequenza di set \_ \_ di WM Cap**](wm-cap-set-sequence-setup.md)

## <a name="avicap-callback-functions"></a>Funzioni di callback AVICap

-   [**capControlCallback**](/windows/desktop/api/Vfw/nc-vfw-capcontrolcallback)
-   [**capErrorCallback**](/windows/desktop/api/Vfw/nc-vfw-caperrorcallbacka)
-   [**capStatusCallback**](/windows/desktop/api/Vfw/nc-vfw-capstatuscallbacka)
-   [**capVideoStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback)
-   [**capWaveStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capwavecallback)
-   [**capYieldCallback**](/windows/desktop/api/Vfw/nc-vfw-capyieldcallback)
-   [**\_CAPCONTROL di \_ \_ callback set di estremità \_ WM**](wm-cap-set-callback-capcontrol.md)
-   [**\_errore di \_ callback del set di estremità WM \_ \_**](wm-cap-set-callback-error.md)
-   [**\_frame di \_ \_ callback \_ per set di estremità WM**](wm-cap-set-callback-frame.md)
-   [**\_stato di \_ callback per set di estremità WM \_ \_**](wm-cap-set-callback-status.md)
-   [**\_VIDEOSTREAM di \_ \_ callback set di estremità \_ WM**](wm-cap-set-callback-videostream.md)
-   [**\_WAVESTREAM di \_ \_ callback set di estremità \_ WM**](wm-cap-set-callback-wavestream.md)
-   [**\_rendimento di \_ \_ callback set di estremità \_ WM**](wm-cap-set-callback-yield.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Acquisizione video](video-capture.md)
</dt> </dl>

 

 




