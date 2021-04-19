---
title: DownloadManager. getdownloadcollection, metodo
description: Si noti che questa sezione descrive la funzionalità progettata per l'uso da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato. Il metodo getdownloadcollection recupera la raccolta di download specificata.
ms.assetid: 743d6bcf-2d5b-4a30-a4ef-4538cf7c901e
keywords:
- Metodo getdownloadcollection Media Player Windows
- Metodo getdownloadcollection Windows Media Player, classe DownloadManager
- Classe DownloadManager Media Player Windows, metodo getdownloadcollection
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
ms.openlocfilehash: 2e879d82c3f49db08d75b8aec37271e8d966019e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326013"
---
# <a name="downloadmanagergetdownloadcollection-method"></a>DownloadManager. getdownloadcollection, metodo

> [!Note]  
> In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

Il metodo **Getdownloadcollection** recupera la raccolta di download specificata.

## <a name="syntax"></a>Sintassi


```JScript
retVal = DownloadManager.getDownloadCollection(
  collectionId
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*CollectionId* \[ in\]
</dt> <dd>

**Numero** (**Long**) che specifica l'ID della raccolta di download da recuperare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un oggetto **DownloadCollection** .

## <a name="remarks"></a>Commenti

È prima necessario chiamare *downloadmanager*. **createDownloadCollection** per creare una nuova raccolta e recuperare il relativo valore ID.

Una raccolta di download esistente può contenere elementi che sono stati contrassegnati come annullati.

Gli elementi di download in tempo reale non completati in una sessione precedente non vengono recuperati come parte della raccolta. I download in background completati prima della sessione corrente rimangono nella raccolta di download fino a quando non vengono rimossi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto DownloadManager**](downloadmanager-object.md)
</dt> <dt>

[**DownloadManager. createDownloadCollection**](downloadmanager-createdownloadcollection.md)
</dt> <dt>

[**Download (oggetto)**](downloadcollection-object.md)
</dt> </dl>

 

 





