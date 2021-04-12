---
title: Controllo ICON
description: Definisce un controllo icona. Questo controllo è un'icona visualizzata in una finestra di dialogo.
ms.assetid: fd2e1e7a-f386-4fdc-8b05-afce19dd3e8d
keywords:
- Menu di controllo delle icone e altre risorse
topic_type:
- apiref
api_name:
- ICON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2400136395a17f039d552373fa35cba0f3545a5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104471918"
---
# <a name="icon-control"></a>Controllo ICON

Definisce un controllo icona. Questo controllo è un'icona visualizzata in una finestra di dialogo.

L'istruzione di controllo **Icon** , che può essere usata solo in un'istruzione [**DIALOGEX**](dialogex-resource.md) , definisce l'identificatore di risorsa icona, l'identificatore di controllo icona, la posizione e gli attributi di un controllo.

``` syntax
ICON text, id, x, y [, width, height, style [, extended-style]]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*testo*
</dt> <dd>

Nome di un'icona (non un nome di file) definito altrove nel file di risorse.

</dd> <dt>

<span id="width"></span><span id="WIDTH"></span>*Larghezza*
</dt> <dd>

Questo valore viene ignorato e deve essere impostato su zero.

</dd> <dt>

<span id="height"></span><span id="HEIGHT"></span>*altezza*
</dt> <dd>

Questo valore viene ignorato e deve essere impostato su zero.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*stile*
</dt> <dd>

Stile del controllo. Questo parametro è facoltativo. L'unico valore che è possibile specificare è lo stile dell' **\_ icona SS** . Si tratta dello stile predefinito se questo parametro è specificato o meno.

</dd> </dl>

Per ulteriori informazioni sulla sintassi generale di un'istruzione di controllo, vedere [parametri di controllo comuni](common-control-parameters.md).

## <a name="examples"></a>Esempio

Questo esempio definisce un controllo Icon il cui identificatore di icona è 901 e il cui nome è l'icona:

``` syntax
ICON "myicon", 901, 30, 30
```

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ICONA**](icon-resource.md)
</dt> </dl>

 

 




