---
title: DownloadItem. Progress
description: Si noti che questa sezione descrive la funzionalità progettata per l'uso da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato. La proprietà Progress recupera lo stato di avanzamento del download in byte.
ms.assetid: 58644eac-8dd0-4e9d-8055-03833c863a6e
keywords:
- Media Player di Windows DownloadItem. Progress
topic_type:
- apiref
api_name:
- DownloadItem.progress
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9a1967c1eb3dc72c00b8b10b70da5d797343e5f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326337"
---
# <a name="downloaditemprogress"></a>DownloadItem. Progress

> [!Note]  
> In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

La proprietà **Progress** recupera lo stato di avanzamento del download in byte.

## <a name="syntax"></a>Sintassi

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).progress
      
```

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un **numero** di sola lettura (**Long**).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto DownloadItem**](downloaditem-object.md)
</dt> <dt>

[**DownloadItem. size**](downloaditem-size.md)
</dt> </dl>

 

 





