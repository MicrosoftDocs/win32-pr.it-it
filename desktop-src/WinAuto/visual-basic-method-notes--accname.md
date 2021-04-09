---
title: Note sul metodo Visual Basic accName
description: Il file di Object Description Language (FAD), oleacc. FAD, contiene informazioni diverse dall'implementazione di C/C++.
ms.assetid: f7960acd-cb1a-4c34-a392-0243155a100f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c404c093fc3b92b4d653b0b1258c62918af8e25
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856249"
---
# <a name="visual-basic-method-notes-accname"></a>Note sul metodo Visual Basic: accName

Il file di Object Description Language (FAD), oleacc. FAD, contiene informazioni diverse dall'implementazione di C/C++. Il file Oleacc. FAD contiene la definizione seguente per la versione che imposta la proprietà della funzione:


```C++
    [hidden, propput, id(DISPID_ACC_NAME)]
    HRESULT accName(
        [in, optional] VARIANT varChild,
        [in] BSTR szName);
```



Anche se il parametro *varChild* è elencato come facoltativo nel file FAD e nel Visualizzatore oggetti, è necessario includerlo quando si chiama la versione dell'impostazione di proprietà di [**accName**](https://www.bing.com/search?q=**accName**).

 

 




