---
title: Rete. bufferingProgress
description: La proprietà bufferingProgress recupera la percentuale di memorizzazione nel buffer completata.
ms.assetid: d604159b-7c42-47f8-8085-53f859f24703
keywords:
- Media Player di Windows Network. bufferingProgress
topic_type:
- apiref
api_name:
- Network.bufferingProgress
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e3a4f37f8f6b8ffe8ff93ca72b0c9551d7e314
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326114"
---
# <a name="networkbufferingprogress"></a>Rete. bufferingProgress

La proprietà **bufferingProgress** recupera la percentuale di memorizzazione nel buffer completata.

## <a name="syntax"></a>Sintassi

*Player*. *rete*. **bufferingProgress**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un **numero** di sola lettura (**Long**).

## <a name="remarks"></a>Commenti

Ogni volta che la riproduzione viene arrestata e riavviata, questa proprietà viene impostata su zero. Non viene reimpostato se la riproduzione viene sospesa.

Il buffering si applica solo ai contenuti in streaming. Questa proprietà restituisce informazioni valide solo in fase di esecuzione, quando il *lettore*. Viene impostata la proprietà **URL** .

Usare l'evento *Player*. * * * * buffering * * * * per determinare quando il buffering viene avviato o interrotto.

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene utilizzata la *rete*. **bufferingProgress** per visualizzare la percentuale di memorizzazione nel buffer completata. Le informazioni vengono visualizzate in un DIV HTML creato con ID = "BP". Nell'esempio viene utilizzato un timer con un intervallo di 1 secondo per aggiornare la visualizzazione. L'oggetto **Player** è stato creato con ID = "Player".


```JScript
<!-- Create an event handler for buffering. -->
<SCRIPT FOR = Player EVENT = buffering(Start)>
   var idI; // Variable for the interval id.

   // Test whether buffering has started or stopped.
   if (true == Start){ 
      // Start the timer. Call the function to update the display every second.
      idI = window.setInterval("UpdateBP()", 1000);
   }

   else{
      // Buffering is complete. Stop the timer.
      window.clearInterval(idI);
   }
</SCRIPT>

<!-- Put the function to update the display in a separate code block. -->
<SCRIPT>
function UpdateBP(){
   BP.innerHTML = "";
   BP.innerHTML = "Buffering progress: " + Player.network.bufferingProgress;
   BP.innerHTML += " percent complete";
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

[**Evento Player. buffering**](player-player-buffering.md)
</dt> <dt>

[**Player. URL**](player-url.md)
</dt> </dl>

 

 





