---
title: Metodo ClosedCaption.getSAMILangID
description: Il metodo getSAMILangID recupera l'identificatore delle impostazioni locali (LCID) di una lingua supportata dal file SAMI corrente.
ms.assetid: 35f8379a-a2f5-4b22-b1ad-3c5cc5bc5e3d
keywords:
- Metodo getSAMILangID Windows Media Player
- Metodo getSAMILangID Windows Media Player , classe ClosedCaption
- Metodo ClosedCaption Windows Media Player , getSAMILangID
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
ms.openlocfilehash: 7317bff13b0dcf29157e4a31c1b854fff781d93460633b64485670fab64e6f1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764041"
---
# <a name="closedcaptiongetsamilangid-method"></a>Metodo ClosedCaption.getSAMILangID

Il **metodo getSAMILangID** recupera l'identificatore delle impostazioni locali (LCID) di una lingua supportata dal file SAMI corrente.

## <a name="syntax"></a>Sintassi


```JScript
retVal = ClosedCaption.getSAMILangID(
  index
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*index* \[ Pollici\]
</dt> <dd>

**Numero** (**long**) che specifica l'indice dell'LCID da recuperare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **valore Number** (**long**) contenente l'LCID della lingua con l'indice specificato.

## <a name="remarks"></a>Commenti

Le lingue in un file SAMI vengono indicizzate nell'ordine indicato nel file, a partire da zero.

Questo metodo non può essere usato fino a quando non viene aperto un file multimediale digitale (*Lettore*.**openState** è uguale a 13).

**Windows Media Player 10 Mobile:** Questo metodo non è supportato.

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
</dt> </dl>

 

 





