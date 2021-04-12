---
title: " ifdef"
description: La direttiva \ ifdef controlla la compilazione condizionale del file di risorse controllando il nome specificato.
ms.assetid: 877c6b58-d8a1-4e68-8b69-29fe106d6cbd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38170fb2140f8405a86529c0899c1e4d4e93c026
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396051"
---
# <a name="ifdef"></a>\#ifdef

La direttiva **\# ifdef** controlla la compilazione condizionale del file di risorse controllando il nome specificato. Se il nome è stato definito usando una direttiva **\# define** o l'opzione della riga di comando **/d** con il compilatore di risorse, **\# ifdef** indica al compilatore di continuare con l'istruzione immediatamente dopo la direttiva **\# ifdef** . Se il nome non è stato definito, **\# ifdef** indica al compilatore di ignorare tutte le istruzioni fino alla direttiva **\# endif** successiva.

``` syntax
#ifdef name
```

<dl> <dt>

<span id="name"></span><span id="NAME"></span>*nome*
</dt> <dd>

Nome che deve essere controllato dalla direttiva.

</dd> </dl>

## <a name="example"></a>Esempio

In questo esempio viene compilata l'istruzione [**bitmap**](bitmap-resource.md) solo se è definito il debug:

``` syntax
#ifdef Debug
BITMAP 1 errbox.bmp
#endif
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Direttive per il preprocessore](preprocessor-directives.md)
</dt> </dl>

 

 




