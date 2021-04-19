---
title: Rete. encodedFrameRate
description: La proprietà encodedFrameRate recupera la frequenza dei fotogrammi video specificata dall'autore del contenuto in frame al secondo.
ms.assetid: 7dad5c90-f750-48d7-9dda-3fc07394edcc
keywords:
- Media Player di Windows Network. encodedFrameRate
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
ms.openlocfilehash: 0008eb5d648dc7d3f51b40329ca3d830c3590c49
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330250"
---
# <a name="networkencodedframerate"></a>Rete. encodedFrameRate

La proprietà **encodedFrameRate** recupera la frequenza dei fotogrammi video specificata dall'autore del contenuto in frame al secondo.

## <a name="syntax"></a>Sintassi

*Player*. *rete*. **encodedFrameRate**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un **numero** di sola lettura (**Long**).

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene utilizzata la *rete*. **encodedFrameRate** consente di visualizzare la frequenza dei fotogrammi specificata quando il file è stato codificato. Le informazioni vengono visualizzate in un DIV HTML creato con ID = "FR". L'oggetto **Player** è stato creato con ID = "Player".


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
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto di rete**](network-object.md)
</dt> <dt>

[**Rete. frameRate**](network-framerate.md)
</dt> </dl>

 

 





