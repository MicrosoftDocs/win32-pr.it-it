---
title: Network.recoveredPackets
description: La proprietà recoveredPackets recupera il numero di pacchetti recuperati.
ms.assetid: ce10b906-2e8b-4b9f-83d0-56ba67cacd3f
keywords:
- Network.recoveredPackets Windows Media Player
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
ms.openlocfilehash: 464f7ad27603e506632d87254eaa4f76cbedf39ed15e353050cd13da0fa46204
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134934"
---
# <a name="networkrecoveredpackets"></a>Network.recoveredPackets

La **proprietà recoveredPackets** recupera il numero di pacchetti recuperati.

## <a name="syntax"></a>Sintassi

*lettore*. *network*. **recoveredPackets**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un numero di sola **lettura** (**long**).

## <a name="remarks"></a>Commenti

Ogni volta che la riproduzione viene arrestata e riavviata, questa proprietà viene impostata su zero. Non viene reimpostata se la riproduzione è sospesa.

Questa proprietà restituisce informazioni valide solo in fase di esecuzione e solo se *il lettore*. **Viene** impostata anche la proprietà URL. Sarà uguale a zero quando si usa il protocollo HTTP, che è senza perdita di dati.

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene utilizzata *la rete*. **recoveredPackets** per visualizzare il numero di pacchetti recuperati. Le informazioni vengono visualizzate in un DIV HTML creato con ID = "PR". Nell'esempio viene utilizzato un timer con un intervallo di 1 secondo per aggiornare la visualizzazione. **L'oggetto** Player è stato creato con ID = "Player".


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
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto di rete**](network-object.md)
</dt> <dt>

[**Player.URL**](player-url.md)
</dt> </dl>

 

 





