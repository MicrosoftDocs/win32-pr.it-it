---
title: Moniker
description: Un moniker in COM non è solo un modo per identificare un oggetto \ 8212; anche un moniker viene implementato come un oggetto.
ms.assetid: ae0cd2f3-8ac0-4388-8781-e86fc4a26b3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf148d63611b5252eec9f5f5f69eacbcece8c65f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044147"
---
# <a name="monikers"></a>Moniker

Un moniker in COM non è solo un modo per identificare un oggetto; un moniker viene inoltre implementato come un oggetto. Questo oggetto fornisce servizi che consentono a un componente di ottenere un puntatore all'oggetto identificato dal moniker. Questo processo è denominato *Binding*.

I moniker sono oggetti che implementano l'interfaccia [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) e vengono in genere implementati nelle DLL come oggetti componente. Esistono due modi per visualizzare l'uso dei moniker: come client moniker, un componente che usa un moniker per ottenere un puntatore a un altro oggetto; e come provider di moniker, un componente che fornisce moniker che identificano i relativi oggetti ai client moniker.

OLE utilizza i moniker per connettersi e attivare gli oggetti, sia che si trovino nello stesso computer o in una rete. Un uso molto importante riguarda le connessioni di rete. Vengono usati anche per identificare, connettersi ed eseguire oggetti di collegamento al documento composito OLE. In questo caso, l'origine del collegamento funge da provider del moniker e il contenitore che contiene l'oggetto collegamento funge da client del moniker.

Per altre informazioni, vedere i seguenti argomenti:

-   [Client moniker](moniker-clients.md)
-   [Provider moniker](moniker-providers.md)
-   [Implementazioni del moniker OLE](ole-moniker-implementations.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Component Object Model (COM)](the-component-object-model.md)
</dt> </dl>

 

 




