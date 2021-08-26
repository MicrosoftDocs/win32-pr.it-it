---
title: Network.frameRate
description: La proprietà frameRate recupera la frequenza dei fotogrammi video corrente in fotogrammi per cento secondi. Ad esempio, un valore pari a 2998 indica 29,98 fotogrammi al secondo.
ms.assetid: ee30dce5-a42e-4be5-ab4b-0d5f8869d23a
keywords:
- Network.frameRate Windows Media Player
topic_type:
- apiref
api_name:
- Network.frameRate
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4da4a0f292c4693c263115dc1ad59ea3c71946d81838d427e6d8e043ac499709
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901651"
---
# <a name="networkframerate"></a>Network.frameRate

La **proprietà frameRate** recupera la frequenza dei fotogrammi video corrente in fotogrammi per cento secondi. Ad esempio, un valore pari a 2998 indica 29,98 fotogrammi al secondo.

## <a name="syntax"></a>Sintassi

*lettore*. *rete*. **frameRate**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un numero di sola **lettura** (**long**).

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene utilizzata *la rete*. **frameRate** per visualizzare la frequenza dei fotogrammi corrente. Le informazioni vengono visualizzate in un DIV HTML creato con ID = "FR". **L'oggetto Player** è stato creato con ID = "Player".


```JScript
<!-- Create an event handler for play state. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   switch (NewState){
      case 3:
          // Display the current frame rate.
          FR.innerHTML = "Frame Rate: ";
          FR.innerHTML += Player.network.frameRate;
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

[**Oggetto Di rete**](network-object.md)
</dt> <dt>

[**Network.encodedFrameRate**](network-encodedframerate.md)
</dt> </dl>

 

 





