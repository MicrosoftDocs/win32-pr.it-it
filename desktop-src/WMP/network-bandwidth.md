---
title: Rete. larghezza di banda
description: La proprietà bandWidth recupera la larghezza di banda corrente della clip.
ms.assetid: 2ef86f2a-98e9-4544-a740-c2237f06c135
keywords:
- Media Player Windows per la larghezza di banda di rete
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
ms.openlocfilehash: 4783d86160070fc61202f97b4cf3882f2cebcfb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326122"
---
# <a name="networkbandwidth"></a>Rete. larghezza di banda

La proprietà **Bandwidth** recupera la larghezza di banda corrente della clip.

## <a name="syntax"></a>Sintassi

*Player*. *rete*. **larghezza di banda**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un **numero** di sola lettura (**Long**).

## <a name="remarks"></a>Commenti

Questa proprietà restituisce zero se il *lettore*. La proprietà **URL** non è impostata. Questa proprietà è valida solo per i flussi multimediali.

## <a name="examples"></a>Esempio

Nell'esempio Microsoft JScript seguente viene utilizzata la *rete*. **larghezza** di banda per visualizzare la larghezza di banda media corrente. Le informazioni vengono visualizzate in un DIV HTML creato con ID = "BW". L'oggetto **Player** è stato creato con ID = "Player".


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
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto di rete**](network-object.md)
</dt> <dt>

[**Player. URL**](player-url.md)
</dt> </dl>

 

 





