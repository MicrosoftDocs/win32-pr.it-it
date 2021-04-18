---
title: ClosedCaption. getSAMILangID, metodo
description: Il metodo getSAMILangID recupera l'identificatore delle impostazioni locali (LCID) di una lingua supportata dal file SAMI corrente.
ms.assetid: 35f8379a-a2f5-4b22-b1ad-3c5cc5bc5e3d
keywords:
- Metodo getSAMILangID Windows Media Player
- Metodo getSAMILangID Windows Media Player, classe ClosedCaption
- Classe ClosedCaption Windows Media Player, metodo getSAMILangID
topic_type:
- apiref
api_name:
- ClosedCaption.getSAMILangID
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cd543c9cb9d884022d78a875a2f8de078c479b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333932"
---
# <a name="closedcaptiongetsamilangid-method"></a>ClosedCaption. getSAMILangID, metodo

Il metodo **getSAMILangID** recupera l'identificatore delle impostazioni locali (LCID) di una lingua supportata dal file Sami corrente.

## <a name="syntax"></a>Sintassi


```JScript
retVal = ClosedCaption.getSAMILangID(
  index
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Indice* \[ di in\]
</dt> <dd>

**Numero** (**Long**) che specifica l'indice dell'LCID da recuperare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **numero** (**Long**) contenente l'identificatore LCID della lingua con l'indice specificato.

## <a name="remarks"></a>Commenti

Le lingue in un file SAMI sono indicizzate nell'ordine indicato nel file, a partire da zero.

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
</dt> </dl>

 

 





