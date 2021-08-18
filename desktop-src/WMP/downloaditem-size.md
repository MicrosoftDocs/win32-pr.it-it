---
title: DownloadItem.size
description: Nota Questa sezione descrive le funzionalità progettate per l'uso da parte dei negozi online. L'uso di questa funzionalità all'esterno del contesto di un negozio online non è supportato. La proprietà size recupera le dimensioni del download.
ms.assetid: e0fd9cb5-155a-4159-94b8-1bf05b4d1062
keywords:
- DownloadItem.size Windows Media Player
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
ms.openlocfilehash: 046c48cc324b8d388d9f730dc3ed4d6739632d169d02d11c77201fe1da3e98c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117749722"
---
# <a name="downloaditemsize"></a>DownloadItem.size

> [!Note]  
> Questa sezione descrive le funzionalità progettate per l'uso da parte dei negozi online. L'uso di questa funzionalità all'esterno del contesto di un negozio online non è supportato.

 

La **proprietà size** recupera le dimensioni del download.

## <a name="syntax"></a>Sintassi

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).size
      
```

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un numero di sola **lettura** (**long**).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successive<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto DownloadItem**](downloaditem-object.md)
</dt> <dt>

[**DownloadItem.progress**](downloaditem-progress.md)
</dt> </dl>

 

 





