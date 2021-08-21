---
title: Moniker puntatore
description: Un moniker di puntatore identifica un oggetto che può esistere solo nello stato attivo o in esecuzione. Questo comportamento è diverso dalle altre classi di moniker, che identificano gli oggetti che possono esistere nello stato passivo o attivo.
ms.assetid: 9895f03d-7110-41c1-a934-87010f9ad380
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bcdf96497751b3f777c292c56d35b2c04432da84b352e20c4dd8b0917dedb16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047899"
---
# <a name="pointer-monikers"></a>Moniker puntatore

Un *moniker di puntatore* identifica un oggetto che può esistere solo nello stato attivo o in esecuzione. Questo comportamento è diverso dalle altre classi di moniker, che identificano gli oggetti che possono esistere nello stato passivo o attivo.

Si supponga, ad esempio, che un'applicazione abbia un oggetto senza rappresentazione permanente. In genere, se un client dell'applicazione deve accedere a tale oggetto, è sufficiente passare al client un puntatore all'oggetto . Si supponga tuttavia che il client si aspetti un moniker. L'oggetto non può essere identificato con un moniker di file, perché non è archiviato in un file né con un moniker di elemento, perché non è contenuto in un altro oggetto.

L'applicazione può invece creare un moniker di puntatore, ovvero un moniker che contiene semplicemente un puntatore internamente, e passarlo al client. Il client può trattare questo moniker come qualsiasi altro. Tuttavia, quando il client chiama [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) sul moniker del puntatore, il codice del moniker non controlla la tabella degli oggetti in esecuzione (ROT) né carica alcun elemento dall'archiviazione. Al contrario, il codice del moniker chiama [**semplicemente QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) sul puntatore archiviato all'interno del moniker.

I moniker puntatore consentono agli oggetti che esistono solo nello stato attivo o in esecuzione di partecipare alle operazioni del moniker e di essere usati dai client del moniker. Una differenza importante tra i moniker puntatore e altre classi di moniker è che i moniker puntatore non possono essere salvati nell'archiviazione permanente. In caso contrario, la chiamata al metodo [**IMoniker::Save**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststream-save) restituisce un errore. Ciò significa che i moniker puntatore sono utili solo in situazioni specializzate. È possibile usare la [**funzione CreatePointerMoniker**](/windows/desktop/api/Objbase/nf-objbase-createpointermoniker) se è necessario usare un moniker di puntatore.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Anti-moniker](anti-monikers.md)
</dt> <dt>

[Moniker di classe](class-monikers.md)
</dt> <dt>

[Moniker compositi](composite-monikers.md)
</dt> <dt>

[Moniker di file](file-monikers.md)
</dt> <dt>

[Moniker di elementi](item-monikers.md)
</dt> </dl>

 

 




