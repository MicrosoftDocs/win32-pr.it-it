---
title: Informazioni di riferimento su Acquisizione video
description: Informazioni di riferimento su Acquisizione video
ms.assetid: 5356c575-2a59-4459-b4eb-76967deb6877
keywords:
- Video per Windows (VFW), informazioni di riferimento per l'acquisizione di video
- VFW (Video per Windows),informazioni di riferimento per l'acquisizione di video
- AVICap, informazioni di riferimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 166bdcf06e700023a197334b0e63f612398485affe21dc9ffbc6e7ac0800926a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119804311"
---
# <a name="video-capture-reference"></a>Informazioni di riferimento su Acquisizione video

Questa sezione descrive le funzioni, le strutture, i messaggi e le macro associate alla classe della finestra AVICap. Questi elementi sono raggruppati nel modo seguente.

## <a name="basic-capture-operations"></a>Operazioni di acquisizione di base

-   [**capCreateCaptureWindow**](/windows/desktop/api/Vfw/nf-vfw-capcreatecapturewindowa)
-   [**WM \_ CAP \_ ABORT**](wm-cap-abort.md)
-   [**WM \_ CAP \_ DRIVER \_ CONNECT**](wm-cap-driver-connect.md)
-   [**SEQUENZA \_ CAP \_ WM**](wm-cap-sequence.md)
-   [**WM \_ CAP \_ STOP**](wm-cap-stop.md)

## <a name="capture-windows"></a>Acquisisci Windows

-   [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus)
-   [**capGetDriverDescription**](/windows/desktop/api/Vfw/nf-vfw-capgetdriverdescriptiona)
-   [**WM \_ CAP \_ DRIVER \_ CONNECT**](wm-cap-driver-connect.md)
-   [**DISCONNESSIONE \_ \_ DEL DRIVER CAP WM \_**](wm-cap-driver-disconnect.md)
-   [**WM \_ CAP \_ GET \_ STATUS**](wm-cap-get-status.md)

## <a name="capture-drivers"></a>Acquisisci driver

-   [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps)
-   [**WM \_ CAP \_ DRIVER \_ GET \_ CAPS**](wm-cap-driver-get-caps.md)
-   [**NOME \_ GET \_ DRIVER \_ CAP \_ WM**](wm-cap-driver-get-name.md)
-   [**OTTENERE \_ LA VERSIONE DEL DRIVER \_ \_ CAP \_ WM**](wm-cap-driver-get-version.md)
-   [**WM \_ CAP \_ GET \_ AUDIOFORMAT**](wm-cap-get-audioformat.md)
-   [**WM \_ CAP \_ GET \_ VIDEOFORMAT**](wm-cap-get-videoformat.md)
-   [**WM \_ CAP \_ SET \_ AUDIOFORMAT**](wm-cap-set-audioformat.md)
-   [**WM \_ CAP \_ SET \_ VIDEOFORMAT**](wm-cap-set-videoformat.md)

## <a name="capture-driver-preview-and-overlay-modes"></a>Modalità di anteprima del driver di acquisizione e sovrimpressione

-   [**\_SOVRIMPRESSIONE \_ SET DI ESTREMITÀ WM \_**](wm-cap-set-overlay.md)
-   [**WM \_ CAP \_ SET \_ PREVIEW**](wm-cap-set-preview.md)
-   [**WM \_ CAP \_ SET \_ PREVIEWRATE**](wm-cap-set-previewrate.md)
-   [**WM \_ CAP \_ SET \_ SCALE**](wm-cap-set-scale.md)
-   [**WM \_ CAP \_ SET \_ SCROLL**](wm-cap-set-scroll.md)

## <a name="capture-driver-video-dialog-boxes"></a>Finestre di dialogo per l'acquisizione di video dei driver

-   [**WM \_ CAP \_ DLG \_ VIDEOCOMPRESSION**](wm-cap-dlg-videocompression.md)
-   [**WM \_ CAP \_ DLG \_ VIDEODISPLAY**](wm-cap-dlg-videodisplay.md)
-   [**WM \_ CAP \_ DLG \_ VIDEOFORMAT**](wm-cap-dlg-videoformat.md)
-   [**WM \_ CAP \_ DLG \_ VIDEOSOURCE**](wm-cap-dlg-videosource.md)

## <a name="audio-format"></a>Formato audio

-   [**WM \_ CAP \_ GET \_ AUDIOFORMAT**](wm-cap-get-audioformat.md)
-   [**WM \_ CAP \_ SET \_ AUDIOFORMAT**](wm-cap-set-audioformat.md)

## <a name="video-capture-settings"></a>Video Capture Impostazioni

-   [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms)
-   [**WM \_ CAP \_ GET \_ SEQUENCE \_ SETUP**](wm-cap-get-sequence-setup.md)
-   [**WM \_ CAP \_ SET \_ SEQUENCE \_ SETUP**](wm-cap-set-sequence-setup.md)

## <a name="capture-file-and-buffers"></a>Acquisisci file e buffer

