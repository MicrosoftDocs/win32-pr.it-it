---
title: Metodo ClosedCaption.getSAMILangName
description: Il metodo getSAMILangName recupera il nome di una lingua supportata dal file SAMI corrente.
ms.assetid: 20cf8faf-3a8c-4d7b-9bd1-2366672f0e67
keywords:
- Metodo getSAMILangName Windows Media Player
- Metodo getSAMILangName Windows Media Player , classe ClosedCaption
- Metodo ClosedCaption Windows Media Player , getSAMILangName
topic_type:
- apiref
api_name:
- ClosedCaption.getSAMILangName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8d4150289eb7637d1772443a5437c6d245993ea0825a37d11bd7ec5accae918
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764031"
---
# <a name="closedcaptiongetsamilangname-method"></a>Metodo ClosedCaption.getSAMILangName

Il **metodo getSAMILangName** recupera il nome di una lingua supportata dal file SAMI corrente.

## <a name="syntax"></a>Sintassi


```JScript
strRetVal = ClosedCaption.getSAMILangName(
  index
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*index* \[ Pollici\]
</dt> <dd>

**Numero** (**long**) che specifica l'indice del nome della lingua da recuperare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **valore String** contenente il nome della lingua come specificato nel file SAMI.

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
</dt> <dt>

[**ClosedCaption.SAMILang**](closedcaption-samilang.md)
</dt> </dl>

 

 





