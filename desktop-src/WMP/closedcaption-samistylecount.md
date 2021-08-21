---
title: ClosedCaption.SAMIStyleCount
description: La proprietà SAMIStyleCount recupera il numero di stili supportati dal file SAMI corrente.
ms.assetid: 57a85e5d-1598-4cb3-b47d-a6d8f22adfff
keywords:
- ClosedCaption.SAMIStyleCount Windows Media Player
topic_type:
- apiref
api_name:
- ClosedCaption.SAMIStyleCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6e5563e40fabfa2cc82dc24598414f312192f864ecacd6ed743834e12e06759
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119522"
---
# <a name="closedcaptionsamistylecount"></a>ClosedCaption.SAMIStyleCount

La **proprietà SAMIStyleCount** recupera il numero di stili supportati dal file SAMI corrente.

``` syntax
player.closedCaption.SAMIStyleCount
```

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un numero di sola **lettura** (**long**).

## <a name="remarks"></a>Commenti

Questo metodo non può essere usato fino a quando non viene aperto un file multimediale digitale (*Lettore*.**openState** è uguale a 13).

**Windows Media Player 10 Mobile:** Questa proprietà restituisce sempre 0.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successive.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Aggiunta di sottotitoli codificati ai supporti digitali**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Oggetto ClosedCaption**](closedcaption-object.md)
</dt> <dt>

[**ClosedCaption.getSAMIStyleName**](closedcaption-getsamistylename.md)
</dt> <dt>

[**ClosedCaption.SAMIStyle**](closedcaption-samistyle.md)
</dt> </dl>

 

 





