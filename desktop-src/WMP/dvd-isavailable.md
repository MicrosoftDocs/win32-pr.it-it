---
title: DVD.isAvailable
description: La proprietà isAvailable indica se è disponibile un tipo specificato di informazioni o se è possibile eseguire un'azione specificata. | DVD.isAvailable
ms.assetid: ed34a943-b9c3-40a8-8845-b83f16951a3e
keywords:
- Dvd.isAvailable Windows Media Player
topic_type:
- apiref
api_name:
- DVD.isAvailable
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efb1a240c8df072d0770521f70c526f4e096c26385df85cff7acf0d229fdc252
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996921"
---
# <a name="dvdisavailable"></a>DVD.isAvailable

La **proprietà isAvailable** indica se è disponibile un tipo specificato di informazioni o se è possibile eseguire un'azione specificata.

``` syntax
player.dvd.isAvailable(
        name
        )
```

## <a name="parameters"></a>Parametri

*nome*

**Stringa** contenente uno dei valori seguenti.



| string     | Descrizione                                                                            |
|------------|----------------------------------------------------------------------------------------|
| Indietro       | Determina se il **metodo Back** è disponibile.                                   |
| Dvd        | Determina se il DVD è caricato.                                                  |
| dvdDecoder | Determina se il decodificatore DVD è installato nel sistema.                             |
| resume     | Determina se il **metodo resume** è disponibile.                                 |
| titleMenu  | Determina se il **metodo titleMenu** è disponibile.                              |
| TopMenu    | Determina se il **metodo topMenu** è disponibile. Comunemente denominato menu radice. |



 

## <a name="return-values"></a>Valori restituiti

Questo metodo restituisce un valore booleano **di** sola lettura che indica se il parametro specificato è disponibile.

## <a name="remarks"></a>Commenti

Le funzionalità DVD di Windows Media Player non funzionano nei computer in cui non sono installati decodificatori DVD di terze parti. È possibile determinare se un decodificatore è disponibile chiamando **isAvailable**("dvdDecoder").

Ogni DVD viene creato in modo diverso. I metodi disponibili durante la riproduzione e la navigazione dei DVD dipendono dalla modalità di creazione del DVD.

**Windows Media Player 10 Mobile:** Questa proprietà restituisce sempre **false.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                               |
| Versione<br/>                  | Windows Media Player per Windows XP o versioni successive<br/>                            |
| DLL<br/>                      | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto DVD**](dvd-object.md)
</dt> </dl>

 

 





