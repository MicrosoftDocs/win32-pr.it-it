---
title: Moniker di file
description: Moniker di file
ms.assetid: 923f798d-d789-4e6d-b27e-dd5a72f92abf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5c18beeff04804b11f04c0a2c211f2dd09dd60d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329188"
---
# <a name="file-monikers"></a>Moniker di file

I *moniker del file* sono la classe del moniker più semplice. I moniker dei file possono essere utilizzati per identificare qualsiasi oggetto archiviato nel proprio file. Un moniker di file funge da wrapper per il nome del percorso che il file system nativo assegna al file. Se si chiama [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) per questo moniker, questo oggetto verrà attivato e quindi restituirà un puntatore di interfaccia all'oggetto. L'origine dell'oggetto denominato dal moniker deve fornire un'implementazione dell'interfaccia [**IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile) per supportare l'associazione di un moniker di file. I moniker del file possono rappresentare un percorso completo o relativo.

Ad esempio, il moniker del file per un oggetto foglio di calcolo archiviato come file C: \\ Work \\MySheet.xls conterrebbe informazioni equivalenti al nome di tale percorso. Il moniker, tuttavia, non è necessariamente costituito dalla stessa stringa. La stringa è semplicemente il *nome displayâ*, una rappresentazione del contenuto del moniker significativo per un utente finale. Il nome visualizzato, disponibile tramite il metodo [**IMoniker:: GetDisplayName**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-getdisplayname) , viene usato solo quando si visualizza un moniker per un utente finale. Questo metodo ottiene il nome visualizzato per qualsiasi classe moniker. Internamente, il moniker può archiviare le stesse informazioni in un formato più efficiente per l'esecuzione di operazioni sui moniker ma non significative per gli utenti. Quindi, quando lo stesso oggetto viene associato tramite una chiamata al metodo [**BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) , l'oggetto verrebbe attivato, probabilmente caricando il file nel foglio di calcolo.

OLE offre ai provider del moniker la funzione di supporto [**CreateFileMoniker**](/windows/desktop/api/Objbase/nf-objbase-createfilemoniker) che crea un oggetto moniker del file e restituisce il relativo puntatore al provider.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Anti-moniker](anti-monikers.md)
</dt> <dt>

[Moniker della classe](class-monikers.md)
</dt> <dt>

[Moniker compositi](composite-monikers.md)
</dt> <dt>

[Moniker elemento](item-monikers.md)
</dt> <dt>

[Moniker puntatore](pointer-monikers.md)
</dt> </dl>

 

 




