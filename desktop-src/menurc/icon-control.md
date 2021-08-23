---
title: Controllo ICON
description: Definisce un controllo icona. Questo controllo è un'icona visualizzata in una finestra di dialogo.
ms.assetid: fd2e1e7a-f386-4fdc-8b05-afce19dd3e8d
keywords:
- Menu e altre risorse del controllo ICON
topic_type:
- apiref
api_name:
- ICON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f4fc5191457996aabe4a70fefcf64235b3a9573cf12733f9ca7bff2ece6356e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034289"
---
# <a name="icon-control"></a>Controllo ICON

Definisce un controllo icona. Questo controllo è un'icona visualizzata in una finestra di dialogo.

L'istruzione di controllo **ICON,** che è possibile usare solo in un'istruzione [**DIALOGEX,**](dialogex-resource.md) definisce l'identificatore di risorsa icona, l'identificatore di controllo icona, la posizione e gli attributi di un controllo.

``` syntax
ICON text, id, x, y [, width, height, style [, extended-style]]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*Testo*
</dt> <dd>

Nome di un'icona (non di un nome file) definito altrove nel file di risorse.

</dd> <dt>

<span id="width"></span><span id="WIDTH"></span>*Larghezza*
</dt> <dd>

Questo valore viene ignorato e deve essere impostato su zero.

</dd> <dt>

<span id="height"></span><span id="HEIGHT"></span>*Altezza*
</dt> <dd>

Questo valore viene ignorato e deve essere impostato su zero.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*Stile*
</dt> <dd>

Stile del controllo. Questo parametro è facoltativo. L'unico valore che può essere specificato è lo **stile SS \_ ICON.** Questo è lo stile predefinito indipendentemente dal fatto che questo parametro sia specificato o meno.

</dd> </dl>

Per altre informazioni sulla sintassi generale di un'istruzione di controllo, vedere [Parametri di controllo comuni](common-control-parameters.md).

## <a name="examples"></a>Esempio

Questo esempio definisce un controllo icona il cui identificatore di icona è 901 e il cui nome è myicon:

``` syntax
ICON "myicon", 901, 30, 30
```

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Icona**](icon-resource.md)
</dt> </dl>

 

 




