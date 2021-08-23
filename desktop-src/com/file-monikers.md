---
title: Moniker file
description: Moniker file
ms.assetid: 923f798d-d789-4e6d-b27e-dd5a72f92abf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa51d000964bcfe7cad29db333bbbbc68b3a94d0f977c47b29affab4eed0b139
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048289"
---
# <a name="file-monikers"></a>Moniker file

*I moniker di* file sono la classe di moniker più semplice. I moniker di file possono essere usati per identificare qualsiasi oggetto archiviato nel proprio file. Un moniker di file funge da wrapper per il nome del percorso file system al file. Se [**si chiama IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) per questo moniker, l'oggetto viene attivato e quindi viene restituito un puntatore di interfaccia all'oggetto. L'origine dell'oggetto denominato dal moniker deve fornire un'implementazione [**dell'interfaccia IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile) per supportare l'associazione di un moniker di file. I moniker di file possono rappresentare un percorso completo o relativo.

Ad esempio, il moniker di file per un oggetto foglio di calcolo archiviato come file C: WorkMySheet.xls conterrà informazioni \\ \\ equivalenti al nome del percorso. Tuttavia, il moniker non è necessariamente costituito dalla stessa stringa. La stringa è solo il *nome* visualizzato, una rappresentazione del contenuto del moniker significativa per un utente finale. Il nome visualizzato, disponibile tramite il metodo [**IMoniker::GetDisplayName,**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-getdisplayname) viene usato solo quando si visualizza un moniker a un utente finale. Questo metodo ottiene il nome visualizzato per una delle classi del moniker. Internamente, il moniker può archiviare le stesse informazioni in un formato più efficiente per l'esecuzione di operazioni del moniker, ma non significativo per gli utenti. Quindi, quando questo stesso oggetto viene associato tramite una chiamata al metodo [**BindToObject,**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) l'oggetto viene attivato, probabilmente caricando il file nel foglio di calcolo.

OLE offre ai provider di moniker la funzione helper [**CreateFileMoniker**](/windows/desktop/api/Objbase/nf-objbase-createfilemoniker) che crea un oggetto moniker di file e restituisce il relativo puntatore al provider.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Anti-moniker](anti-monikers.md)
</dt> <dt>

[Moniker di classe](class-monikers.md)
</dt> <dt>

[Moniker compositi](composite-monikers.md)
</dt> <dt>

[Moniker degli elementi](item-monikers.md)
</dt> <dt>

[Moniker puntatore](pointer-monikers.md)
</dt> </dl>

 

 




