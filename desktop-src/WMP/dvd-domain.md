---
title: DVD.domain
description: La proprietà domain recupera il dominio corrente del DVD.
ms.assetid: 74f4a6a3-8518-48c7-b023-f0255a3a62fd
keywords:
- DVD.domain Windows Media Player
topic_type:
- apiref
api_name:
- DVD.domain
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0db8e6e212fec11de5f3619c2c1f97a90f579b34515983b0384d0d08ab0ff60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119651171"
---
# <a name="dvddomain"></a>DVD.domain

La **proprietà** domain recupera il dominio corrente del DVD.

``` syntax
player.dvd.domain
      
```

## <a name="possible-values"></a>Valori possibili

Questa proprietà è una stringa di sola **lettura** contenente uno dei valori seguenti.



| string            | Descrizione                                                                                                                           |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| firstPlay         | Esecuzione dell'inizializzazione predefinita di un disco DVD.                                                                                      |
| videoManagerMenu  | Visualizzazione dei menu per l'intero disco. Noto anche come topMenu per Windows Media Player. Comunemente chiamato menu del titolo o menu superiore. |
| videoTitleSetMenu | Visualizzazione dei menu per il set di titoli corrente. Noto anche come titleMenu per Windows Media Player. Comunemente chiamato menu radice.              |
| title             | In genere viene visualizzato il titolo corrente.                                                                                                 |
| stop              | Lo strumento di spostamento DVD si trova nel dominio DVD Stop.                                                                                          |
| Non definito         | Il lettore non si trova in alcun dominio DVD.                                                                                                      |



 

## <a name="remarks"></a>Commenti

Ogni DVD viene creato in modo diverso. Alcuni DVD non contengono i domini firstPlay, videoManagerMenu o videoTitleSetMenu.

**Windows Media Player 10 Mobile:** Questa proprietà restituisce sempre una stringa vuota.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                               |
| Versione<br/>                  | Windows Media Player per Windows XP o versione successiva<br/>                            |
| DLL<br/>                      | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto DVD**](dvd-object.md)
</dt> </dl>

 

 





