---
title: Note sul metodo Visual Basic accValue
description: Il file di Object Description Language (FAD), oleacc. FAD, contiene informazioni diverse dall'implementazione di C/C++. Il file Oleacc. FAD contiene la definizione seguente per la versione che imposta la proprietà della funzione.
ms.assetid: 8c27d63a-ae69-4667-9b65-be743a00b49d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ce93bc5d4ff2a2e01da55e30630fda42c573b7f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044563"
---
# <a name="visual-basic-method-notes-accvalue"></a>Note sul metodo Visual Basic: accValue

Il file di Object Description Language (FAD), oleacc. FAD, contiene informazioni diverse dall'implementazione di C/C++. Il file Oleacc. FAD contiene la definizione seguente per la versione che imposta la proprietà della funzione.


```C++
    [hidden, propput, id(DISPID_ACC_VALUE)]
    HRESULT accValue(
        [in, optional] VARIANT varChild,
        [in] BSTR szValue);
```



Anche se il parametro *varChild* è elencato come facoltativo nel file FAD e nel Visualizzatore oggetti, è necessario includerlo quando si chiama la versione dell'impostazione di proprietà di [**accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-put_accvalue).

 

 




