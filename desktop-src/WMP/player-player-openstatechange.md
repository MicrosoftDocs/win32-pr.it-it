---
title: Evento Player.OpenStateChange
description: L'evento OpenStateChange si verifica quando il valore della proprietà openState cambia. | Evento Player.OpenStateChange
ms.assetid: b6b840ab-72c7-4150-a259-1e7d8afcec81
keywords:
- Evento OpenStateChange Windows Media Player
- Classe di evento OpenStateChange Windows Media Player , Player
- Classe Player Windows Media Player, evento OpenStateChange
topic_type:
- apiref
api_name:
- Player.OpenStateChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b65436dee60a5207e09a57a39c32dc479ce110e1dafb07a7dbd7cab86e4f0a92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003221"
---
# <a name="playeropenstatechange-event"></a>Evento Player.OpenStateChange

**L'evento OpenStateChange** si verifica quando il valore della **proprietà openState** cambia.

## <a name="syntax"></a>Sintassi


```JScript
Player.OpenStateChange(
  NewState
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Newstate* 
</dt> <dd>

**Numero** (**long**) che specifica il nuovo stato aperto. Vedere [openState](player-openstate.md) per una tabella di valori.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Windows Media Player possibile passare attraverso diversi stati aperti mentre tenta di aprire un file di rete, ad esempio l'individuazione del server, la connessione al server e infine l'apertura del file. Questo evento verrà generato ogni volta che lo stato di apertura cambia.

Il valore dei parametri dell'evento viene specificato da Windows Media Player e può essere accessibile o passato a un metodo in un file JScript importato usando il nome del parametro specificato. Questo nome di parametro deve essere digitato esattamente come illustrato, inclusa l'maiuscola.

Windows Media Player non è garantito che gli stati si verifichino in un ordine particolare. Inoltre, non tutti gli stati si verificano necessariamente durante una sequenza di eventi. È consigliabile non scrivere codice che si basa sull'ordine di stato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Player**](player-object.md)
</dt> <dt>

[**Player.openState**](player-openstate.md)
</dt> </dl>

 

 





