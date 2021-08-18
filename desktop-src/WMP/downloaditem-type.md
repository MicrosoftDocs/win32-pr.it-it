---
title: DownloadItem.type
description: Nota Questa sezione descrive le funzionalità progettate per l'uso da parte dei negozi online. L'uso di questa funzionalità all'esterno del contesto di un negozio online non è supportato. La proprietà type recupera il tipo di download.
ms.assetid: 58ffb8a3-5410-492b-bb0f-9130ed209b78
keywords:
- DownloadItem.type Windows Media Player
topic_type:
- apiref
api_name:
- DownloadItem.type
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 038f348093a512095ee930c4147024bc789ead5edd3498243eb83a01608bfac9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117749712"
---
# <a name="downloaditemtype"></a>DownloadItem.type

> [!Note]  
> Questa sezione descrive le funzionalità progettate per l'uso da parte dei negozi online. L'uso di questa funzionalità all'esterno del contesto di un negozio online non è supportato.

 

La **proprietà** type recupera il tipo di download.

## <a name="syntax"></a>Sintassi

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).type
      
```

## <a name="possible-values"></a>Valori possibili

Questa proprietà è una stringa di sola **lettura** contenente uno dei valori seguenti.



| Valore      | Descrizione                                                                                                                                                                            |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| background | (Windows solo XP. Il download viene eseguito come processo in background quando il tempo del processore diventa disponibile. Gli stati di download persistono anche quando Windows Media Player o Windows XP viene arrestato. |
| tempo reale  | (Tutti i sistemi operativi supportati). Il download viene eseguito tutti contemporaneamente. Gli stati di download non vengono mantenuti tra le sessioni.                                                                       |



 

## <a name="remarks"></a>Commenti

Ogni tipo di download presenta vantaggi e svantaggi. Il download in background consente all'utente di procedere ad altre attività e persino di riavviare Windows senza annullare il download, ma richiede più tempo nel complesso per completare il download ed è supportato solo per Windows XP. Il download in tempo reale richiede meno tempo, ma richiede all'utente di completare tutti i download prima di chiudere il Windows Media Player.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successive<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto DownloadItem**](downloaditem-object.md)
</dt> </dl>

 

 





