---
title: Rete. recoveredPackets
description: La proprietà recoveredPackets Recupera il numero di pacchetti ripristinati.
ms.assetid: ce10b906-2e8b-4b9f-83d0-56ba67cacd3f
keywords:
- Media Player di Windows Network. recoveredPackets
topic_type:
- apiref
api_name:
- Network.recoveredPackets
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a4222033d7e124e6ef29714bc47faf5664950fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328714"
---
# <a name="networkrecoveredpackets"></a>Rete. recoveredPackets

La proprietà **recoveredPackets** Recupera il numero di pacchetti ripristinati.

## <a name="syntax"></a>Sintassi

*Player*. *rete*. **recoveredPackets**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un **numero** di sola lettura (**Long**).

## <a name="remarks"></a>Commenti

Ogni volta che la riproduzione viene arrestata e riavviata, questa proprietà viene impostata su zero. Non viene reimpostato se la riproduzione viene sospesa.

Questa proprietà restituisce informazioni valide solo in fase di esecuzione e solo se il *lettore*. Viene impostata anche la proprietà **URL** . Sarà uguale a zero quando si usa il protocollo HTTP, che è lossless.

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene utilizzata la *rete*. **recoveredPackets** per visualizzare il numero di pacchetti ripristinati. Le informazioni vengono visualizzate in un DIV HTML creato con ID = "PR". Nell'esempio viene utilizzato un timer con un intervallo di 1 secondo per aggiornare la visualizzazione. L'oggetto **Player** è stato creato con ID = "Player".


```JScript
<!-- Create an event handler for play state change. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   var idI; // Variable for the interval id.

   // Test whether content is playing.
   if (3 == NewState){
      // Start the timer. Call the function to update the display every second.
      idI = window.setInterval("UpdatePR()", 1000);
   }
   else{
      // Not playing; stop the timer.
      window.clearInterval(idI);
   }   
</SCRIPT>

<!-- Put the function to update the display in a separate code block. -->
<SCRIPT>
function UpdatePR(){
   PR.innerHTML = "";
   PR.innerHTML = "Packets recovered: " + Player.network.recoveredPackets;
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

 

 





