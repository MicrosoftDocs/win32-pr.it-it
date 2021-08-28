---
title: Metodo DownloadManager.getDownloadCollection
description: Nota Questa sezione descrive le funzionalità progettate per l'uso da parte dei negozi online. L'uso di questa funzionalità all'esterno del contesto di un negozio online non è supportato. Il metodo getDownloadCollection recupera la raccolta di download specificata.
ms.assetid: 743d6bcf-2d5b-4a30-a4ef-4538cf7c901e
keywords:
- Metodo getDownloadCollection Windows Media Player
- Metodo getDownloadCollection Windows Media Player , classe DownloadManager
- Metodo della classe DownloadManager Windows Media Player , getDownloadCollection
topic_type:
- apiref
api_name:
- DownloadManager.getDownloadCollection
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57fc729296f15b39e603683cab38e3d0d878733ab0990d9876e32b4001a15cf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117749621"
---
# <a name="downloadmanagergetdownloadcollection-method"></a>Metodo DownloadManager.getDownloadCollection

> [!Note]  
> Questa sezione descrive le funzionalità progettate per l'uso da parte dei negozi online. L'uso di questa funzionalità all'esterno del contesto di un negozio online non è supportato.

 

Il **metodo getDownloadCollection** recupera la raccolta di download specificata.

## <a name="syntax"></a>Sintassi


```JScript
retVal = DownloadManager.getDownloadCollection(
  collectionId
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*collectionId* \[ Pollici\]
</dt> <dd>

**Numero** (**long**) che specifica l'ID della raccolta di download da recuperare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **oggetto DownloadCollection.**

## <a name="remarks"></a>Commenti

È prima necessario chiamare *DownloadManager*. **createDownloadCollection per** creare una nuova raccolta e recuperarne il valore ID.

Una raccolta di download esistente può contenere elementi contrassegnati come annullati.

Gli elementi di download in tempo reale non completati in una sessione precedente non vengono recuperati come parte della raccolta. I download in background completati prima della sessione corrente rimangono nella raccolta di download fino a quando non vengono rimossi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successive<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto DownloadManager**](downloadmanager-object.md)
</dt> <dt>

[**DownloadManager. createDownloadCollection**](downloadmanager-createdownloadcollection.md)
</dt> <dt>

[**Oggetto DownloadCollection**](downloadcollection-object.md)
</dt> </dl>

 

 





