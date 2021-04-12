---
title: Uso di eventi con chiamate asincrone
description: Uso di eventi con chiamate asincrone
ms.assetid: 98c24176-a632-400e-b23b-5e13f1bd9a27
keywords:
- Windows Media Format SDK, eventi con chiamate asincrone
- Windows Media Format SDK, eventi di chiamata asincrona
- eventi, chiamate asincrone
- eventi di chiamata asincrona
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1729108cae5b73ec96be208709c1360e9401ac0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396635"
---
# <a name="using-events-with-asynchronous-calls"></a>Uso di eventi con chiamate asincrone

Spesso, quando si usano metodi che vengono chiamati in modo asincrono, è opportuno arrestare l'ulteriore elaborazione dell'applicazione fino al completamento dell'elaborazione da parte del metodo. È possibile implementare tutte le tecniche desiderate per gestire questa situazione. In questa sezione viene descritto l'utilizzo di un evento per attendere le chiamate asincrone nel thread chiamante. Questa tecnica viene spesso usata con Windows Media Format SDK ed è illustrata in alcune applicazioni di esempio.

Nell'elenco seguente viene riepilogato l'utilizzo degli eventi per attendere le chiamate asincrone.

1.  Creare un evento da usare con l'applicazione chiamando la funzione **CreateEvent** di Platform SDK.
2.  Quando si implementano i callback appropriati per l'applicazione, intercettare i messaggi per i quali è necessario attendere. Nella logica di gestione dei messaggi per i messaggi desiderati, segnalare l'evento chiamando la funzione **seevent** di Platform SDK.
3.  Dopo aver eseguito le chiamate agli eventi asincroni nell'applicazione, attendere che l'evento segnali chiamando la funzione **WaitForSingleObject** di Platform SDK. Se si progetta un'applicazione Windows, è necessario creare un ciclo per verificare la presenza di messaggi di Windows e includere una chiamata a **WaitForSingleObject** nel ciclo con un breve periodo di attesa.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Utilizzo dei metodi di callback**](using-the-callback-methods.md)
</dt> </dl>

 

 




