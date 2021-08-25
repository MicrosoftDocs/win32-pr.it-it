---
title: Network.bufferingCount
description: La proprietà bufferingCount recupera il numero di volte in cui si è verificata la memorizzazione nel buffer durante la riproduzione di clip.
ms.assetid: 25a58795-161e-4290-8ea7-51acca968ef9
keywords:
- Network.bufferingCount Windows Media Player
topic_type:
- apiref
api_name:
- Network.bufferingCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d19c80715ca04965927bb0a50450213d707beeb124fd671fd8071e2cdd90e3a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901761"
---
# <a name="networkbufferingcount"></a>Network.bufferingCount

La **proprietà bufferingCount** recupera il numero di volte in cui si è verificata la memorizzazione nel buffer durante la riproduzione di clip.

## <a name="syntax"></a>Sintassi

*lettore*. *rete*. **bufferingCount**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un numero di sola **lettura** (**long**).

## <a name="remarks"></a>Commenti

Ogni volta che la riproduzione viene arrestata e riavviata, questa proprietà viene impostata su zero. Non viene reimpostata se la riproduzione è sospesa.

La memorizzazione nel buffer si applica solo al contenuto in streaming. Questa proprietà restituisce informazioni valide solo in fase di esecuzione quando l'oggetto *Player .* **La proprietà URL** è impostata.

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene utilizzata *la rete*. **bufferingCount per** visualizzare il numero di volte in cui si verifica la memorizzazione nel buffer durante la riproduzione. Le informazioni vengono visualizzate in un DIV HTML creato con ID = "CB". **L'oggetto Player** è stato creato con ID = "Player".


```JScript
<!-- Create an event handler. -->
<SCRIPT FOR = Player EVENT = buffering(Start)>
   if (true == Start) 
      CB.innerHTML = "Buffering count: " + Player.network.bufferingCount;
</SCRIPT>

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Di rete**](network-object.md)
</dt> <dt>

[**Player.URL**](player-url.md)
</dt> </dl>

 

 





