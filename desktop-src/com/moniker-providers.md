---
title: Provider di moniker
description: Provider di moniker
ms.assetid: 4d4820d2-bf5f-4543-b318-59481dcc51de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8fab6c5a84d7020b8bcb02979471cb2fbd76df7e66fc9909eec2121926827df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130103"
---
# <a name="moniker-providers"></a>Provider di moniker

In generale, un componente deve essere un provider di moniker quando consente l'accesso a uno dei relativi oggetti, controllando comunque l'archiviazione dell'oggetto. Se un componente deve fornire moniker che identificano i relativi oggetti, deve essere in grado di eseguire le attività seguenti:

-   Su richiesta, creare un moniker che identifica un oggetto.
-   Abilitare il moniker da associare quando un client chiama [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) su di esso.

Un provider di moniker deve creare un moniker di una classe *moniker appropriata* per identificare un oggetto. La classe moniker fa riferimento a un'implementazione specifica [**dell'interfaccia IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) che definisce il tipo di moniker creato. Sebbene sia possibile implementare IMoniker per creare una nuova classe moniker, spesso non è necessario perché OLE fornisce implementazioni di diverse classi di **moniker,** ognuna con il proprio CLSID. Per le descrizioni delle classi di moniker fornite da OLE, vedere Implementazioni di [moniker](ole-moniker-implementations.md) OLE.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Client moniker](moniker-clients.md)
</dt> <dt>

[Implementazioni di moniker OLE](ole-moniker-implementations.md)
</dt> </dl>

 

 




