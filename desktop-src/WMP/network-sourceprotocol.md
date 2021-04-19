---
title: Rete. sourceProtocol
description: La proprietà sourceProtocol Recupera il protocollo di origine utilizzato per la ricezione dei dati.
ms.assetid: f09bbcd0-9c34-49d1-8080-247aed2548d5
keywords:
- Media Player di Windows Network. sourceProtocol
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
ms.openlocfilehash: 29e3f0ad63827605eb79a89325877e4bb83bfc62
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326329"
---
# <a name="networksourceprotocol"></a>Rete. sourceProtocol

La proprietà **sourceProtocol** Recupera il protocollo di origine utilizzato per la ricezione dei dati.

## <a name="syntax"></a>Sintassi

*Player*. *rete*. **sourceProtocol**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è una **stringa** di sola lettura.

## <a name="remarks"></a>Commenti

Questa proprietà è impostata su "" (stringa vuota) quando si esegue la riproduzione di file multimediali da un CD o un DVD.

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene utilizzata la *rete*. **sourceProtocol** per visualizzare il protocollo di origine utilizzato per la ricezione dei dati. Le informazioni vengono visualizzate in un DIV HTML creato con ID = "SP". L'oggetto **Player** è stato creato con ID = "Player".


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
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto di rete**](network-object.md)
</dt> </dl>

 

 





