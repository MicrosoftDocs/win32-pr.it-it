---
title: Metodo DownloadCollection. removeItem
description: Si noti che questa sezione descrive la funzionalità progettata per l'uso da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato. Il metodo removeItem rimuove un elemento di download da una raccolta di download.
ms.assetid: 0008752e-c81a-4f91-a582-9d6b46569479
keywords:
- Metodo removeItem Windows Media Player
- Metodo removeItem Windows Media Player, classe DownloadCollection
- Scaricacollection (classe) Windows Media Player, metodo removeItem
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
ms.openlocfilehash: a1798665b79327b7956c1b78509b55cc6e6dd70c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333417"
---
# <a name="downloadcollectionremoveitem-method"></a>Metodo DownloadCollection. removeItem

> [!Note]  
> In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

Il metodo **RemoveItem** rimuove un elemento di download da una raccolta di download.

## <a name="syntax"></a>Sintassi


```JScript
DownloadCollection.removeItem(
  itemID
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ID* \[ elemento in\]
</dt> <dd>

**Numero** (**Long**) che specifica l'indice del **DownloadItem** da rimuovere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Se è in corso il download rappresentato da *ItemId* , questo metodo annulla il download.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DownloadCollection. Item**](downloadcollection-item.md)
</dt> <dt>

[**Download (oggetto)**](downloadcollection-object.md)
</dt> </dl>

 

 





