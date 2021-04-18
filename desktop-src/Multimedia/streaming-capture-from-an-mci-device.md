---
title: Acquisizione di flussi da un dispositivo MCI
description: Acquisizione di flussi da un dispositivo MCI
ms.assetid: 44cbf375-f97e-426a-a703-dfb1b1933138
keywords:
- MCI (Media Control Interface), acquisizione di flussi
- Messaggio WM_CAP_SET_MCI_DEVICE
- capSetMCIDeviceName (macro)
- Messaggio WM_CAP_GET_MCI_DEVICE
- capGetMCIDeviceName (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab8cf358a87a812024328abf7fc1aae0509a126f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515976"
---
# <a name="streaming-capture-from-an-mci-device"></a>Acquisizione di flussi da un dispositivo MCI

I dispositivi MCI potenziano l'operazione di acquisizione in acquisizione in tempo reale e acquisizione frame. È possibile specificare il dispositivo MCI, ad esempio videodisco o videoregistratore (VCR), che funge da origine video per l'operazione di acquisizione usando il [**\_ dispositivo WM Cap \_ set \_ MCI \_**](wm-cap-set-mci-device.md) (o la macro [**capSetMCIDeviceName**](/windows/desktop/api/Vfw/nf-vfw-capsetmcidevicename) ) e specificando il nome del dispositivo. È anche possibile recuperare il nome del dispositivo attualmente impostato usando il messaggio [**WM \_ Cap \_ get \_ MCI \_ Device**](wm-cap-get-mci-device.md) (o la macro [**capGetMCIDeviceName**](/windows/desktop/api/Vfw/nf-vfw-capgetmcidevicename) ).

Nell'acquisizione in tempo reale la finestra di acquisizione sincronizza l'operazione di acquisizione e compensa i ritardi associati al posizionamento dell'origine video MCI e l'inizializzazione delle risorse, ad esempio i buffer di acquisizione, necessarie per l'acquisizione dei dati. La finestra di acquisizione prevede l'installazione di un dispositivo video MCI valido nel sistema per l'acquisizione dei dati in questo modo.

Le specifiche per il controllo di un dispositivo MCI sono archiviate nei membri della struttura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) . Le origini video compatibili con MCI includono VCR e Laserdisc. Se il membro **fMCIControl** della struttura è impostato su **true**, la finestra di acquisizione coordina l'operazione MCI. La finestra di acquisizione usa i parametri specificati nei membri **dwMCIStartTime** e **dwMCIStopTime** per ottenere le posizioni di avvio e arresto, in millisecondi, della sequenza. Se il valore di **fMCIControl** è **false**, l'origine video non viene considerata come un dispositivo MCI e il contenuto di **dwMCIStartTime** e **dwMCIStopTime** viene ignorato.

È possibile utilizzare Media Player per verificare rapidamente che un dispositivo video MCI sia connesso correttamente al sistema. La riproduzione di un dispositivo con Media Player verifica che la configurazione di MCI per il dispositivo sia corretta. Se viene visualizzata un'immagine sullo schermo video, l'origine video è connessa correttamente all'hardware di acquisizione.

In Step-Frame Capture la finestra di acquisizione sincronizza l'operazione di acquisizione e compensa i ritardi associati al posizionamento dell'origine video MCI e l'inizializzazione delle risorse necessarie per l'acquisizione dei dati. Inoltre, la finestra di acquisizione garantisce che non vengano eliminati frame; scorre i frame video singolarmente, assicurando che il frame venga acquisito e archiviato prima di acquisire il frame successivo nel flusso video.

Le specifiche per il controllo dell'acquisizione di frame Step sono archiviate nei membri della struttura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) . L'acquisizione con frame Step USA i membri seguenti oltre ai membri usati per l'acquisizione in tempo reale: **fStepMCIDevice**, **fStepCaptureAt2x** e **wStepCaptureAverageFrames**. Se il membro **fStepMCIDevice** è impostato su **true**, la finestra di acquisizione coordina il passaggio Frame Capture. La finestra di acquisizione usa i parametri specificati nei membri **dwMCIStartTime** e **dwMCIStopTime** per le posizioni di avvio e arresto, in millisecondi, della sequenza. La finestra di acquisizione USA **fStepCaptureAt2x** per determinare se l'hardware di acquisizione deve acquisire i fotogrammi video con una doppia risoluzione normale e USA **wStepCaptureAverageFrames** per specificare il numero di volte in cui viene campionato ogni frame nell'operazione di acquisizione.

Se **fStepMCIDevice** è **false**, viene utilizzata l'acquisizione in tempo reale al posto di Step-Frame Capture e il contenuto di **fStepCaptureAt2x** e **wStepCaptureAverageFrames** vengono ignorati.

Se viene specificata un'acquisizione con frame Step e **fStepCaptureAt2x** è impostato su **true**, l'hardware di acquisizione acquisisce il doppio della risoluzione specificata. (Le risoluzioni dell'altezza e della larghezza sono raddoppiate). Il software esegue l'interpolazione dei pixel nell'immagine di risoluzione superiore per produrre l'immagine in corrispondenza della risoluzione specificata. Questa forma di media può migliorare la definizione perimetrale delle immagini in un frame. È possibile abilitare questa opzione se l'hardware non supporta la decimazione basata su hardware e si sta acquisendo in formato RGB.

> [!Note]  
> Se l'hardware supporta la decimazione basata su hardware, può acquisire campioni a una velocità superiore rispetto a quanto specificato e usare questi esempi aggiuntivi per ottenere le definizioni dei colori più coerenti con l'immagine originale. Gli esempi aggiuntivi vengono eliminati dopo essere stati usati e l'hardware passa gli esempi al driver di acquisizione alla velocità specificata.

 

Se viene specificata un'acquisizione con frame Step, il membro **wStepCaptureAverageFrames** specifica il numero di volte in cui un frame viene campionato durante la creazione di un frame basato sull'esempio medio. Questa tecnica di media riduzione riduce il rumore di digitalizzazione casuale visualizzato in un frame. Un valore tipico per il numero di medie è 5.

Per ulteriori informazioni su MCI, vedere [MCI](mci.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Variazioni di acquisizione](capture-variations.md)
</dt> </dl>

 

 




