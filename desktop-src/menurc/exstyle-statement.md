---
title: EXSTYLE-istruzione
description: Definisce gli stili estesi della finestra per una finestra di dialogo. In una definizione di risorsa, l'istruzione EXSTYLE viene inserita con le istruzioni facoltative prima dell'inizio del corpo della definizione di risorsa.
ms.assetid: 5dc74bab-e385-457c-80c4-5e04eed589b5
keywords:
- Menu di istruzioni EXSTYLE e altre risorse
topic_type:
- apiref
api_name:
- EXSTYLE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 277727757daeaafe5ad11cfd2e4f5fb6ee726458
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472915"
---
# <a name="exstyle-statement"></a>EXSTYLE-istruzione

Definisce gli stili estesi della finestra per una finestra di dialogo. In una definizione di risorsa, l'istruzione **ExStyle** viene inserita con le istruzioni facoltative prima dell'inizio del corpo della definizione di risorsa.

``` syntax
EXSTYLE extended-style
```

<dl> <dt>

<span id="extended-style"></span><span id="EXTENDED-STYLE"></span>*stile esteso*
</dt> <dd>

Stile di finestra esteso per la finestra di dialogo o il controllo. Per un elenco degli stili estesi della finestra, vedere [**stili finestra estesi**](/windows/desktop/winmsg/extended-window-styles).

</dd> </dl>

## <a name="remarks"></a>Commenti

Per i controlli, gli stili estesi vengono specificati dopo l'opzione *stile* nell'istruzione di definizione della risorsa del controllo. Per ulteriori informazioni, vedere l'istruzione di definizione delle risorse per il singolo controllo.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ACCELERATORI**](accelerators-resource.md)
</dt> <dt>

[**CONTROLLO**](control-control.md)
</dt> <dt>

[**DIALOGO**](dialog-resource.md)
</dt> <dt>

[**MENU**](menu-resource.md)
</dt> <dt>

[**POPUP**](popup-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**UN'STRINGTABLE**](stringtable-resource.md)
</dt> <dt>

[Risorsa definita dall'utente](user-defined-resource.md)
</dt> </dl>

 

 