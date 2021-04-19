---
title: ClosedCaption. getSAMIStyleName, metodo
description: Il metodo getSAMIStyleName Recupera il nome di uno stile supportato dal file SAMI corrente.
ms.assetid: c2ffedf8-4622-44fe-9d92-b52ed3bf3b9a
keywords:
- Metodo getSAMIStyleName Windows Media Player
- Metodo getSAMIStyleName Windows Media Player, classe ClosedCaption
- Classe ClosedCaption Windows Media Player, metodo getSAMIStyleName
topic_type:
- apiref
api_name:
- ClosedCaption.getSAMIStyleName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96480e28e0341b822aaf6726e63a6038681a577f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326735"
---
# <a name="closedcaptiongetsamistylename-method"></a>ClosedCaption. getSAMIStyleName, metodo

Il metodo **getSAMIStyleName** Recupera il nome di uno stile supportato dal file Sami corrente.

## <a name="syntax"></a>Sintassi


```JScript
strRetVal = ClosedCaption.getSAMIStyleName(
  index
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Indice* \[ di in\]
</dt> <dd>

**Numero** (**Long**) che specifica l'indice del nome dello stile da recuperare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce una **stringa** contenente il nome dello stile come specificato nel file Sami.

## <a name="remarks"></a>Commenti

Gli stili in un file SAMI vengono indicizzati nell'ordine indicato nel file, a partire da zero.

Questo metodo non può essere usato fino a quando non viene aperto un file multimediale digitale (*Player*.**openState** è uguale a 13).

**Windows Media Player 10 Mobile:** Questo metodo non è supportato.

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

[**ClosedCaption.SAMIStyle**](closedcaption-samistyle.md)
</dt> </dl>

 

 





