---
title: Identificatori client
description: Identificatori client
ms.assetid: 69ff159c-9264-4958-a712-4aa50db6e48e
keywords:
- Framework servizi di testo (TSF), identificatori client
- TSF (Framework servizi di testo),identificatori client
- servizi di testo, identificatori client
- applicazioni abilitate per TSF, identificatori client
- identificatori client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f37b230eed1f47ad3e31a5831bddaf8634837c1173806deb084c1e3a4d08790
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117953909"
---
# <a name="client-identifiers"></a>Identificatori client

## <a name="applications"></a>Applicazioni

Un'applicazione ottiene l'identificatore client chiamando [ITfThreadMgr::Activate.](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate)

## <a name="text-services"></a>Servizi di testo

Un servizio di testo ottiene l'identificatore client quando viene chiamato il metodo [ITfTextInputProcessor::Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) del servizio di testo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[ITfThreadMgr::Activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate)
</dt> <dt>

[ITfTextInputProcessor::Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate)
</dt> </dl>

 

 




