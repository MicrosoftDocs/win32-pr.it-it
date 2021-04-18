---
title: Metodo DownloadCollection. Item
description: Si noti che questa sezione descrive la funzionalità progettata per l'uso da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato. Il metodo Item recupera un oggetto download in sospeso.
ms.assetid: a79db9db-e80c-48db-aee6-9bd8f77a7dff
keywords:
- Metodo Item Media Player Windows
- Metodo Item Media Player Windows, classe DownloadCollection
- Scaricacollection (classe) Windows Media Player, metodo Item
topic_type:
- apiref
api_name:
- DownloadCollection.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d57db60a776c71d9ff16eceb1584c79a125bbf46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331486"
---
# <a name="downloadcollectionitem-method"></a>Metodo DownloadCollection. Item

> [!Note]  
> In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

Il metodo **Item** recupera un oggetto download in sospeso.

## <a name="syntax"></a>Sintassi


```JScript
retVal = DownloadCollection.item(
  itemId
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ID* \[ elemento in\]
</dt> <dd>

**Numero** (**Long**) che specifica l'indice di **DownloadItem** da recuperare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un oggetto **DownloadItem** .

## <a name="remarks"></a>Commenti

Il valore *ItemId* è in base zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Download (oggetto)**](downloadcollection-object.md)
</dt> <dt>

[**Oggetto DownloadItem**](downloaditem-object.md)
</dt> </dl>

 

 





