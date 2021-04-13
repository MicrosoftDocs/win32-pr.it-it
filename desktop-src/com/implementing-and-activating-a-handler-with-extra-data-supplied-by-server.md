---
title: Implementazione e attivazione di un gestore con dati aggiuntivi forniti dal server
description: Implementazione e attivazione di un gestore con dati aggiuntivi forniti dal server
ms.assetid: 5bbf81bd-430d-4008-b1cc-9ea91bb3b1e7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db78a3e39c85c37c52dfa3f09ef41f0a71b5f431
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/03/2021
ms.locfileid: "104350866"
---
# <a name="implementing-and-activating-a-handler-with-extra-data-supplied-by-server"></a>Implementazione e attivazione di un gestore con dati aggiuntivi forniti dal server

Se il server desidera includere nel pacchetto alcuni dati aggiuntivi che devono essere utilizzati dal gestore, il server deve implementare entrambe le interfacce [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) e [**IStdMarshalInfo**](/windows/win32/api/objidlbase/nn-objidlbase-istdmarshalinfo) . Il server deve aggregare il gestore di marshalling standard e deve delegare la prima parte del marshalling al gestore di marshalling standard aggregato, tra cui [**IMarshal:: GetUnmarshalClass**](/windows/desktop/api/ObjIdl/nf-objidl-imarshal-getunmarshalclass)e deve aggiungere la propria dimensione dei dati alle dimensioni restituite dal [**IMarshal:: GetMarshalSizeMax**](/windows/desktop/api/ObjIdl/nf-objidl-imarshal-getmarshalsizemax)del gestore di marshalling standard. Il gestore di marshalling standard chiama [**IStdMarshalInfo:: GetClassForHandler**](/windows/win32/api/objidlbase/nf-objidlbase-istdmarshalinfo-getclassforhandler) per ottenere il CLSID del gestore da creare. Dopo che il gestore di marshalling standard ha eseguito il marshalling, il server scrive i dati aggiuntivi nel flusso. Le strutture risultanti, con dati aggiuntivi nel flusso, sono illustrate nella figura seguente:

![Diagramma che mostra le strutture con dati aggiuntivi nel flusso.](images/4cff306b-bb82-4c05-8e64-7ca73731f265.png)

## <a name="server-side-structures-with-extra-data-in-stream"></a>Server-Side strutture con dati aggiuntivi nel flusso

Ciò consente alla chiamata da COM a [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface) sul lato client di ignorare i dati non letti e lasciare il flusso nella posizione appropriata dopo tutti i dati dell'interfaccia di cui è stato effettuato il marshalling, se non è possibile creare il gestore.

## <a name="client-side-structures-with-extra-data-in-stream"></a>Client-Side strutture con dati aggiuntivi nel flusso

Come nel caso in cui non vi siano dati server aggiuntivi nel flusso, la chiamata COM sul lato client a [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface) creerà l'identità e il gestore. Il gestore deve implementare [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) e deve delegare prima le chiamate **IMarshal** al gestore di marshalling standard aggregato e quindi effettuare il marshalling o l'unmarshalling dei dati aggiuntivi forniti dal server. Il [**UnmarshalInterface**](/windows/win32/api/objidlbase/nf-objidlbase-imarshal-unmarshalinterface) del gestore verrà chiamato per ogni unmarshalling, indipendentemente dal fatto che sia stato effettuato l'unmarshalling dell'interfaccia prima o meno. In questo caso, il server non chiama [**CoGetStdMarshalEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstdmarshalex) , ma il gestore deve. La struttura del lato client risultante è illustrata nella figura seguente.

![Diagramma che mostra la struttura lato client.](images/053411c7-9d54-4ae5-bcb6-778454b1d86f.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestore di Client-Side Lightweight](the-lightweight-client-side-handler.md)
</dt> </dl>

 

 