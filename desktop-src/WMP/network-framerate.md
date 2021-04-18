---
title: Rete. frameRate
description: La proprietà frameRate recupera la frequenza dei fotogrammi video corrente in frame per cento secondi. Ad esempio, il valore 2998 indica 29,98 fotogrammi al secondo.
ms.assetid: ee30dce5-a42e-4be5-ab4b-0d5f8869d23a
keywords:
- Media Player Windows di rete. frameRate
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
ms.openlocfilehash: 30ec6e16a3cef86a385525a793d73a50c3124e21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329442"
---
# <a name="networkframerate"></a>Rete. frameRate

La proprietà **framerate** recupera la frequenza dei fotogrammi video corrente in frame per cento secondi. Ad esempio, il valore 2998 indica 29,98 fotogrammi al secondo.

## <a name="syntax"></a>Sintassi

*Player*. *rete*. **framerate**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un **numero** di sola lettura (**Long**).

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene utilizzata la *rete*. **framerate** per visualizzare la frequenza dei fotogrammi corrente. Le informazioni vengono visualizzate in un DIV HTML creato con ID = "FR". L'oggetto **Player** è stato creato con ID = "Player".


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
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto di rete**](network-object.md)
</dt> <dt>

[**Rete. encodedFrameRate**](network-encodedframerate.md)
</dt> </dl>

 

 





