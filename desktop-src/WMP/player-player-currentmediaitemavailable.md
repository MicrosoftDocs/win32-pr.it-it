---
title: Evento Player. CurrentMediaItemAvailable
description: L'evento CurrentMediaItemAvailable si verifica quando diventa disponibile un elemento di metadati grafici nell'elemento multimediale corrente. | Evento Player. CurrentMediaItemAvailable
ms.assetid: dc692b14-67d3-4867-8f99-ddfcf7d1610c
keywords:
- Media Player di Windows Event CurrentMediaItemAvailable
- Windows Event CurrentMediaItemAvailable Media Player, classe Player
- Classe Player Windows Media Player, evento CurrentMediaItemAvailable
topic_type:
- apiref
api_name:
- Player.CurrentMediaItemAvailable
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7f25d085c354cf18966ec37f822a080db56cf16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326722"
---
# <a name="playercurrentmediaitemavailable-event"></a>Evento Player. CurrentMediaItemAvailable

L'evento **CurrentMediaItemAvailable** si verifica quando diventa disponibile un elemento di metadati grafici nell'elemento multimediale corrente.

## <a name="syntax"></a>Sintassi


```JScript
Player.CurrentMediaItemAvailable(
  bstrItemName
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrItemName* 
</dt> <dd>

**Stringa** contenente il nome dell'elemento multimediale corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Poiché la riproduzione può iniziare prima che un elemento multimediale venga scaricato completamente, eventuali elementi grafici dei metadati contenuti nell'elemento multimediale, ad esempio Album Cover Art, potrebbero non essere disponibili quando viene avviata la riproduzione. Questo evento avvisa l'utente al termine del download di un elemento grafico dei metadati. È quindi possibile recuperare l'oggetto **multimediale** passando il valore di *bstrItemName* a *mediacollection*. metodo **GetByName** , dopo il quale è possibile accedere all'elemento grafico dei metadati usando i *supporti*. **getItemInfoByType** e specificando **WM/Picture** per il nome dell'attributo.

Il valore dei parametri evento viene specificato da Windows Media Player ed è possibile accedervi o passarli a un metodo in un file JScript importato usando il nome del parametro specificato. Questo nome di parametro deve essere digitato esattamente come illustrato, incluse le maiuscole.

**Windows Media Player 10 Mobile:** Questo evento non è supportato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto multimediale**](media-object.md)
</dt> <dt>

[**Media. getItemInfoByType**](media-getiteminfobytype.md)
</dt> <dt>

[**Mediacollection. getByName**](mediacollection-getbyname.md)
</dt> <dt>

[**Oggetto Player**](player-object.md)
</dt> </dl>

 

 





