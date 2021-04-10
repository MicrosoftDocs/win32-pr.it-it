---
title: Uso di una finestra o di un thread per elaborare i messaggi dei driver
description: Uso di una finestra o di un thread per elaborare i messaggi dei driver
ms.assetid: 7a9eaaa1-d3b0-400e-8fbf-ee5fe59efc32
keywords:
- audio Waveform, callback finestra
- blocchi di dati audio, callback della finestra
- audio Waveform, callback di thread
- blocchi di dati audio, callback di thread
- audio Waveform, elaborazione dei messaggi del driver
- blocchi di dati audio, elaborazione dei messaggi del driver
- elaborazione dei messaggi del driver
- waveInOpen (funzione)
- waveOutOpen (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a147bd86b3c8045456ef9961039f645fd4023f13
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103963077"
---
# <a name="using-a-window-or-thread-to-process-driver-messages"></a>Uso di una finestra o di un thread per elaborare i messaggi dei driver

Per usare una funzione di callback della finestra, specificare il \_ flag della finestra di callback nel parametro *fdwOpen* e un handle di finestra nella parola di ordine inferiore del parametro *dwCallback* della funzione [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) o [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) . I messaggi del driver verranno inviati alla routine della finestra per la finestra identificata dall'handle in *dwCallback*.

Analogamente, per usare un callback del thread, specificare \_ il thread di callback e un handle di thread nella chiamata a **waveInOpen** o **waveOutOpen**. In questo caso, i messaggi vengono inviati al thread specificato anziché a una finestra.

I messaggi inviati al callback della finestra o del thread sono specifici del tipo di dispositivo audio usato. Per ulteriori informazioni su questi messaggi, vedere la pagina relativa alla [riproduzione di file di Waveform-Audio](playing-waveform-audio-files.md).

 

 