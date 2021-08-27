---
title: Spostamento di oggetti
description: Spostamento di oggetti
ms.assetid: 3afdf480-a7ee-4b7b-99f6-4a8e8cb2096c
ms.tgt_platform: multiple
keywords:
- Esempi di Active Directory Active Directory , spostamento di oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1158bfc3fb85712b2ab52b6b69d86c7af52675d210b75b0c9974fc2da6359ae4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025859"
---
# <a name="moving-objects"></a>Spostamento di oggetti

Per spostare un oggetto all'interno di un dominio, usare il [**metodo IADsContainer.MoveHere.**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere)

**Per spostare un oggetto all'interno di un dominio**

1.  Eseguire [**l'associazione all'interfaccia IAD**](/windows/desktop/api/iads/nn-iads-iads) dell'oggetto da spostare.
2.  Ottiene l'ADsPath dell'oggetto da spostare dalla [**proprietà IADs.ADsPath.**](/windows/desktop/ADSI/iads-property-methods)
3.  Eseguire l'associazione [**all'interfaccia IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) del contenitore in cui verrà spostato l'oggetto.
4.  Spostare l'oggetto con [**il metodo IADsContainer.MoveHere.**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere)

Se esiste un'interfaccia per l'oggetto spostato, l'interfaccia non è valida dopo lo spostamento dell'oggetto perché l'oggetto directory rappresentato dall'interfaccia non esiste più.

Per altre informazioni e un esempio di codice che illustra come spostare un oggetto, vedere [Codice di esempio per lo spostamento di un oggetto](example-code-for-moving-an-object.md).

 

 