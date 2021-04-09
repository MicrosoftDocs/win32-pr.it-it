---
title: Implementazione e attivazione di un gestore senza dati server aggiuntivi
description: Implementazione e attivazione di un gestore senza dati server aggiuntivi
ms.assetid: 9d91260a-4cec-4a10-bb57-d02999efae47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6866b40e1257a865aa5068ffd46611c411498877
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/03/2021
ms.locfileid: "103968795"
---
# <a name="implementing-and-activating-a-handler-with-no-extra-server-data"></a>Implementazione e attivazione di un gestore senza dati server aggiuntivi

Per creare un'istanza del gestore, se è uno che non ottiene dati server aggiuntivi, il server deve implementare [**IStdMarshalInfo**](/windows/win32/api/objidlbase/nn-objidlbase-istdmarshalinfo) ma non [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal). **IStdMarshalInfo** dispone di un metodo, [**GetClassForHandler**](/windows/win32/api/objidlbase/nf-objidlbase-istdmarshalinfo-getclassforhandler), che recupera il CLSID del gestore dell'oggetto da utilizzare nel processo di destinazione. COM chiama questo oggetto quando chiama [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface) per l'utente e attiva il gestore sul lato client.

Le implementazioni del server e del gestore devono quindi chiamare la funzione [**CoGetStdMarshalEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstdmarshalex) . Questa funzione crea un gestore di marshalling standard su ciascun lato (chiamato gestione proxy sul lato client e un gestore Stub sul lato server).

Il server chiama [**CoGetStdMarshalEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstdmarshalex), passando il flag SMEXF \_ Server. Viene creato un gestore di marshalling standard lato server (gestione Stub). La struttura sul lato server è illustrata nella figura seguente:

![Diagramma che mostra la struttura lato server.](images/b47b3bc0-3e7d-4be4-9767-7ae436bd1b21.png)

## <a name="server-side-structure"></a>Struttura Server-Side

Il gestore chiama [**CoGetStdMarshalEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstdmarshalex), passando il flag SMEXF \_ handler. Viene creato un gestore di marshalling standard lato client (gestione proxy) che viene aggregato con il gestore sul lato client. La durata di entrambi i valori viene gestita dall'oggetto identità di controllo (che implementa [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)) implementato dal sistema quando il gestore chiama **CoGetStdMarshalEx**. La struttura sul lato client è illustrata nella figura seguente.

![Diagramma che mostra la struttura lato client.](images/24ae70ef-dfa8-4784-90ac-dc6cfb043ee5.png)

## <a name="client-side-structure"></a>Struttura Client-Side

Come illustrato nella figura precedente, il gestore è effettivamente inserito tra il gestore del proxy e l'identità o il controllo sconosciuto. In questo modo il controllo del sistema viene assegnato alla durata dell'oggetto, fornendo al gestore il controllo sulle interfacce esposte. La linea tratteggiata tra Identity e gestione proxy indica che i due condividono una stretta integrazione tramite interfacce private interne.

Quando COM chiama [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface) per il client, crea l'istanza del gestore e la aggrega con l'identità. Il gestore creerà il gestore di marshalling standard, tramite la chiamata a [**CoGetStdMarshalEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstdmarshalex), passando il controllo sconosciuto ricevuto al momento della creazione. Il gestore non implementa [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) ma restituisce solo **IMarshal** dal gestore di marshalling standard. Anche se il gestore implementa **IMarshal**, non viene chiamato durante l'unmarshalling.

Se due thread eseguono contemporaneamente l'unmarshalling dello stesso oggetto per la prima volta, è possibile che due gestori vengano creati temporaneamente. Una verrà rilasciata successivamente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestore di Client-Side Lightweight](the-lightweight-client-side-handler.md)
</dt> </dl>

 

 