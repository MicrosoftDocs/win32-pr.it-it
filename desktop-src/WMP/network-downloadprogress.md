---
title: Network.downloadProgress
description: La proprietà downloadProgress recupera la percentuale di download completata.
ms.assetid: bb57ce84-babb-4dc2-bc2b-c40cbb587e91
keywords:
- Network.downloadProgress Windows Media Player
topic_type:
- apiref
api_name:
- Network.downloadProgress
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffc8d2707cd5fc24129363d53f9ee58fedf7b15c5da4eb5b80f032524ee66c09
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901721"
---
# <a name="networkdownloadprogress"></a>Network.downloadProgress

La **proprietà downloadProgress** recupera la percentuale di download completata.

## <a name="syntax"></a>Sintassi

*lettore*. *rete*. **downloadProgress**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un numero di sola **lettura** (**long**).

## <a name="remarks"></a>Commenti

Quando il controllo Windows Media Player è connesso a un file multimediale che può essere riprodotto e scaricato contemporaneamente, la proprietà **downloadProgress** restituisce la percentuale del file totale scaricato. Questa funzionalità è attualmente supportata solo nei server Web. I formati di file seguenti possono essere scaricati e riprodotti contemporaneamente:

-   Advanced Systems Format (ASF)
-   Windows Media Audio (WMA)
-   Windows Media Video (WMV)
-   MP3
-   Mpeg
-   WAV
-   Alcuni file AVI

Usare il *lettore*. **Evento di memorizzazione** nel buffer per determinare quando inizia e termina il download.

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene utilizzata *la rete*. **downloadProgress per** visualizzare la percentuale di download completato. Le informazioni vengono visualizzate in un DIV HTML creato con ID = "DP". L'esempio usa un timer con un intervallo di 1 secondo per aggiornare la visualizzazione. **L'oggetto Player** è stato creato con ID = "Player".


```JScript
<!-- Create an event handler for buffering. -->
<SCRIPT FOR = Player EVENT = buffering(Start)>
   var idI; // Variable for the interval id.
   
   // Test whether downloading has started or stopped.
   if (true == Start){ 
      // Start the timer. Call the function to update the display.
      idI = window.setInterval("UpdateDP()", 1000);
   }
   else{
      // Downloading is complete. Stop the timer.
      window.clearInterval(idI);
   }
</SCRIPT>

<!-- Put the function to update the display in a separate code block. -->
<SCRIPT>
function UpdateDP(){
   DP.innerHTML = "";
   DP.innerHTML = "Download progress: " + Player.network.downloadProgress;
   DP.innerHTML += " percent complete";
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

[**Oggetto Di rete**](network-object.md)
</dt> <dt>

[**Evento Player.Buffering**](player-player-buffering.md)
</dt> </dl>

 

 





