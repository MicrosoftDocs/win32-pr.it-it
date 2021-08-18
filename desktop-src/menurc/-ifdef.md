---
title: " ifdef"
description: La direttiva \ ifdef controlla la compilazione condizionale del file di risorse controllando il nome specificato.
ms.assetid: 877c6b58-d8a1-4e68-8b69-29fe106d6cbd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e834dc84d54e1d6f7725008b8bcf28f4ed49fc3fe45f36fb291ddc397d30eb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034479"
---
# <a name="ifdef"></a>\#ifdef

La **\# direttiva ifdef** controlla la compilazione condizionale del file di risorse controllando il nome specificato. Se il nome è stato definito usando una direttiva **\# define** o l'opzione della riga di comando **/d** con il compilatore di risorse, **\# ifdef** indica al compilatore di continuare con l'istruzione immediatamente dopo la **\# direttiva ifdef.** Se il nome non è stato definito, **\# ifdef** indica al compilatore di ignorare tutte le istruzioni fino alla direttiva **\# endif** successiva.

``` syntax
#ifdef name
```

<dl> <dt>

<span id="name"></span><span id="NAME"></span>*Nome*
</dt> <dd>

Nome che deve essere controllato dalla direttiva .

</dd> </dl>

## <a name="example"></a>Esempio

In questo esempio viene compilata [**l'istruzione BITMAP**](bitmap-resource.md) solo se è definito Debug:

``` syntax
#ifdef Debug
BITMAP 1 errbox.bmp
#endif
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Direttive per il preprocessore](preprocessor-directives.md)
</dt> </dl>

 

 




