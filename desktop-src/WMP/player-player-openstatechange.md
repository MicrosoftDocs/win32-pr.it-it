---
title: Evento Player. OpenStateChange
description: L'evento OpenStateChange si verifica in seguito alla modifica del valore della proprietà openState. | Evento Player. OpenStateChange
ms.assetid: b6b840ab-72c7-4150-a259-1e7d8afcec81
keywords:
- Media Player di Windows Event OpenStateChange
- Windows Event OpenStateChange Media Player, classe Player
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
ms.openlocfilehash: 020a25a811623b9f7d7dd8f316c470cada6a142b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326463"
---
# <a name="playeropenstatechange-event"></a>Evento Player. OpenStateChange

L'evento **OpenStateChange** si verifica in seguito alla modifica del valore della proprietà **openState** .

## <a name="syntax"></a>Sintassi


```JScript
Player.OpenStateChange(
  NewState
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*NewState* 
</dt> <dd>

**Numero** (**Long**) che specifica il nuovo stato aperto. Per una tabella di valori, vedere [openState](player-openstate.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Windows Media Player può passare attraverso diversi stati aperti mentre tenta di aprire un file di rete, ad esempio l'individuazione del server, la connessione al server e infine l'apertura del file. Questo evento verrà generato ogni volta che viene modificato lo stato di apertura.

Il valore dei parametri evento viene specificato da Windows Media Player ed è possibile accedervi o passarli a un metodo in un file JScript importato usando il nome del parametro specificato. Questo nome di parametro deve essere digitato esattamente come illustrato, incluse le maiuscole.

Non è garantito che gli Stati di Windows Media Player vengano eseguiti in un ordine particolare. Inoltre, non tutti gli Stati si verificano necessariamente durante una sequenza di eventi. Non è necessario scrivere codice che si basa sull'ordine di stato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Player**](player-object.md)
</dt> <dt>

[**Player. openState**](player-openstate.md)
</dt> </dl>

 

 





