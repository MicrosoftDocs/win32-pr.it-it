---
title: Metodo DownloadCollection.item
description: Nota Questa sezione descrive le funzionalità progettate per l'uso da parte dei negozi online. L'uso di questa funzionalità all'esterno del contesto di un negozio online non è supportato. Il metodo item recupera un oggetto di download in sospeso.
ms.assetid: a79db9db-e80c-48db-aee6-9bd8f77a7dff
keywords:
- Metodo item Windows Media Player
- metodo item Windows Media Player , classe DownloadCollection
- Metodo della classe DownloadCollection Windows Media Player , item
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
ms.openlocfilehash: 8a82a903236038c2f0372786137eec48ad5c5f502d7fd614eb8944f3f4684aea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997041"
---
# <a name="downloadcollectionitem-method"></a>Metodo DownloadCollection.item

> [!Note]  
> Questa sezione descrive le funzionalità progettate per l'uso da parte dei negozi online. L'uso di questa funzionalità all'esterno del contesto di un negozio online non è supportato.

 

Il **metodo item** recupera un oggetto di download in sospeso.

## <a name="syntax"></a>Sintassi


```JScript
retVal = DownloadCollection.item(
  itemId
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*itemId* \[ Pollici\]
</dt> <dd>

**Numero** (**long**) che specifica l'indice di **DownloadItem** da recuperare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **oggetto DownloadItem.**

## <a name="remarks"></a>Commenti

Il *valore itemID* è in base zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successive<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto DownloadCollection**](downloadcollection-object.md)
</dt> <dt>

[**Oggetto DownloadItem**](downloaditem-object.md)
</dt> </dl>

 

 





