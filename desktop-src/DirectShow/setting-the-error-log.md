---
description: Impostazione del log degli errori
ms.assetid: 2e3124e3-32d0-4eb6-9c1d-91b625018ac4
title: Impostazione del log degli errori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac96fb90570408ca41be06656f7cf1704e9f48dc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303695"
---
# <a name="setting-the-error-log"></a>Impostazione del log degli errori

\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]

Dopo aver implementato la classe di registrazione degli errori, creare una nuova istanza della classe. Assegnare quindi ai [servizi di modifica DirectShow](directshow-editing-services.md) un puntatore chiamando il metodo [**IAMSetErrorLog::p log degli \_ errori UT**](iamseterrorlog-put-errorlog.md) nella sequenza temporale. Eseguire una query sulla sequenza temporale per l'interfaccia **IAMSetErrorLog** . Per assicurarsi che tutti gli errori vengano registrati, è necessario chiamare questo metodo prima di caricare, salvare o eseguire il rendering della sequenza temporale.


```C++
IAMSetErrorLog  *pSetLog = NULL;
IAMErrorLog     *pLog = new CErrReporter();

pTL->QueryInterface(IID_IAMSetErrorLog, (void **)&pSetLog);
pSetLog->put_ErrorLog(pLog);
pSetLog->Release();
```



La registrazione degli errori non ha alcun effetto sui valori restituiti ricevuti quando si chiamano i metodi nell'applicazione. La registrazione degli errori è complementare, ma non sostituisce le consuete tecniche di gestione degli errori. Per creare un'applicazione affidabile, controllare sempre i valori HRESULT.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Errori di registrazione](logging-errors.md)
</dt> </dl>

 

 



