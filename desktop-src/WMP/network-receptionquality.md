---
title: Rete. receptionQuality
description: La proprietà receptionQuality recupera la percentuale di pacchetti ricevuti negli ultimi 30 secondi.
ms.assetid: 432f7f0a-0130-4485-b4a3-daa80ce9bb36
keywords:
- Media Player di Windows Network. receptionQuality
topic_type:
- apiref
api_name:
- Network.receptionQuality
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3706ba4d953f80c4a9e799971a7e73d49553c709
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331379"
---
# <a name="networkreceptionquality"></a>Rete. receptionQuality

La proprietà **receptionQuality** recupera la percentuale di pacchetti ricevuti negli ultimi 30 secondi.

## <a name="syntax"></a>Sintassi

*Player*. *rete*. **receptionQuality**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un **numero** di sola lettura (**Long**).

## <a name="remarks"></a>Commenti

Il numero di pacchetti ricevuti, persi e ripristinati durante il flusso viene monitorato una volta al secondo. **receptionQuality** è la percentuale di pacchetti non persi negli ultimi 30 secondi.

Ogni volta che la riproduzione viene arrestata e riavviata, questa proprietà viene impostata su zero. Non viene reimpostato se la riproduzione viene sospesa.

Questa proprietà restituisce informazioni valide solo in fase di esecuzione e solo se il *lettore*. Viene impostata anche la proprietà **URL** .

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene utilizzata la *rete*. **receptionQuality** per visualizzare la percentuale dei pacchetti ricevuti. Le informazioni vengono visualizzate in un DIV HTML creato con ID = "RQ". Nell'esempio viene utilizzato un timer con un intervallo di 30 secondi per aggiornare la visualizzazione. L'oggetto **Player** è stato creato con ID = "Player".


```JScript
<!-- Create an event handler for play state change. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   var idI; // Variable for the interval id.

   // Test whether content is playing.
   if (3 == NewState){
         // Start the timer. Update the display every 30 seconds.
         idI = window.setInterval("UpdateRQ()", 30000);
   }

      else{
         // Not playing; stop the timer.
         window.clearInterval(idI);
      }
</SCRIPT>

<!-- Put the function to update the display in a separate code block. -->
<SCRIPT>
function UpdateRQ(){
         RQ.innerHTML = "";
         RQ.innerHTML = "Reception quality: " + Player.network.receptionQuality;
         RQ.innerHTML += "%";         
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

 

 





