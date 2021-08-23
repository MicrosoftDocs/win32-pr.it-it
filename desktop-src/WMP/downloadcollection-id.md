---
title: DownloadCollection.id
description: Nota Questa sezione descrive le funzionalità progettate per l'uso da parte dei negozi online. L'uso di questa funzionalità al di fuori del contesto di un negozio online non è supportato. La proprietà id recupera l'ID della raccolta di download.
ms.assetid: b5b17f22-913c-4055-8958-e3efac819b2b
keywords:
- DownloadCollection.id Windows Media Player
topic_type:
- apiref
api_name:
- DownloadCollection.id
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97e505db2e643286f84b61bfa8604b9edc8ef36fa39cdd040bd9cc49bb98f82d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119651270"
---
# <a name="downloadcollectionid"></a>DownloadCollection.id

> [!Note]  
> Questa sezione descrive le funzionalità progettate per l'uso da parte dei negozi online. L'uso di questa funzionalità al di fuori del contesto di un negozio online non è supportato.

 

La **proprietà id** recupera l'ID della raccolta di download.

## <a name="syntax"></a>Sintassi

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).id
      
```

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un numero di sola **lettura** (**long**).

## <a name="remarks"></a>Commenti

Quando Download Manager crea una nuova raccolta di download, assegna alla raccolta un numero ID. I numeri ID vengono mantenuti tra Windows Media Player e le sessioni del sistema operativo.

I numeri ID non sono univoci. Tuttavia, nel valore a 32 bit sono disponibili numeri ID sufficienti che è estremamente improbabile che un numero ID esistente possa essere sovrascritto da uno nuovo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successive<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto DownloadCollection**](downloadcollection-object.md)
</dt> </dl>

 

 





