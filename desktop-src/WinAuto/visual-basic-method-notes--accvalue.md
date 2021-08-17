---
title: Visual Basic Note sul metodo accValue
description: Il file Object Description Language (ODL), Oleacc.odl, contiene informazioni diverse dall'implementazione di C/C++. Il file Oleacc.odl contiene la definizione seguente per la versione che imposta la proprietà della funzione.
ms.assetid: 8c27d63a-ae69-4667-9b65-be743a00b49d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f552f5a79740e71984b4d9beaba9faad23142b2c9afc78a7378e9b11be4dc521
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117744781"
---
# <a name="visual-basic-method-notes-accvalue"></a>Visual Basic Note sul metodo: accValue

Il file Object Description Language (ODL), Oleacc.odl, contiene informazioni diverse dall'implementazione di C/C++. Il file Oleacc.odl contiene la definizione seguente per la versione che imposta la proprietà della funzione.


```C++
    [hidden, propput, id(DISPID_ACC_VALUE)]
    HRESULT accValue(
        [in, optional] VARIANT varChild,
        [in] BSTR szValue);
```



Anche se *il parametro varChild* è elencato come facoltativo nel file ODL e nel visualizzatore oggetti, è necessario includerlo quando si chiama la versione dell'impostazione della proprietà [**di accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-put_accvalue).

 

 




