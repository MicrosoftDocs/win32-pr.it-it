---
title: " ifndef"
description: La direttiva \ ifndef controlla la compilazione condizionale del file di risorse controllando il nome specificato.
ms.assetid: b83d7b0e-1a37-47a8-b495-0eab05ed3a9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23728acabc0ca0179c544a66657a2d1b8343d5eae24556018e0e65025420bfba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118472987"
---
# <a name="ifndef"></a>\#ifndef

La **\# direttiva ifndef** controlla la compilazione condizionale del file di risorse controllando il nome specificato. Se il nome non è stato definito o se la relativa definizione è stata rimossa usando la direttiva **\# undef,** **\# ifndef** indica al compilatore di continuare l'elaborazione delle istruzioni fino alla successiva direttiva **\# endif**, **\# else** o **\# elif** e quindi passare all'istruzione dopo la **\# direttiva endif.** Se il nome è definito, **\# ifndef** indica al compilatore di passare alla direttiva **\# endif** successiva, **\# else** o **\# elif.**

``` syntax
#ifndef name
```

<dl> <dt>

<span id="name"></span><span id="NAME"></span>*Nome*
</dt> <dd>

Nome che deve essere controllato dalla direttiva .

</dd> </dl>

## <a name="example"></a>Esempio

Questo esempio compila l'istruzione [**BITMAP**](bitmap-resource.md) solo se Optimize non è definito:

``` syntax
#ifndef Optimize
BITMAP 1 errbox.bmp
#endif
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Direttive per il preprocessore](preprocessor-directives.md)
</dt> </dl>

 

 




