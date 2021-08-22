---
title: Visual Basic Note sul metodo accName
description: Il file Object Description Language (ODL), Oleacc.odl, contiene informazioni diverse dall'implementazione C/C++.
ms.assetid: f7960acd-cb1a-4c34-a392-0243155a100f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6cef15db4a8b5705af70f81018ab66f298868b16b32ad658fde4387fdeb4882
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118823616"
---
# <a name="visual-basic-method-notes-accname"></a>Visual Basic Note sul metodo: accName

Il file Object Description Language (ODL), Oleacc.odl, contiene informazioni diverse dall'implementazione C/C++. Il file Oleacc.odl contiene la definizione seguente per la versione che imposta la proprietà della funzione:


```C++
    [hidden, propput, id(DISPID_ACC_NAME)]
    HRESULT accName(
        [in, optional] VARIANT varChild,
        [in] BSTR szName);
```



Anche se *il parametro varChild* è elencato come facoltativo nel file ODL e nel Visualizzatore oggetti, è necessario includerlo quando si chiama la versione dell'impostazione della proprietà [**di accName**](https://www.bing.com/search?q=**accName**).

 

 




