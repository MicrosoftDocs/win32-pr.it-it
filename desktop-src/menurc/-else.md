---
title: " else"
description: La direttiva \ else contrassegna una clausola facoltativa di un blocco di compilazione condizionale definito da una direttiva \ ifdef, \ ifndef o \ if. La direttiva \ else deve essere l'ultima direttiva prima della direttiva \ endif.
ms.assetid: 982466d9-ae77-4e1c-89f3-511335165da7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 086acd9e6323f7be11a65951a33b2b11b680ad46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710912"
---
# <a name="else"></a>\#else

La direttiva **\# else** contrassegna una clausola facoltativa di un blocco di compilazione condizionale definito da una direttiva **\# ifdef**, **\# ifndef** o **\# if** . La direttiva **\# else** deve essere l'ultima direttiva prima della direttiva **\# endif** .

``` syntax
#else
```

Questa direttiva non ha parametri.

## <a name="example"></a>Esempio

Questo esempio compila la seconda istruzione [**bitmap**](bitmap-resource.md) solo se il debug non è definito:

``` syntax
#ifdef DEBUG
    BITMAP 1 errbox.bmp
#else
    BITMAP 1 userbox.bmp
#endif
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Direttive per il preprocessore](preprocessor-directives.md)
</dt> </dl>

 

 




