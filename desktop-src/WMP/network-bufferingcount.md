---
title: Rete. bufferingCount
description: La proprietà bufferingCount Recupera il numero di volte in cui si è verificato il buffer durante la riproduzione della clip.
ms.assetid: 25a58795-161e-4290-8ea7-51acca968ef9
keywords:
- Media Player di Windows Network. bufferingCount
topic_type:
- apiref
api_name:
- Network.bufferingCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 524dc66c7f4ed1d413f264a91ae9385d458d632b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326118"
---
# <a name="networkbufferingcount"></a>Rete. bufferingCount

La proprietà **bufferingCount** Recupera il numero di volte in cui si è verificato il buffer durante la riproduzione della clip.

## <a name="syntax"></a>Sintassi

*Player*. *rete*. **bufferingCount**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un **numero** di sola lettura (**Long**).

## <a name="remarks"></a>Commenti

Ogni volta che la riproduzione viene arrestata e riavviata, questa proprietà viene impostata su zero. Non viene reimpostato se la riproduzione viene sospesa.

Il buffering si applica solo ai contenuti in streaming. Questa proprietà restituisce informazioni valide solo in fase di esecuzione quando il *lettore*. Viene impostata la proprietà **URL** .

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene utilizzata la *rete*. **bufferingCount** per visualizzare il numero di volte in cui si verifica il buffer durante la riproduzione. Le informazioni vengono visualizzate in un DIV HTML creato con ID = "CB". L'oggetto **Player** è stato creato con ID = "Player".


```JScript
<!-- Create an event handler. -->
<SCRIPT FOR = Player EVENT = buffering(Start)>
   if (true == Start) 
      CB.innerHTML = "Buffering count: " + Player.network.bufferingCount;
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

 

 





