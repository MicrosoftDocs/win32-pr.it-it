---
title: Utilizzo dei metodi di callback
description: Utilizzo dei metodi di callback
ms.assetid: 098cb90b-8c21-4692-a4f9-bacce042520a
keywords:
- Windows Media Format SDK, metodi di callback
- Windows Media Format SDK, metodi chiamati in modo asincrono
- metodi di callback
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d39201c101c9031a7157f79f6c12ec88f07decfc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723415"
---
# <a name="using-the-callback-methods"></a>Utilizzo dei metodi di callback

Diverse interfacce in Windows Media Format SDK contengono metodi che vengono chiamati in modo asincrono. La maggior parte di questi metodi usa funzioni di callback per passare informazioni all'applicazione di controllo.

Nelle sezioni seguenti vengono descritti alcuni problemi generali relativi all'utilizzo di metodi di callback con Windows Media Format SDK.



| Sezione                                                                          | Descrizione                                                                                                                                                                                          |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Uso del callback di OnStatus](using-the-onstatus-callback.md)                   | Viene descritto come implementare il metodo di callback [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) , utilizzato da diversi oggetti per consigliare l'avanzamento dell'operazione dell'SDK. |
| [Uso di eventi con chiamate asincrone](using-events-with-asynchronous-calls.md) | Viene descritta una tecnica comune per gestire le chiamate asincrone al metodo in un'applicazione.                                                                                                                  |
| [Uso del parametro di contesto](using-the-context-parameter.md)                   | Introduce il parametro *pvContext* , condiviso da diversi callback e i relativi metodi di chiamata, e spiega come usarlo.                                                                             |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida per programmatori**](programming-guide.md)
</dt> </dl>

 

 




