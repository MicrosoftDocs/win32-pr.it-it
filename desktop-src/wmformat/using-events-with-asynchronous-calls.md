---
title: Uso di eventi con chiamate asincrone
description: Uso di eventi con chiamate asincrone
ms.assetid: 98c24176-a632-400e-b23b-5e13f1bd9a27
keywords:
- Windows MEDIA Format SDK, eventi con chiamate asincrone
- Windows Media Format SDK, eventi di chiamata asincrona
- eventi, chiamate asincrone
- eventi di chiamata asincrona
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd315b56570419afd81aa3300cfa3ee1dd907e22310aba79432e4533f99a82db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929131"
---
# <a name="using-events-with-asynchronous-calls"></a>Uso di eventi con chiamate asincrone

Spesso, quando si usano metodi chiamati in modo asincrono, è necessario interrompere l'ulteriore elaborazione dell'applicazione fino al termine dell'elaborazione del metodo. È possibile implementare qualsiasi tecnica per gestire questa situazione. In questa sezione viene descritto l'utilizzo di un evento per attendere chiamate asincrone nel thread chiamante. Questa tecnica viene spesso usata con Windows Media Format SDK e viene illustrata in alcune delle applicazioni di esempio.

Nell'elenco seguente viene riepilogato l'utilizzo di eventi per l'attesa di chiamate asincrone.

1.  Creare un evento da usare con l'applicazione chiamando la **funzione CreateEvent** di Platform SDK.
2.  Quando si implementano i callback appropriati per l'applicazione, intercettare i messaggi per i quali è necessario attendere. Nella logica di gestione dei messaggi per i messaggi desiderati segnalare l'evento chiamando la **funzione SetEvent** di Platform SDK.
3.  Dopo aver effettuato chiamate a eventi asincroni nell'applicazione, attendere che l'evento segnali chiamando la **funzione WaitForSingleObject** di Platform SDK. Se si progetta un'applicazione Windows, è necessario creare un ciclo per verificare la presenza di messaggi Windows e includere una chiamata a **WaitForSingleObject** nel ciclo con un breve tempo di attesa.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso dei metodi di callback**](using-the-callback-methods.md)
</dt> </dl>

 

 




