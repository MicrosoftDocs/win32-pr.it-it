---
title: " ifndef"
description: La direttiva \ ifndef controlla la compilazione condizionale del file di risorse controllando il nome specificato.
ms.assetid: b83d7b0e-1a37-47a8-b495-0eab05ed3a9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 984a969123ea68fd68b14c1b98354b8bc5205aba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298245"
---
# <a name="ifndef"></a>\#ifndef

La direttiva **\# ifndef** controlla la compilazione condizionale del file di risorse controllando il nome specificato. Se il nome non è stato definito o la relativa definizione è stata rimossa usando la direttiva **\# undef** , **\# ifndef** indirizza il compilatore affinché continui a elaborare istruzioni fino alla successiva direttiva **\# endif**, **\# else** o **\# Elif** , quindi passare all'istruzione dopo la direttiva **\# endif** . Se il nome è definito, **\# ifndef** indica al compilatore di ignorare la direttiva **\# endif**, **\# else** o **\# Elif** successiva.

``` syntax
#ifndef name
```

<dl> <dt>

<span id="name"></span><span id="NAME"></span>*nome*
</dt> <dd>

Nome che deve essere controllato dalla direttiva.

</dd> </dl>

## <a name="example"></a>Esempio

In questo esempio viene compilata l'istruzione [**bitmap**](bitmap-resource.md) solo se Optimize non è definito:

``` syntax
#ifndef Optimize
BITMAP 1 errbox.bmp
#endif
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Direttive per il preprocessore](preprocessor-directives.md)
</dt> </dl>

 

 




