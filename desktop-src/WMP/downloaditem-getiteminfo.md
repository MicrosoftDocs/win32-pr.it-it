---
title: DownloadItem. getItemInfo, metodo
description: Si noti che questa sezione descrive la funzionalità progettata per l'uso da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato. Il metodo getItemInfo Recupera il valore di un attributo per l'elemento di download.
ms.assetid: da885611-b4a0-4264-8b32-13cc6f87d6e9
keywords:
- metodo getItemInfo Windows Media Player
- metodo getItemInfo Windows Media Player, classe DownloadItem
- Classe DownloadItem Windows Media Player, metodo getItemInfo
topic_type:
- apiref
api_name:
- DownloadItem.getItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1367e5c7a8990a9172ee758d2b811b9074ed02fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326345"
---
# <a name="downloaditemgetiteminfo-method"></a>DownloadItem. getItemInfo, metodo

> [!Note]  
> In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

Il metodo **GetItemInfo** Recupera il valore di un attributo per l'elemento di download.

## <a name="syntax"></a>Sintassi


```JScript
strRetVal = DownloadItem.getItemInfo(
  itemname
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ItemName* \[ in\]
</dt> <dd>

**Stringa** contenente il nome dell'attributo. I valori supportati sono AlbumArtist, album, Duration, WM/provider, title, UserRating e WM/numero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce una **stringa** contenente il valore dell'attributo specificato da *ItemName*.

## <a name="remarks"></a>Commenti

Questo metodo recupera gli attributi specificati usando la stringa di descrizione BITS. Vedere la [convenzione di processo di Windows Media Player bits](windows-media-player-bits-job-convention.md).

Questo metodo è supportato per il download in background. Il codice non deve chiamare questo metodo quando si usa il download in tempo reale.

Questo metodo consente di recuperare informazioni per i processi BITS aggiunti solo durante la sessione corrente di Windows Media Player.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 10 o versione successiva<br/>                                        |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DownloadItem. Type**](downloaditem-type.md)
</dt> <dt>

[**Oggetto DownloadItem**](downloaditem-object.md)
</dt> </dl>

 

 





