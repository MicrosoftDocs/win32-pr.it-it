---
title: Comunicazione con i dispositivi MCI
description: Comunicazione con i dispositivi MCI
ms.assetid: 2408f8e4-d040-40f5-a880-1ecb8025656c
keywords:
- Macro MCIWndSendString
- Funzione mciSendString
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3def53cda9374ba50dfea8252918f073d961410092a977c8779f3a29d6b36204
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807841"
---
# <a name="communicating-with-mci-devices"></a>Comunicazione con i dispositivi MCI

Il driver di ogni dispositivo MCI gestisce un elenco delle impostazioni e delle funzionalità correnti, in modo che possa emettere una risposta accurata quando viene eseguita una query per ottenere informazioni.

Quando si vuole comunicare con un dispositivo MCI, è possibile usare macro e funzioni MCIWnd. Molti dei comandi e delle query MCI più comuni sono definiti come macro. Tuttavia, se l'attività da eseguire non è disponibile come funzione o macro, è possibile inviare comandi MCI direttamente al driver di dispositivo usando la macro [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) o usando il modulo del messaggio o la forma stringa dei comandi MCI. L'uso della macro **MCIWndSendString** equivale all'uso della [**funzione mciSendString**](/previous-versions//dd757161(v=vs.85)) come indicato di seguito:


```C++
mciSendString(sz, Null, 0, Null) 
```



I parametri di [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) includono solo l'handle della finestra e il formato stringa del comando. Per recuperare le informazioni restituite da un comando stringa, usare la macro [**MCIWndReturnString.**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring)

Per altre informazioni su MCI, vedere [MCI](mci.md).

> [!Note]  
> È necessario escludere l'alias di dispositivo dal comando MCI quando si usa **MCIWndSendString**. La libreria MCIWnd aggiunge questo alias quando invia il comando al dispositivo MCI.

 

 

 