-   [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms)
-   [**WM \_ CAP \_ FILE \_ ALLOCATE**](wm-cap-file-allocate.md)
-   [**FILE CAP WM \_ - OTTENERE IL FILE DI \_ \_ \_ \_ ACQUISIZIONE**](wm-cap-file-get-capture-file.md)
-   [**SALVATAGGIO \_ FILE CAP \_ \_ WMAS**](wm-cap-file-saveas.md)
-   [**FILE DI ACQUISIZIONE SET DI FILE WM \_ CAP \_ \_ \_ \_**](wm-cap-file-set-capture-file.md)

## <a name="directly-using-capture-data"></a>Uso diretto dei dati di acquisizione

-   [**WM \_ CAP \_ SEQUENCE \_ NOFILE**](wm-cap-sequence-nofile.md)

## <a name="capture-from-mci-device"></a>Acquisire da un dispositivo MCI

-   [**WM \_ CAP \_ SET \_ MCI \_ DEVICE**](wm-cap-set-mci-device.md)

## <a name="manual-frame-capture"></a>Acquisizione manuale dei frame

-   [**FRAME SINGOLO CAP WM \_ \_ \_**](wm-cap-single-frame.md)
-   [**CHIUSURA \_ FRAME \_ SINGOLO CAP \_ \_ WM**](wm-cap-single-frame-close.md)
-   [**WM \_ CAP \_ SINGLE \_ FRAME \_ OPEN**](wm-cap-single-frame-open.md)

## <a name="still-image-capture"></a>Still-Image capture

-   [**WM \_ CAP \_ EDIT \_ COPY**](wm-cap-edit-copy.md)
-   [**FILE CAP WM \_ \_ \_ SALVATOIB**](wm-cap-file-savedib.md)
-   [**WM \_ CAP \_ GRAB \_ FRAME**](wm-cap-grab-frame.md)
-   [**WM \_ CAP \_ GRAB \_ FRAME \_ NOSTOP**](wm-cap-grab-frame-nostop.md)

## <a name="advanced-capture-options"></a>Opzioni di acquisizione avanzate

-   [**WM \_ CAP \_ FILE \_ SET \_ INFOCHUNK**](wm-cap-file-set-infochunk.md)
-   [**WM \_ CAP \_ GET \_ USER \_ DATA**](wm-cap-get-user-data.md)
-   [**WM \_ CAP \_ SET \_ USER \_ DATA**](wm-cap-set-user-data.md)

## <a name="working-with-palettes"></a>Uso delle tavolozze

-   [**WM \_ CAP \_ EDIT \_ COPY**](wm-cap-edit-copy.md)
-   [**WM \_ CAP \_ PAL \_ AUTOCREATE**](wm-cap-pal-autocreate.md)
-   [**WM \_ CAP \_ PAL \_ MANUALCREATE**](wm-cap-pal-manualcreate.md)
-   [**WM \_ CAP \_ PAL \_ OPEN**](wm-cap-pal-open.md)
-   [**WM \_ CAP \_ PAL \_ PASTE**](wm-cap-pal-paste.md)
-   [**WM \_ CAP \_ PAL \_ SAVE**](wm-cap-pal-save.md)

## <a name="yielding-to-other-applications"></a>Cede ad altre applicazioni

-   [**WM \_ CAP \_ GET \_ SEQUENCE \_ SETUP**](wm-cap-get-sequence-setup.md)
-   [**WM \_ CAP \_ SET \_ CALLBACK \_ YIELD**](wm-cap-set-callback-yield.md)
-   [**WM \_ CAP \_ SET \_ SEQUENCE \_ SETUP**](wm-cap-set-sequence-setup.md)

## <a name="avicap-callback-functions"></a>Funzioni di callback AVICap

-   [**capControlCallback**](/windows/desktop/api/Vfw/nc-vfw-capcontrolcallback)
-   [**capErrorCallback**](/windows/desktop/api/Vfw/nc-vfw-caperrorcallbacka)
-   [**capStatusCallback**](/windows/desktop/api/Vfw/nc-vfw-capstatuscallbacka)
-   [**capVideoStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback)
-   [**capWaveStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capwavecallback)
-   [**capYieldCallback**](/windows/desktop/api/Vfw/nc-vfw-capyieldcallback)
-   [**WM \_ CAP \_ SET \_ CALLBACK \_ CAPCONTROL**](wm-cap-set-callback-capcontrol.md)
-   [**ERRORE DI \_ CALLBACK WM CAP \_ SET \_ \_**](wm-cap-set-callback-error.md)
-   [**FRAME DI \_ CALLBACK WM CAP \_ SET \_ \_**](wm-cap-set-callback-frame.md)
-   [**WM \_ CAP \_ SET \_ CALLBACK \_ STATUS**](wm-cap-set-callback-status.md)
-   [**WM \_ CAP \_ SET \_ CALLBACK \_ VIDEOSTREAM**](wm-cap-set-callback-videostream.md)
-   [**WM \_ CAP \_ SET \_ CALLBACK \_ WAVESTREAM**](wm-cap-set-callback-wavestream.md)
-   [**WM \_ CAP \_ SET \_ CALLBACK \_ YIELD**](wm-cap-set-callback-yield.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Acquisizione video](video-capture.md)
</dt> </dl>

 

 




