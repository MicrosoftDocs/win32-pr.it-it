---
title: DVD. disponibile
description: La proprietà disavailable indica se è disponibile un tipo specificato di informazioni o se è possibile eseguire un'azione specificata. | DVD. disponibile
ms.assetid: ed34a943-b9c3-40a8-8845-b83f16951a3e
keywords:
- DVD. Media Player Windows disponibile
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
ms.openlocfilehash: 5088b4b6365dd60d859fda8ec563cc9c8ff8a4c8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321399"
---
# <a name="dvdisavailable"></a>DVD. disponibile

La proprietà **disavailable** indica se è disponibile un tipo specificato di informazioni o se è possibile eseguire un'azione specificata.

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
| Indietro       | Determina se il metodo **indietro** è disponibile.                                   |
| DVD        | Determina se il DVD è caricato.                                                  |
| dvdDecoder | Determina se il decoder DVD è installato nel sistema.                             |
| resume     | Determina se il metodo **Resume** è disponibile.                                 |
| titleMenu  | Determina se il metodo **titleMenu** è disponibile.                              |
| Menu di scelta rapida    | Determina se il metodo **tomenu** è disponibile. Comunemente chiamato menu radice. |



 

## <a name="return-values"></a>Valori restituiti

Questo metodo restituisce un **valore booleano** di sola lettura che indica se il parametro specificato è disponibile.

## <a name="remarks"></a>Commenti

Le funzionalità DVD di Windows Media Player non funzioneranno nei computer in cui non sono installati decodificatori DVD di terze parti. È possibile determinare se un decodificatore **è disponibile chiamando l'oggetto ("** dvdDecoder").

Ogni DVD viene creato in modo diverso. I metodi disponibili durante la riproduzione e la navigazione in DVD dipendono dal modo in cui viene creato il DVD.

**Windows Media Player 10 Mobile:** Questa proprietà restituisce sempre **false**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                               |
| Versione<br/>                  | Windows Media Player per Windows XP o versione successiva<br/>                            |
| DLL<br/>                      | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto DVD**](dvd-object.md)
</dt> </dl>

 

 





