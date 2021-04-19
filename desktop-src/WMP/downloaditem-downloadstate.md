---
title: DownloadItem.downloadState
description: Si noti che questa sezione descrive la funzionalità progettata per l'uso da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato. La proprietà downloadState recupera lo stato del download.
ms.assetid: dde27f43-40ee-4eb9-b316-42312ee937d0
keywords:
- Media Player Windows DownloadItem. downloadState
topic_type:
- apiref
api_name:
- DownloadItem.downloadState
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbd2af2fab2ecb69df5b4695b227631b5be2dd96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333414"
---
# <a name="downloaditemdownloadstate"></a>DownloadItem.downloadState

> [!Note]  
> In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

La proprietà **downloadState** recupera lo stato del download.

## <a name="syntax"></a>Sintassi

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).downloadState
      
```

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un **numero** di sola lettura contenente uno dei valori seguenti.



| Valore | Descrizione |
|-------|-------------|
| 0     | Download in corso |
| 1     | Paused      |
| 2     | Elaborazione in corso  |
| 3     | Completato   |
| 4     | Cancellati    |



 

## <a name="remarks"></a>Commenti

Gli Stati di download possono essere eseguiti in qualsiasi ordine. Non scrivere codice che dipende dall'occorrenza di un particolare stato di download.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto DownloadItem**](downloaditem-object.md)
</dt> </dl>

 

 





