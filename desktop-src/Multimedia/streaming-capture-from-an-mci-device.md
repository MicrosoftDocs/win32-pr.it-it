---
title: Acquisizione di streaming da un dispositivo MCI
description: Acquisizione di streaming da un dispositivo MCI
ms.assetid: 44cbf375-f97e-426a-a703-dfb1b1933138
keywords:
- MCI (Media Control Interface), acquisizione di streaming
- WM_CAP_SET_MCI_DEVICE messaggio
- Macro capSetMCIDeviceName
- WM_CAP_GET_MCI_DEVICE messaggio
- Macro capGetMCIDeviceName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24d469465f47e908bda2512261ea638ad23e931a43cbb0449df676829469c3d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892591"
---
# <a name="streaming-capture-from-an-mci-device"></a>Acquisizione di streaming da un dispositivo MCI

I dispositivi MCI aumentano l'operazione di acquisizione nell'acquisizione in tempo reale e nell'acquisizione dei fotogrammi in passaggi. È possibile specificare il dispositivo MCI, ad esempio un videodisco o un videoregistratore (VCR), che funge da origine video per l'operazione di acquisizione usando il messaggio [**WM \_ CAP SET \_ \_ MCI \_ DEVICE**](wm-cap-set-mci-device.md) (o la macro [**capSetMCIDeviceName)**](/windows/desktop/api/Vfw/nf-vfw-capsetmcidevicename) e specificando il nome del dispositivo. È anche possibile recuperare il nome del dispositivo attualmente impostato usando il messaggio [**WM \_ CAP GET \_ \_ MCI \_ DEVICE**](wm-cap-get-mci-device.md) (o la macro [**capGetMCIDeviceName).**](/windows/desktop/api/Vfw/nf-vfw-capgetmcidevicename)

Nell'acquisizione in tempo reale, la finestra di acquisizione sincronizza l'operazione di acquisizione e compensa i ritardi associati al posizionamento dell'origine video MCI e all'inizializzazione delle risorse (ad esempio i buffer di acquisizione) necessarie per l'acquisizione dei dati. La finestra di acquisizione prevede l'installazione di un dispositivo video MCI valido nel sistema per l'acquisizione dei dati in questo modo.

Le specifiche per il controllo di un dispositivo MCI vengono archiviate nei membri della [**struttura CAPTUREPARMS.**](/windows/win32/api/vfw/ns-vfw-captureparms) Le origini video compatibili con MCI includono vcr edisci. Se il **membro fMCIControl** di questa struttura è impostato su **TRUE,** la finestra di acquisizione coordina l'operazione MCI. La finestra di acquisizione usa i parametri specificati nei membri **dwMCIStartTime** e **dwMCIStopTime** per ottenere le posizioni iniziale e di arresto, in millisecondi, della sequenza. Se il valore di **fMCIControl** è **FALSE,** l'origine video non viene considerata come un dispositivo MCI e i contenuti di **dwMCIStartTime** e **dwMCIStopTime** vengono ignorati.

È possibile usare Media Player per verificare rapidamente che un dispositivo video MCI sia connesso correttamente al sistema. La riproduzione di un dispositivo Media Player verifica che la configurazione mci per il dispositivo sia corretta. Se sullo schermo del video viene visualizzata un'immagine, l'origine video è connessa correttamente all'hardware di acquisizione.

Nell'acquisizione di fotogrammi in passaggi, la finestra di acquisizione sincronizza l'operazione di acquisizione e compensa i ritardi associati al posizionamento dell'origine video MCI e all'inizializzazione delle risorse necessarie per l'acquisizione dei dati. Inoltre, la finestra di acquisizione garantisce che nessun frame sia eliminato. i fotogrammi video vengono elaborati singolarmente, assicurandosi che il fotogramma venga acquisito e archiviato prima di acquisire il fotogramma successivo nel flusso video.

Le specifiche per il controllo dell'acquisizione dei fotogrammi dei passaggi vengono archiviate nei membri della [**struttura CAPTUREPARMS.**](/windows/win32/api/vfw/ns-vfw-captureparms) L'acquisizione di frame di passaggio usa i membri seguenti oltre ai membri usati per l'acquisizione in tempo reale: **fStepMCIDevice**, **fStepCaptureAt2x** e **wStepCaptureAverageFrames**. Se il **membro fStepMCIDevice** è impostato su **TRUE,** la finestra di acquisizione coordina l'acquisizione dei fotogrammi di passaggio. La finestra di acquisizione usa i parametri specificati nei membri **dwMCIStartTime** e **dwMCIStopTime** per le posizioni iniziale e di arresto, in millisecondi, della sequenza. La finestra di acquisizione usa **fStepCaptureAt2x** per determinare se l'hardware di acquisizione deve acquisire fotogrammi video con una risoluzione doppia rispetto alla normale e **usa wStepCaptureAverageFrames** per specificare il numero di volte in cui viene campionato ogni fotogramma nell'operazione di acquisizione.

Se **fStepMCIDevice** è **FALSE,** viene usata l'acquisizione in tempo reale anziché l'acquisizione di fotogrammi passaggio e il contenuto di **fStepCaptureAt2x** e **wStepCaptureAverageFrames** viene ignorato.

Se viene specificata un'acquisizione di fotogrammi passaggio e **fStepCaptureAt2x** è impostato su **TRUE,** l'hardware di acquisizione acquisisce il doppio della risoluzione specificata. Le risoluzioni dell'altezza e della larghezza sono raddoppiati. Il software interpola i pixel nell'immagine con risoluzione superiore per produrre l'immagine con la risoluzione specificata. Questa forma di media può migliorare la definizione dei bordi delle immagini in un frame. È possibile abilitare questa opzione se l'hardware non supporta la compressione basata su hardware e si esegue l'acquisizione in formato RGB.

> [!Note]  
> Se l'hardware supporta la compressione basata su hardware, può acquisire campioni con una frequenza superiore a quella specificata e usare questi esempi aggiuntivi per ottenere definizioni dei colori più coerenti con l'immagine originale. Gli esempi aggiuntivi vengono eliminati dopo essere stati usati e l'hardware passa i campioni al driver di acquisizione alla frequenza specificata.

 

Se viene specificata un'acquisizione di fotogrammi di passaggio, il membro **wStepCaptureAverageFrames** specifica il numero di campionamenti di un frame durante la creazione di un frame in base al campione medio. Questa tecnica di media riduce il rumore di digitalizzazione casuale visualizzato in un fotogramma. Un valore tipico per il numero di medie è 5.

Per altre informazioni su MCI, vedere [MCI.](mci.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Acquisisci varianti](capture-variations.md)
</dt> </dl>

 

 




