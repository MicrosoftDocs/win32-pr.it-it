---
title: Rete. lostPackets
description: La proprietà lostPackets Recupera il numero di pacchetti persi.
ms.assetid: b90faaaf-656a-4b9b-abfe-370e6f7c7c4b
keywords:
- Media Player di Windows Network. lostPackets
topic_type:
- apiref
api_name:
- Network.lostPackets
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a780afaea1ba46c5e2d5c7eb55b9476f68c9570
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328294"
---
# <a name="networklostpackets"></a>Rete. lostPackets

La proprietà **lostPackets** Recupera il numero di pacchetti persi.

## <a name="syntax"></a>Sintassi

*Player*. *rete*. **lostPackets**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un **numero** di sola lettura (**Long**).

## <a name="remarks"></a>Commenti

Questa proprietà è valida solo per i flussi multimediali e sarà uguale a zero quando si usa il protocollo HTTP, che è senza perdita di contenuti.

I pacchetti possono essere persi per diversi motivi, ad esempio il tipo e la qualità della connessione di rete.

Ogni volta che la riproduzione viene arrestata e riavviata, questa proprietà viene impostata su zero. Non viene reimpostato se la riproduzione viene sospesa e riavviata. Questa proprietà restituisce informazioni valide solo in fase di esecuzione e solo se il *lettore*. Viene impostata la proprietà **URL** .

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene utilizzata la *rete*. **lostPackets** per visualizzare il numero totale di pacchetti persi durante la riproduzione quando l'utente fa clic su un pulsante. Le informazioni vengono visualizzate in un DIV HTML creato con ID = "LP". L'oggetto **Player** è stato creato con ID = "Player".


```JScript
<!-- Create an HTML BUTTON element. -->
<INPUT TYPE = "BUTTON" ID = "lostpkts" NAME = "lostpkts"
       VALUE = "Count lost packets" 
       onClick = "LP.innerHTML = 'Packets lost: ' + Player.network.lostPackets;">

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

 

 





