---
title: " in, string e out, string Prototype"
description: 'Il prototipo di funzione seguente usa due parametri: \ in, string\ parameter e \ out, string\ parameter.'
ms.assetid: acb0ec4f-1846-4fa2-98c2-2081b52a8260
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 498d12c85130bba8d7d8dcddfc400e2a90fa2d0e2c3cb11c4a7d89696cfe9aa4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073621"
---
# <a name="in-string-and-out-string-prototype"></a>\[in, string \] e \[ out, string \] Prototype

Il prototipo di funzione seguente usa due parametri: \[ [**un parametro in**](/windows/desktop/Midl/in), un parametro [**di**](/windows/desktop/Midl/string) stringa e un parametro di \] stringa \[ [**out.**](/windows/desktop/Midl/out-idl)  \]

``` syntax
void Analyze(
    [in, string]                       *pszInput,
    [out, string, size_is(STRSIZE)]    *pszOutput);
```

Il primo parametro è \[ [**solo in**](/windows/desktop/Midl/in) \] . Questa stringa di input viene trasmessa solo dal client al server. Il server lo usa come base per un'ulteriore elaborazione. La stringa non viene modificata e non è richiesta nuovamente dal client, pertanto non deve essere restituita al client.

Il secondo parametro, che rappresenta la risposta del medico, è \[ [**solo**](/windows/desktop/Midl/out-idl) \] out. Questa stringa di risposta viene trasmessa solo dal server al client. Le dimensioni di allocazione vengono fornite in modo che gli stub del server possano allocare memoria. Poiché *pszOutput è* un \[ [**puntatore ref,**](/windows/desktop/Midl/ref) il client deve avere memoria \] sufficiente allocata per la stringa prima della chiamata. La stringa di risposta viene scritta in quest'area di memoria quando la procedura remota viene restituita.

 

 