---
title: Impostazioni.balance
description: La proprietà balance specifica o recupera il bilanciamento stereo corrente.
ms.assetid: 26f04989-a1b1-4aec-8a15-c4e3737a4e62
keywords:
- Impostazioni.balance Windows Media Player
topic_type:
- apiref
api_name:
- Settings.balance
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e569c40214655fc643762da8580bd8d6a16e098b99c649bb27e1a1485d498931
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118569576"
---
# <a name="settingsbalance"></a>Impostazioni.balance

La **proprietà balance** specifica o recupera il bilanciamento stereo corrente.

## <a name="syntax"></a>Sintassi

player.settings.balance

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un numero di **lettura/scrittura** (**long**). I valori sono compreso tra 100 e 100, con un valore predefinito pari a zero.

## <a name="remarks"></a>Commenti

Il valore zero indica che l'audio viene riprodotto con lo stesso volume su entrambi i canali sinistro e destro. Il valore 100 indica che l'audio viene riprodotto solo sul canale sinistro. Il valore 100 indica che l'audio viene riprodotto solo sul canale destro.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Impostazioni Oggetto**](settings-object.md)
</dt> </dl>

 

 





