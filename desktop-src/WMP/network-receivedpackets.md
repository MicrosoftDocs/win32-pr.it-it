---
title: Rete. receivedPackets
description: La proprietà receivedPackets Recupera il numero di pacchetti ricevuti.
ms.assetid: db4f6f08-c248-4db8-ab19-fdd5d2794085
keywords:
- Media Player di Windows Network. receivedPackets
topic_type:
- apiref
api_name:
- Network.receivedPackets
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bc792330cd107ca428ad0fbec930fe262a2f131
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331382"
---
# <a name="networkreceivedpackets"></a>Rete. receivedPackets

La proprietà **receivedPackets** Recupera il numero di pacchetti ricevuti.

## <a name="syntax"></a>Sintassi

*Player*. *rete*. **receivedPackets**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un **numero** di sola lettura (**Long**).

## <a name="remarks"></a>Commenti

Ogni volta che la riproduzione clip viene arrestata e riavviata, questa proprietà viene impostata su zero. Non viene reimpostato se la riproduzione del file viene sospesa.

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene utilizzata la *rete*. **receivedPackets** per visualizzare il numero di pacchetti ricevuti. Le informazioni vengono visualizzate in un DIV HTML creato con ID = "RP". Nell'esempio viene utilizzato un timer con un intervallo di 1 secondo per aggiornare la visualizzazione. L'oggetto **Player** è stato creato con ID = "Player".


```JScript
<!-- Create an event handler for play state change. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>

   var idI; // Variable for the interval id.

   // Test whether packets may be arriving.
   switch (NewState){
      case 1, 2, 4, 5, 7, 8, 9:
          window.clearInterval(idI);
          break;

      default:
         idI = window.setInterval("UpdateRP()", 1000);

   }</SCRIPT>

<!-- Put the function to update the display in a separate code block. -->
<SCRIPT>
function UpdateRP(){
   RP.innerHTML = "";
   RP.innerHTML = "Packets received: " + Player.network.receivedPackets;         
}

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

 

 





