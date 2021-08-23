---
title: Network.bandWidth
description: La proprietà bandWidth recupera la larghezza di banda corrente del clip.
ms.assetid: 2ef86f2a-98e9-4544-a740-c2237f06c135
keywords:
- Network.bandWidth Windows Media Player
topic_type:
- apiref
api_name:
- Network.bandWidth
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40bd97ae2efe7513bc69d308a29356cfc7b141ecc84b816bdc7fad68d79aa785
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119616878"
---
# <a name="networkbandwidth"></a>Network.bandWidth

La **proprietà bandWidth** recupera la larghezza di banda corrente del clip.

## <a name="syntax"></a>Sintassi

*lettore*. *rete*. **bandWidth**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un numero di sola **lettura** (**long**).

## <a name="remarks"></a>Commenti

Questa proprietà restituisce zero se *l'oggetto Player*. **La proprietà URL** non è impostata. Questa proprietà è valida solo per i supporti di streaming.

## <a name="examples"></a>Esempio

Nell'esempio di Microsoft JScript seguente viene *utilizzata la rete*. **bandWidth** per visualizzare la larghezza di banda multimediale corrente. Le informazioni vengono visualizzate in un DIV HTML creato con ID = "BW". **L'oggetto** Player è stato creato con ID = "Player".


```JScript
<!-- Create an event handler for play state.-->
<SCRIPT FOR = Player EVENT = PlayStateChange()>

   switch (Player.playState){

      case 3:

         if (Player.network.bandwidth != 0){
  
            BW.innerHTML = "Current Bandwidth: " + Player.network.bandWidth;
            BW.innerHTML += " K bits/second";
         }

         else
            BW.innerHTML = "Bandwidth is only available for streaming media.";

            break;

      default:
}
</SCRIPT>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto di rete**](network-object.md)
</dt> <dt>

[**Player.URL**](player-url.md)
</dt> </dl>

 

 





