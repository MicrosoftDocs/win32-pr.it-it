---
title: Provider moniker
description: Provider moniker
ms.assetid: 4d4820d2-bf5f-4543-b318-59481dcc51de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fde584e12daddacbc940b23b21a0386aa37de2c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710351"
---
# <a name="moniker-providers"></a>Provider moniker

In generale, un componente deve essere un provider del moniker quando consente l'accesso a uno dei relativi oggetti, controllando comunque l'archiviazione dell'oggetto. Se un componente distribuisce moniker che identificano gli oggetti, deve essere in grado di eseguire le attività seguenti:

-   Su richiesta, creare un moniker che identifichi un oggetto.
-   Consente di associare il moniker quando un client chiama [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) .

Un provider del moniker deve creare un moniker di una *classe di moniker* appropriata per identificare un oggetto. La classe moniker si riferisce a un'implementazione specifica dell'interfaccia [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) che definisce il tipo di moniker creato. Sebbene sia possibile implementare **IMoniker** per creare una nuova classe moniker, spesso non è necessario perché OLE fornisce implementazioni di diverse classi moniker, ciascuna con il proprio CLSID. Vedere [implementazioni del moniker OLE](ole-moniker-implementations.md) per le descrizioni delle classi moniker fornite da OLE.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Client moniker](moniker-clients.md)
</dt> <dt>

[Implementazioni del moniker OLE](ole-moniker-implementations.md)
</dt> </dl>

 

 




