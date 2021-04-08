---
title: Trasferimento di oggetti
description: Trasferimento di oggetti
ms.assetid: 3afdf480-a7ee-4b7b-99f6-4a8e8cb2096c
ms.tgt_platform: multiple
keywords:
- Esempi di Active Directory Active Directory, trasferimento di oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7019904d0de42492b98ddd297ab007a6f4e52f6a
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046501"
---
# <a name="moving-objects"></a>Trasferimento di oggetti

Per spostare un oggetto all'interno di un dominio, usare il metodo [**IADsContainer. MoveHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere) .

**Per spostare un oggetto all'interno di un dominio**

1.  Eseguire l'associazione all'interfaccia [**IADs**](/windows/desktop/api/iads/nn-iads-iads) dell'oggetto da spostare.
2.  Ottenere il ADsPath dell'oggetto da spostare dalla proprietà [**IADs. ADsPath**](/windows/desktop/ADSI/iads-property-methods) .
3.  Eseguire l'associazione all'interfaccia [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) del contenitore in cui verrà spostato l'oggetto.
4.  Spostare l'oggetto con il metodo [**IADsContainer. MoveHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere) .

Se è presente un'interfaccia per l'oggetto spostato, l'interfaccia non è valida dopo lo spostamento dell'oggetto perché l'oggetto directory rappresentato dall'interfaccia non esiste più.

Per ulteriori informazioni e un esempio di codice in cui viene illustrato come spostare un oggetto, vedere il [codice di esempio per lo spostamento di un oggetto](example-code-for-moving-an-object.md).

 

 