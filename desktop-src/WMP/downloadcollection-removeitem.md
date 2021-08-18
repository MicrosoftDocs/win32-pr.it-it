---
title: Metodo DownloadCollection.removeItem
description: Nota Questa sezione descrive le funzionalità progettate per l'uso da parte dei negozi online. L'uso di questa funzionalità al di fuori del contesto di uno store online non è supportato. Il metodo removeItem rimuove un elemento di download da una raccolta di download.
ms.assetid: 0008752e-c81a-4f91-a582-9d6b46569479
keywords:
- Metodo removeItem Windows Media Player
- Metodo removeItem Windows Media Player , classe DownloadCollection
- Classe DownloadCollection Windows Media Player metodo , removeItem
topic_type:
- apiref
api_name:
- DownloadCollection.removeItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1d7eaa7b26a4d64070cae426d1bbc23418593fa8ec5472e870ed7529ce8a122
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997071"
---
# <a name="downloadcollectionremoveitem-method"></a>Metodo DownloadCollection.removeItem

> [!Note]  
> Questa sezione descrive le funzionalità progettate per l'uso da parte dei negozi online. L'uso di questa funzionalità al di fuori del contesto di uno store online non è supportato.

 

Il **metodo removeItem** rimuove un elemento di download da una raccolta di download.

## <a name="syntax"></a>Sintassi


```JScript
DownloadCollection.removeItem(
  itemID
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*itemID* \[ Pollici\]
</dt> <dd>

**Numero** (**long**) che specifica l'indice di **DownloadItem** da rimuovere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Se il download rappresentato da *itemID* è in corso, questo metodo annulla il download.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successive<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DownloadCollection.item**](downloadcollection-item.md)
</dt> <dt>

[**Oggetto DownloadCollection**](downloadcollection-object.md)
</dt> </dl>

 

 





