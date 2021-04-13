---
title: Moniker puntatore
description: Un moniker del puntatore identifica un oggetto che può esistere solo nello stato attivo o in esecuzione. Questo comportamento è diverso da quello delle altre classi dei moniker, che identificano gli oggetti che possono esistere nello stato passivo o attivo.
ms.assetid: 9895f03d-7110-41c1-a934-87010f9ad380
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aebebfce908571b69a5b8ce05f589a4ca4b30977
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "104398449"
---
# <a name="pointer-monikers"></a>Moniker puntatore

Un *moniker del puntatore* identifica un oggetto che può esistere solo nello stato attivo o in esecuzione. Questo comportamento è diverso da quello delle altre classi dei moniker, che identificano gli oggetti che possono esistere nello stato passivo o attivo.

Si supponga, ad esempio, che un'applicazione disponga di un oggetto senza rappresentazione permanente. In genere, se un client dell'applicazione deve accedere a tale oggetto, è sufficiente passare al client un puntatore all'oggetto. Si supponga, tuttavia, che il client stia aspettando un moniker. L'oggetto non può essere identificato con un moniker di file perché non è archiviato in un file, né con un moniker di elemento, perché non è contenuto in un altro oggetto.

Al contrario, l'applicazione può creare un moniker puntatore, che è un moniker che contiene semplicemente un puntatore internamente e passarlo al client. Il client può gestire questo moniker come qualsiasi altro. Tuttavia, quando il client chiama [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) sul moniker del puntatore, il codice del moniker non controlla la tabella degli oggetti in esecuzione (ROT) o carica qualsiasi elemento dalla risorsa di archiviazione. Al contrario, il codice del moniker chiama semplicemente [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) sul puntatore archiviato all'interno del moniker.

I moniker del puntatore consentono agli oggetti esistenti solo nello stato attivo o in esecuzione di partecipare alle operazioni del moniker e di essere utilizzati dai client del moniker. Una differenza importante tra i moniker del puntatore e altre classi di moniker è che i moniker del puntatore non possono essere salvati nell'archivio permanente. In tal caso, la chiamata al metodo [**IMoniker:: Save**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststream-save) restituisce un errore. Ciò significa che i moniker del puntatore sono utili solo in situazioni specializzate. Se è necessario usare un moniker puntatore, è possibile usare la funzione [**CreatePointerMoniker**](/windows/desktop/api/Objbase/nf-objbase-createpointermoniker) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Anti-moniker](anti-monikers.md)
</dt> <dt>

[Moniker della classe](class-monikers.md)
</dt> <dt>

[Moniker compositi](composite-monikers.md)
</dt> <dt>

[Moniker di file](file-monikers.md)
</dt> <dt>

[Moniker elemento](item-monikers.md)
</dt> </dl>

 

 




