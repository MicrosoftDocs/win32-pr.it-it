---
title: DownloadItem. size
description: Si noti che questa sezione descrive la funzionalità progettata per l'uso da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato. La proprietà Size recupera le dimensioni del download.
ms.assetid: e0fd9cb5-155a-4159-94b8-1bf05b4d1062
keywords:
- DownloadItem. Size Media Player Windows
topic_type:
- apiref
api_name:
- DownloadItem.size
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0ebb1ce15d34ad04095f1ef1ed84ad2df008c7e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328721"
---
# <a name="downloaditemsize"></a>DownloadItem. size

> [!Note]  
> In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

La proprietà **size** recupera le dimensioni del download.

## <a name="syntax"></a>Sintassi

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).size
      
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

[**DownloadItem. Progress**](downloaditem-progress.md)
</dt> </dl>

 

 





