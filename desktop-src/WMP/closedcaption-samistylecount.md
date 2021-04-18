---
title: ClosedCaption.SAMIStyleCount
description: La proprietà SAMIStyleCount Recupera il numero di stili supportati dal file SAMI corrente.
ms.assetid: 57a85e5d-1598-4cb3-b47d-a6d8f22adfff
keywords:
- Media Player Windows ClosedCaption. SAMIStyleCount
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
ms.openlocfilehash: 3ab48fc6660065da1635b58b67784f2ab0ff91b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324835"
---
# <a name="closedcaptionsamistylecount"></a>ClosedCaption.SAMIStyleCount

La proprietà **SAMIStyleCount** Recupera il numero di stili supportati dal file Sami corrente.

``` syntax
player.closedCaption.SAMIStyleCount
```

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un **numero** di sola lettura (**Long**).

## <a name="remarks"></a>Commenti

Questo metodo non può essere usato fino a quando non viene aperto un file multimediale digitale (*Player*.**openState** è uguale a 13).

**Windows Media Player 10 Mobile:** Questa proprietà restituisce sempre 0.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Aggiunta di didascalie chiuse a file multimediali digitali**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Oggetto ClosedCaption**](closedcaption-object.md)
</dt> <dt>

[**ClosedCaption.getSAMIStyleName**](closedcaption-getsamistylename.md)
</dt> <dt>

[**ClosedCaption.SAMIStyle**](closedcaption-samistyle.md)
</dt> </dl>

 

 





