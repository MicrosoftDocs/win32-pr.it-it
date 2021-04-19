---
title: Media. getItemInfo, metodo
description: Il metodo getItemInfo Recupera il valore dell'attributo specificato per l'elemento multimediale corrente.
ms.assetid: a1ee0d40-b979-424b-bd4e-d1acf6354d8d
keywords:
- metodo getItemInfo Windows Media Player
- metodo getItemInfo Windows Media Player, classe media
- Media class Media Player Windows, metodo getItemInfo
topic_type:
- apiref
api_name:
- Media.getItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef7e7348e73e3550ed668f6694ccfe9ed615215b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332552"
---
# <a name="mediagetiteminfo-method"></a>Media. getItemInfo, metodo

Il metodo **GetItemInfo** Recupera il valore dell'attributo specificato per l'elemento multimediale corrente.

## <a name="syntax"></a>Sintassi


```JScript
strRetVal = Media.getItemInfo(
  name
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*nome* \[ in\]
</dt> <dd>

**Stringa** contenente il nome dell'attributo. Per informazioni sugli attributi supportati da Windows Media Player, vedere la Guida di [riferimento](attribute-reference.md)agli attributi di Windows Media Player.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce una **stringa** che rappresenta il valore dell'attributo specificato. Per gli attributi il cui valore sottostante è **booleano**, viene restituita la stringa "true" o "false".

## <a name="remarks"></a>Commenti

Questo metodo recupera i metadati per un singolo elemento multimediale digitale o un elemento multimediale che fa parte di una playlist.

La proprietà **attributeCount** contiene il numero di nomi di attributi disponibili per un determinato oggetto **multimediale** . I numeri di indice possono quindi essere usati con il metodo **GetAttribute** per determinare il nome di ogni attributo disponibile. I singoli nomi di attributo possono essere passati a **GetItemInfo**.

Per recuperare gli attributi con più valori e attributi con valori complessi, usare il metodo **getItemInfoByType** .

Per usare questo metodo, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

Per condividere le librerie di Windows Media tramite UPnP, Windows Media Player crea un servizio directory contenuto (CDS) esposto tramite UPnP. Gli altri dispositivi potranno quindi navigare ed esplorare le librerie.

In Windows 7, un'applicazione può usare gli attributi Windows Media Player [**TrackingId**](trackingid-attribute.md) e [**mediaType**](mediatype-attribute.md) per costruire l'ID oggetto di ogni elemento in CDS. Si noti che questa costruzione potrebbe cambiare nelle versioni future di Windows. L'applicazione passa ogni stringa di attributo nel parametro *Name* in una chiamata a **GetItemInfo**. **GetItemInfo** restituisce il valore per ogni attributo nel valore restituito. L'applicazione usa quindi la sintassi seguente per costruire ogni ID oggetto:

*TrackingId*. 0. *MediaTypeID*

Questa sintassi ha il significato seguente:

-   *TrackingId* è la stringa archiviata nell'attributo Windows Media Player [**TrackingId**](trackingid-attribute.md) dell'elemento multimediale.
-   *MediaTypeID* dipende dal valore dell'attributo [**mediaType**](mediatype-attribute.md) , come illustrato nella tabella seguente:

    | Attributo MediaType                      | MediaTypeID |
    |------------------------------------------|-------------|
    | [Elementi audio](audio-item-attributes.md) | 4           |
    | [Elementi foto](photo-item-attributes.md) | B           |
    | [Elementi video](video-item-attributes.md) | 8           |

    

     

**Windows Media Player 10 Mobile:** Gli attributi per un elemento multimediale sono disponibili solo durante la riproduzione, a meno che non vengano recuperati dall'elemento tramite la raccolta di supporti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto multimediale**](media-object.md)
</dt> <dt>

[**Media. attributeCount**](media-attributecount.md)
</dt> <dt>

[**Media. GetAttribute**](media-getattributename.md)
</dt> <dt>

[**Media. getItemInfoByType**](media-getiteminfobytype.md)
</dt> <dt>

[**Media. setItemInfo**](media-setiteminfo.md)
</dt> <dt>

[**Lettura di valori di attributo**](reading-attribute-values.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





