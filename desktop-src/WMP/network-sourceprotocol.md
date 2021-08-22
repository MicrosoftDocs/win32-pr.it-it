---
title: Network.sourceProtocol
description: La proprietà sourceProtocol recupera il protocollo di origine usato per ricevere i dati.
ms.assetid: f09bbcd0-9c34-49d1-8080-247aed2548d5
keywords:
- Network.sourceProtocol Windows Media Player
topic_type:
- apiref
api_name:
- Network.sourceProtocol
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f23cba2fdd56c1076110c495f7dab2451b7fa103e1dd0e0253e4f74f4f8ab59f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118836217"
---
# <a name="networksourceprotocol"></a>Network.sourceProtocol

La **proprietà sourceProtocol** recupera il protocollo di origine usato per ricevere i dati.

## <a name="syntax"></a>Sintassi

*lettore*. *network*. **sourceProtocol**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è una stringa di sola **lettura.**

## <a name="remarks"></a>Commenti

Questa proprietà è impostata su "" (stringa vuota) durante la riproduzione di supporti da un CD o DVD.

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene utilizzata *la rete*. **sourceProtocol per** visualizzare il protocollo di origine usato per ricevere i dati. Le informazioni vengono visualizzate in un DIV HTML creato con ID = "SP". **L'oggetto** Player è stato creato con ID = "Player".


```JScript
<!-- Create an event handler for play state change. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   if (3 == NewState){
     SP.innerHTML = "Source protocol: " + Player.network.sourceProtocol;
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
</dt> </dl>

 

 





