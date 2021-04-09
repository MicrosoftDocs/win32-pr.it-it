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
# <a name="visual-basic-method-notes-accvalue"></a><span data-ttu-id="81edd-104">Note sul metodo Visual Basic: accValue</span><span class="sxs-lookup"><span data-stu-id="81edd-104">Visual Basic Method Notes: accValue</span></span>

<span data-ttu-id="81edd-105">Il file di Object Description Language (FAD), oleacc. FAD, contiene informazioni diverse dall'implementazione di C/C++.</span><span class="sxs-lookup"><span data-stu-id="81edd-105">The Object Description Language (ODL) file, Oleacc.odl, contains information that differs from the C/C++ implementation.</span></span> <span data-ttu-id="81edd-106">Il file Oleacc. FAD contiene la definizione seguente per la versione che imposta la proprietà della funzione.</span><span class="sxs-lookup"><span data-stu-id="81edd-106">The file Oleacc.odl contains the following definition for the version that sets the property of the function.</span></span>


```C++
    [hidden, propput, id(DISPID_ACC_VALUE)]
    HRESULT accValue(
        [in, optional] VARIANT varChild,
        [in] BSTR szValue);
```



<span data-ttu-id="81edd-107">Anche se il parametro *varChild* è elencato come facoltativo nel file FAD e nel Visualizzatore oggetti, è necessario includerlo quando si chiama la versione dell'impostazione di proprietà di [**accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-put_accvalue).</span><span class="sxs-lookup"><span data-stu-id="81edd-107">Although the *varChild* parameter is listed as optional in the ODL file and the object browser, you must include it when calling the property-setting version of [**accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-put_accvalue).</span></span>

 

 




