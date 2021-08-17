---
description: Una libreria di collegamento generico è una singola libreria a collegamento statico che esporta un subset di API Win32. Ad esempio, una libreria di ombrello denominata OneCore.lib fornisce le esportazioni per il subset di API Win32 comuni a tutti Windows 10 dispositivi.
ms.assetid: A323B5D1-3235-4BBA-96BF-A7DFEBB85C89
title: Librerie generiche di Windows
ms.topic: article
ms.date: 10/14/2020
ms.openlocfilehash: 8714f7054e11e488c61a01fd3f010faaae8c1403efdce6727e88dc26a9d5f133
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117737618"
---
# <a name="windows-umbrella-libraries"></a>Librerie generiche di Windows

Una *libreria di collegamento generico* è una singola libreria a collegamento statico che esporta un subset di API Win32. Ad esempio, una libreria ombrello denominata **OneCore.lib** fornisce le esportazioni per il subset di API Win32 comuni a tutti Windows 10 dispositivi.

Le API in una libreria di ombrello possono essere implementate in un'ampia gamma di moduli (che si tratta di un [set di API](windows-apisets.md) o di una DLL), ma la libreria di ombrello estrae i dettagli, rendendo l'app più portabile tra le versioni del sistema operativo. È sufficiente collegare l'app desktop o il driver alla libreria dell'ombrello che contiene il set di API a cui si è interessati ed è sufficiente. 

| Libreria | Descrizione |
|------------------------|-------------------------|
| OneCore.lib | Questa libreria fornisce le esportazioni per il subset di API Win32 comuni a tutti Windows 10 dispositivi. Collegare l'app desktop o il driver con OneCore.lib (e nessuna altra libreria) per accedere a queste API. Se si collega l'app o il driver a OneCore.lib e si chiamano solo LE API Win32 in tale libreria, l'app o il driver verrà caricato correttamente in tutti Windows 10 dispositivi.         |
| OneCore_apiset.lib | Questa libreria fornisce lo stesso code coverage di OneCore.lib, ma usa l'inoltro diretto [del set](api-set-loader-operation.md#direct-forwarding)di API . Si noti che l'uso di questa libreria sarà compatibile solo con la versione Windows 10 specificata dall'SDK di destinazione o versione successiva.  |
| OneCoreUap.lib | Questa libreria fornisce le esportazioni per il subset di API Win32 comuni a tutti i dispositivi Windows 10 che supportano Windows Runtime (WinRT). Collegare l'app desktop o il driver con OneCoreUap.lib (e nessuna altra libreria) per accedere a queste API. Se si collega l'app o il driver a OneCoreUap.lib e si chiamano solo LE API Win32 in tale libreria, l'app o il driver verrà caricato correttamente in tutti i dispositivi Windows 10 che supportano la UWP. |
| OneCoreUAP_apiset.lib | Questa libreria fornisce lo stesso code coverage di OneCoreUAP.lib, ma usa la tecnica di inoltro diretto [del set di API.](api-set-loader-operation.md#direct-forwarding) Si noti che l'uso di questa libreria sarà compatibile solo con la versione Windows 10 specificata dall'SDK di destinazione o versione successiva.  |
