---
title: DVD. dominio
description: La proprietà del dominio recupera il dominio corrente del DVD.
ms.assetid: 74f4a6a3-8518-48c7-b023-f0255a3a62fd
keywords:
- DVD. dominio Windows Media Player
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
ms.openlocfilehash: db4a2af92abe533fed7a13e48cb7c0724223bbc1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340593"
---
# <a name="dvddomain"></a>DVD. dominio

La proprietà del **dominio** Recupera il dominio corrente del DVD.

``` syntax
player.dvd.domain
      
```

## <a name="possible-values"></a>Valori possibili

Questa proprietà è una **stringa** di sola lettura contenente uno dei valori seguenti.



| string            | Descrizione                                                                                                                           |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| firstPlay         | Esecuzione dell'inizializzazione predefinita di un disco DVD.                                                                                      |
| videoManagerMenu  | Visualizzazione dei menu per l'intero disco. Noto anche come menu di scelta rapida per Windows Media Player. Comunemente chiamato menu titolo o menu in alto. |
| videoTitleSetMenu | Visualizzazione dei menu per il set di titoli corrente. Noto anche come titleMenu per Windows Media Player. Comunemente chiamato menu radice.              |
| title             | In genere viene visualizzato il titolo corrente.                                                                                                 |
| stop              | Il navigatore DVD si trova nel dominio di arresto DVD.                                                                                          |
| Non definito         | Il lettore non è in nessun dominio DVD.                                                                                                      |



 

## <a name="remarks"></a>Commenti

Ogni DVD viene creato in modo diverso. Alcuni DVD non contengono i domini firstPlay, videoManagerMenu o videoTitleSetMenu.

**Windows Media Player 10 Mobile:** Questa proprietà restituisce sempre una stringa vuota.

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

 

 





