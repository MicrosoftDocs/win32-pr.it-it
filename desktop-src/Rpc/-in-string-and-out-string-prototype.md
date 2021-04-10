---
title: " in, String e out, prototipo di stringa"
description: Il prototipo di funzione seguente usa due parametri, ovvero un parametro \ in, String \ parameter e un parametro \ out, String \.
ms.assetid: acb0ec4f-1846-4fa2-98c2-2081b52a8260
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c216197fb33a666029429d98761b3219b27b176
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963398"
---
# <a name="in-string-and-out-string-prototype"></a>\[in, String \] e \[ out, \] prototipo di stringa

Il prototipo di funzione seguente usa due parametri: un \[ parametro in, un parametro [**di**](/windows/desktop/Midl/in) [**stringa**](/windows/desktop/Midl/string) \] e un \[ parametro [**out**](/windows/desktop/Midl/out-idl), **String** \] .

``` syntax
void Analyze(
    [in, string]                       *pszInput,
    [out, string, size_is(STRSIZE)]    *pszOutput);
```

Il primo parametro è \[ solo [**in**](/windows/desktop/Midl/in) \] . Questa stringa di input viene trasmessa solo dal client al server. Il server lo utilizza come base per l'ulteriore elaborazione. La stringa non viene modificata e non è richiesta nuovamente dal client, pertanto non è necessario che venga restituita al client.

Il secondo parametro, che rappresenta la risposta del dottore, è \[ [](/windows/desktop/Midl/out-idl) \] solo out. Questa stringa di risposta viene trasmessa solo dal server al client. Le dimensioni di allocazione vengono fornite in modo che gli stub del server possano allocare memoria. Poiché *pszOutput* è un \[ puntatore [**ref**](/windows/desktop/Midl/ref) \] , il client deve disporre di memoria sufficiente allocata per la stringa prima della chiamata. La stringa di risposta viene scritta in questa area di memoria quando la procedura remota restituisce.

 

 