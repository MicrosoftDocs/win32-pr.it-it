---
title: Evento Player.DomainChange
description: L'evento DomainChange si verifica quando cambia il dominio DVD. | Evento Player.DomainChange
ms.assetid: 01965492-276e-4d30-99eb-767e0776b423
keywords:
- Evento DomainChange Windows Media Player
- Evento DomainChange Windows Media Player , classe Player
- Classe Player Windows Media Player , evento DomainChange
topic_type:
- apiref
api_name:
- Player.DomainChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f6d70c6a3c2ac2d29c03e6d0518b5e7341f988f41e1bf2f5bb84a7de9f83f68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995911"
---
# <a name="playerdomainchange-event"></a>Evento Player.DomainChange

**L'evento DomainChange** si verifica quando il dominio DVD cambia.

## <a name="syntax"></a>Sintassi


```JScript
Player.DomainChange(
  strDomain
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*strDomain* 
</dt> <dd>

**Stringa** che indica il nuovo dominio. Contiene uno dei valori seguenti.



| string            | Descrizione                                                          |
|-------------------|----------------------------------------------------------------------|
| firstplay         | Esecuzione dell'inizializzazione predefinita di un disco DVD.                     |
| videoManagerMenu  | Visualizzazione dei menu per l'intero disco. Noto anche come menu radice o topMenu. |
| videoTitleSetMenu | Visualizzazione dei menu per il set di titoli corrente. Nota anche come titleMenu.     |
| title             | Visualizzazione del titolo corrente.                                        |
| stop              | Lo strumento di spostamento DVD si trova nel dominio DVD Stop.                         |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Il valore dei parametri dell'evento viene specificato da Windows Media Player ed è accessibile o passato a un metodo in un file JScript importato usando il nome del parametro specificato. Questo nome di parametro deve essere digitato esattamente come illustrato, inclusa l'maiuscola.

**Windows Media Player 10 Mobile:** Questo evento non è supportato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player per Windows XP o versione successiva.<br/>                           |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto DVD**](dvd-object.md)
</dt> <dt>

[**Oggetto Player**](player-object.md)
</dt> </dl>

 

 





