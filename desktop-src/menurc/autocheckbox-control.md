---
title: Controllo AUTOCHECKBOX
description: Definisce un controllo casella di controllo automatico.
ms.assetid: 086f5dd3-267f-4ec6-be37-4e9402f7aede
keywords:
- Menu di controllo AUTOCHECKBOX e altre risorse
topic_type:
- apiref
api_name:
- AUTOCHECKBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 842bb3ede2b1f96f3e5b343e351e047d112a8403
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725559"
---
# <a name="autocheckbox-control"></a>Controllo AUTOCHECKBOX

Definisce un controllo casella di controllo automatico. Il controllo è un rettangolo di piccole dimensioni (casella di controllo) a cui viene visualizzato il testo specificato (in genere, a destra). Quando l'utente sceglie il controllo, il controllo evidenzia il rettangolo e invia un messaggio alla relativa finestra padre.

L'istruzione **AUTOCHECKBOX** può essere utilizzata solo nel corpo di una [**finestra di dialogo**](dialog-resource.md) o di un'istruzione [**DIALOGEX**](dialogex-resource.md) .

``` syntax
AUTOCHECKBOX text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*stile*
</dt> <dd>

Stili del controllo. Questo valore può essere una combinazione dello stile della classe Button **BS \_ AUTOCHECKBOX** e degli stili **WS \_ TABSTOP** e **WS \_ Group** .

Se non si specifica uno stile, lo stile predefinito è `BS_AUTOCHECKBOX | WS_TABSTOP` .

</dd> </dl>

Per ulteriori informazioni sulla sintassi generale di un'istruzione di controllo, vedere [parametri di controllo comuni](common-control-parameters.md).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**AUTO3STATE**](auto3state-control.md)
</dt> <dt>

[Stili dei pulsanti](../controls/button-styles.md)
</dt> <dt>

[**CASELLA**](checkbox-control.md)
</dt> <dt>

[**CONTROLLO**](control-control.md)
</dt> <dt>

[**STATE3**](state3-control.md)
</dt> </dl>

 

 