---
description: Una libreria Umbrella è una singola libreria a collegamento statico che esporta un subset di API Win32. Ad esempio, una lib di Umbrella denominata OneCore. lib fornisce le esportazioni per il subset di API Win32 comuni a tutti i dispositivi Windows 10.
ms.assetid: A323B5D1-3235-4BBA-96BF-A7DFEBB85C89
title: Librerie generiche di Windows
ms.topic: article
ms.date: 10/14/2020
ms.openlocfilehash: 86a8f9b8f3bef5081bd7e0e64300b9295fd85401
ms.sourcegitcommit: 0c786b1682063d0cae0fc43180945183fa2c7981
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/24/2020
ms.locfileid: "103734783"
---
# <a name="windows-umbrella-libraries"></a>Librerie generiche di Windows

Una *libreria Umbrella* è una singola libreria a collegamento statico che esporta un subset di API Win32. Ad esempio, una libreria Umbrella denominata **OneCore. lib** fornisce le esportazioni per il subset di API Win32 comuni a tutti i dispositivi Windows 10.

Le API in una libreria Umbrella possono essere implementate in un'ampia gamma di moduli, sia che si tratti di un [set di API](windows-apisets.md) o di una dll, ma la libreria Umbrella astrarre i dettagli dall'utente, rendendo l'app più portabile tra le versioni del sistema operativo. È sufficiente collegare l'app desktop o il driver alla libreria Umbrella che contiene il set di API a cui si è interessati ed è sufficiente eseguire questa operazione. 

| Libreria | Descrizione |
|------------------------|-------------------------|
| OneCore. lib | Questa libreria fornisce le esportazioni per il subset di API Win32 comuni a tutti i dispositivi Windows 10. Collegare l'app desktop o il driver con OneCore. lib (e nessuna altra libreria) per accedere alle API. Se si collega l'app o il driver a OneCore. lib e si chiamano solo le API Win32 in tale libreria, l'app o il driver si caricherà correttamente in tutti i dispositivi Windows 10.         |
| OneCore_apiset. lib | Questa libreria fornisce lo stesso code coverage di OneCore. lib, ma usa l' [invio diretto del set di API](api-set-loader-operation.md#direct-forwarding). Si noti che l'uso di questa libreria è compatibile solo con la versione di Windows 10, come specificato dall'SDK versione di destinazione o superiore.  |
| OneCoreUap. lib | Questa libreria fornisce le esportazioni per il subset di API Win32 comuni a tutti i dispositivi Windows 10 che supportano il Windows Runtime (WinRT). Collegare l'app desktop o il driver con OneCoreUap. lib (e nessuna altra libreria) per accedere alle API. Se si collega l'app o il driver a OneCoreUap. lib e si chiamano solo le API Win32 in tale libreria, l'app o il driver si caricherà correttamente in tutti i dispositivi Windows 10 che supportano il UWP. |
| OneCoreUAP_apiset. lib | Questa libreria fornisce la stessa copertura di OneCoreUAP. lib, ma usa la tecnica di [invio diretto dell'API set](api-set-loader-operation.md#direct-forwarding) . Si noti che l'uso di questa libreria è compatibile solo con la versione di Windows 10, come specificato dall'SDK di destinazione o superiore.  |
