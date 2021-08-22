---
title: Network.receivedPackets
description: La proprietà receivedPackets recupera il numero di pacchetti ricevuti.
ms.assetid: db4f6f08-c248-4db8-ab19-fdd5d2794085
keywords:
- Network.receivedPackets Windows Media Player
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
ms.openlocfilehash: ca9544332fa6e81211dae45cddc74ce9daee0d47e70d467137aaca2084bbc6f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054499"
---
# <a name="networkreceivedpackets"></a>Network.receivedPackets

La **proprietà receivedPackets** recupera il numero di pacchetti ricevuti.

## <a name="syntax"></a>Sintassi

*lettore*. *network*. **receivedPackets**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un numero di sola **lettura** (**long**).

## <a name="remarks"></a>Commenti

Ogni volta che la riproduzione del clip viene arrestata e riavviata, questa proprietà è impostata su zero. Non viene reimpostata se la riproduzione dei file è sospesa.

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene utilizzata *la rete*. **receivedPackets** per visualizzare il numero di pacchetti ricevuti. Le informazioni vengono visualizzate in un DIV HTML creato con ID = "RP". Nell'esempio viene utilizzato un timer con un intervallo di 1 secondo per aggiornare la visualizzazione. **L'oggetto** Player è stato creato con ID = "Player".


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
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto di rete**](network-object.md)
</dt> </dl>

 

 





