---
title: Evento Player. DomainChange
description: L'evento DomainChange si verifica quando viene modificato il dominio DVD. | Evento Player. DomainChange
ms.assetid: 01965492-276e-4d30-99eb-767e0776b423
keywords:
- Media Player di Windows Event DomainChange
- Windows Event DomainChange Media Player, classe Player
- Classe Player Windows Media Player, evento DomainChange
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
ms.openlocfilehash: fa9637913451aa5bba937906130899c46e0bd34d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329303"
---
# <a name="playerdomainchange-event"></a>Evento Player. DomainChange

L'evento **DomainChange** si verifica quando viene modificato il dominio DVD.

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
| FirstPlay         | Esecuzione dell'inizializzazione predefinita di un disco DVD.                     |
| videoManagerMenu  | Visualizzazione dei menu per l'intero disco. Noto anche come menu radice o menu di scelta rapida. |
| videoTitleSetMenu | Visualizzazione dei menu per il set di titoli corrente. Noto anche come titleMenu.     |
| title             | Visualizzazione del titolo corrente.                                        |
| stop              | Il navigatore DVD si trova nel dominio di arresto DVD.                         |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Il valore dei parametri evento viene specificato da Windows Media Player ed è possibile accedervi o passarli a un metodo in un file JScript importato usando il nome del parametro specificato. Questo nome di parametro deve essere digitato esattamente come illustrato, incluse le maiuscole.

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

 

 





