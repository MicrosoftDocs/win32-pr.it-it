---
title: Gestione documenti
description: Gestione documenti
ms.assetid: e30087b6-524a-481e-845d-0348bac3830a
keywords:
- Framework servizi di testo (TSF), gestione documenti
- TSF (Framework di servizi di testo), gestione documenti
- Servizi di testo, gestione documenti
- Applicazioni abilitate per TSF, gestione documenti
- gestione documenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc2182782218ad6a8aa0a70f296f639560307249
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708914"
---
# <a name="document-manager"></a>Gestione documenti

## <a name="applications"></a>Applicazioni

Per creare un oggetto di gestione documenti, un'applicazione chiama [ITfThreadMgr:: CreateDocumentMgr](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr). L'applicazione crea un oggetto di gestione documenti separato per ogni singolo documento gestito dall'applicazione. L'applicazione utilizza Gestione documenti per creare contesti di modifica, aggiungere un contesto allo stack del contesto e rimuovere un contesto dallo stack di contesto.

## <a name="text-services"></a>Servizi di testo

Un servizio di testo non crea mai un oggetto di gestione documenti. Al contrario, il servizio di testo ottiene l'oggetto gestione documenti attualmente attivo chiamando [ITfThreadMgr:: GetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus). Un servizio di testo utilizza Gestione documenti per ottenere il contesto all'inizio dello stack.

Un servizio di testo può inoltre utilizzare Gestione documenti per creare il proprio contesto e aggiungerlo e rimuoverlo dallo stack di contesto. Questa operazione viene in genere eseguita quando il servizio di testo deve visualizzare un'interfaccia utente modale, ad esempio quando viene visualizzato un elenco di parole per consentire all'utente di selezionare una parola. Quando viene visualizzato l'elenco, il servizio di testo inserisce il proprio contesto nello stack. Quando l'elenco di parole viene eliminato, il servizio di testo rimuove il contesto dallo stack.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[ITfDocumentMgr](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr)
</dt> <dt>

[ITfThreadMgr:: CreateDocumentMgr](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr)
</dt> <dt>

[ITfThreadMgr:: GetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus)
</dt> </dl>

 

 




