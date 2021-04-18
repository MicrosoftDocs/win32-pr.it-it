---
title: Comunicazione con i dispositivi MCI
description: Comunicazione con i dispositivi MCI
ms.assetid: 2408f8e4-d040-40f5-a880-1ecb8025656c
keywords:
- MCIWndSendString (macro)
- mciSendString (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f7f5458cff0ef4c5c5f84e565fae06ade8796c4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299600"
---
# <a name="communicating-with-mci-devices"></a>Comunicazione con i dispositivi MCI

Il driver di ogni dispositivo MCI gestisce un elenco delle impostazioni e delle funzionalità correnti, quindi può emettere una risposta accurata quando viene eseguita una query per ottenere informazioni.

Quando si vuole comunicare con un dispositivo MCI, è possibile usare le macro e le funzioni di MCIWnd. Molti dei comandi e delle query MCI più comuni sono definiti come macro. Tuttavia, se l'attività che si desidera eseguire non è disponibile come funzione o macro, è possibile inviare i comandi MCI direttamente al driver di dispositivo utilizzando la macro [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) o il form del messaggio o il formato stringa dei comandi MCI. L'uso della macro **MCIWndSendString** equivale all'uso della funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) come indicato di seguito:


```C++
mciSendString(sz, Null, 0, Null) 
```



I parametri di [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) includono solo l'handle di finestra e il formato stringa del comando. Per recuperare le informazioni restituite da un comando stringa, usare la macro [**MCIWndReturnString**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring) .

Per ulteriori informazioni su MCI, vedere [MCI](mci.md).

> [!Note]  
> È necessario escludere l'alias del dispositivo dal comando MCI quando si usa **MCIWndSendString**. La libreria MCIWnd aggiunge questo alias quando invia il comando al dispositivo MCI.

 

 

 