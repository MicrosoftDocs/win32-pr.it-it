---
title: Uso dei metodi di callback
description: Uso dei metodi di callback
ms.assetid: 098cb90b-8c21-4692-a4f9-bacce042520a
keywords:
- Windows Media Format SDK, metodi di callback
- Windows Media Format SDK, metodi chiamati in modo asincrono
- metodi di callback
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b1ee2bcf6587e2e9e75e18404a60c3b85fb4bac5e9f14fd0164304bcc3f3338
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110061"
---
# <a name="using-the-callback-methods"></a>Uso dei metodi di callback

Diverse interfacce nell'SDK Windows Media Format contengono metodi chiamati in modo asincrono. La maggior parte di questi metodi usa funzioni di callback per passare informazioni all'applicazione di controllo.

Le sezioni seguenti descrivono alcuni dei problemi generali relativi all'uso dei metodi di callback con Windows Media Format SDK.



| Sezione                                                                          | Descrizione                                                                                                                                                                                          |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Uso del callback OnStatus](using-the-onstatus-callback.md)                   | Viene descritto come implementare il metodo di callback [**IWMStatusCallback::OnStatus,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) usato da diversi oggetti per consigliare alle applicazioni lo stato dell'operazione DELL'SDK. |
| [Uso di eventi con chiamate asincrone](using-events-with-asynchronous-calls.md) | Descrive una tecnica comune per gestire le chiamate al metodo asincrone in un'applicazione.                                                                                                                  |
| [Uso del parametro context](using-the-context-parameter.md)                   | Introduce il *parametro pvContext,* condiviso da diversi callback e dai relativi metodi chiamanti, e spiega come usarlo.                                                                             |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida per programmatori**](programming-guide.md)
</dt> </dl>

 

 




