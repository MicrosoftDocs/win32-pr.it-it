---
title: Network.encodedFrameRate
description: La proprietà encodedFrameRate recupera la frequenza fotogrammi video specificata dall'autore del contenuto in fotogrammi al secondo.
ms.assetid: 7dad5c90-f750-48d7-9dda-3fc07394edcc
keywords:
- Network.encodedFrameRate Windows Media Player
topic_type:
- apiref
api_name:
- Network.encodedFrameRate
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1f64b6f57b4cfd0e7bc94715f80c1066ebe23a601e64c173926cf2cd9e36393
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901701"
---
# <a name="networkencodedframerate"></a>Network.encodedFrameRate

La **proprietà encodedFrameRate** recupera la frequenza fotogrammi video specificata dall'autore del contenuto in fotogrammi al secondo.

## <a name="syntax"></a>Sintassi

*lettore*. *network*. **encodedFrameRate**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un numero di sola **lettura** (**long**).

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene utilizzata *la rete*. **encodedFrameRate per** visualizzare la frequenza dei fotogrammi specificata quando il file è stato codificato. Le informazioni vengono visualizzate in un DIV HTML creato con ID = "FR". **L'oggetto** Player è stato creato con ID = "Player".


```JScript
<!-- Create an event handler for play state. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   switch (NewState){
      case 3:
          // Display the encoded frame rate.
          FR.innerHTML = "Encoded Frame Rate: ";
          FR.innerHTML += Player.network.encodedFrameRate;
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

[**Network.frameRate**](network-framerate.md)
</dt> </dl>

 

 





