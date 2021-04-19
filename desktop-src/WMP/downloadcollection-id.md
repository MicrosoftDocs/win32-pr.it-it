---
title: DownloadCollection.id
description: Si noti che questa sezione descrive la funzionalità progettata per l'uso da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato. La proprietà ID recupera l'ID della raccolta di download.
ms.assetid: b5b17f22-913c-4055-8958-e3efac819b2b
keywords:
- Media Player Windows DownloadCollection.id
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
ms.openlocfilehash: 9edcca4f56c485951ca907ae228dfec7a958b308
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333419"
---
# <a name="downloadcollectionid"></a>DownloadCollection.id

> [!Note]  
> In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

La proprietà **ID** recupera l'ID della raccolta di download.

## <a name="syntax"></a>Sintassi

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).id
      
```

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un **numero** di sola lettura (**Long**).

## <a name="remarks"></a>Commenti

Quando Download Manager crea una nuova raccolta di download, assegna alla raccolta un numero ID. I numeri ID vengono mantenuti tra le sessioni di Windows Media Player e quelle del sistema operativo.

I numeri ID non sono univoci. Tuttavia, sono disponibili numeri ID sufficienti nel valore a 32 bit che è estremamente improbabile che un numero ID esistente venga sovrascritto da uno nuovo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Download (oggetto)**](downloadcollection-object.md)
</dt> </dl>

 

 





