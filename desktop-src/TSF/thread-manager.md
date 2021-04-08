---
title: Gestione thread
description: Gestione thread è il componente di base del gestore di TSF.
ms.assetid: fd43b4c3-80bb-4118-a880-bdea07022c95
keywords:
- Framework servizi di testo (TSF), gestione thread
- TSF (Text Services Framework), gestione thread
- Servizi di testo, gestione thread
- Applicazioni abilitate per TSF, gestione thread
- gestione thread
- Gestione TSF
- notifiche di eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b29596c5c39267181c6a2c301aede3f15ca7297
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046991"
---
# <a name="thread-manager"></a>Gestione thread

Gestione thread è il componente di base del gestore di TSF. Gestione thread esegue attività comuni correlate alle applicazioni e ai servizi di testo (client). Queste attività includono, ad esempio, l'attivazione e la disattivazione di servizi di testo TSF, la creazione di gestori di documenti e la manutenzione della relazione corretta tra documenti e lo stato attivo per l'input. Gestione thread viene definito dall'interfaccia [ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr) .

La maggior parte delle interfacce e degli oggetti forniti dal gestore di TSF può essere ottenuta usando i metodi forniti dall'interfaccia del gestore di thread.

## <a name="applications"></a>Applicazioni

Un'applicazione crea un oggetto gestore thread chiamando [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) con CLSID \_ TFThreadMgr.

## <a name="text-services"></a>Servizi di testo

Un servizio di testo ottiene un oggetto gestore thread nel metodo [ITfTextInputProcessor:: Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) del servizio di testo.

## <a name="event-notifications"></a>Notifiche degli eventi

Gestione thread fornisce inoltre la notifica degli eventi ai client. In TSF, le notifiche degli eventi vengono fornite per mezzo di un sink di evento, ovvero un oggetto COM. Per ricevere notifiche da gestione thread, un client implementa un oggetto [ITfThreadMgrEventSink](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgreventsink) e installa il sink di evento. Il sink di evento viene installato eseguendo una query su gestione thread per IID \_ ITfSource e chiamando [ITfSource:: ADVISESINK](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink) con IID \_ ITfThreadMgrEventSink.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr)
</dt> <dt>

[CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

[ITfTextInputProcessor:: Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate)
</dt> <dt>

[ITfThreadMgrEventSink](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgreventsink)
</dt> <dt>

[ITfSource:: AdviseSink](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink)
</dt> </dl>

 

 