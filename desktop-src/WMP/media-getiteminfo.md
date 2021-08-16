---
title: Metodo Media.getItemInfo
description: Il metodo getItemInfo recupera il valore dell'attributo specificato per l'elemento multimediale corrente.
ms.assetid: a1ee0d40-b979-424b-bd4e-d1acf6354d8d
keywords:
- Metodo getItemInfo Windows Media Player
- Metodo getItemInfo Windows Media Player , classe Media
- Classe media Windows Media Player , metodo getItemInfo
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
ms.openlocfilehash: ab885a8505f3637d21f4a406e5a7c324ee6b9ec90e5ad0434a385e321072ccaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135154"
---
# <a name="mediagetiteminfo-method"></a>Metodo Media.getItemInfo

Il **metodo getItemInfo** recupera il valore dell'attributo specificato per l'elemento multimediale corrente.

## <a name="syntax"></a>Sintassi


```JScript
strRetVal = Media.getItemInfo(
  name
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*name* \[ Pollici\]
</dt> <dd>

**Stringa** contenente il nome dell'attributo. Per informazioni sugli attributi supportati da Windows Media Player, vedere le informazioni di riferimento Windows Media Player [attributi.](attribute-reference.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **valore String** che rappresenta il valore dell'attributo specificato. Per gli attributi il cui valore sottostante **è booleano,** restituisce la stringa "true" o "false".

## <a name="remarks"></a>Commenti

Questo metodo recupera i metadati per un singolo elemento multimediale digitale o un elemento multimediale che fa parte di una playlist.

La **proprietà attributeCount** contiene il numero di nomi di attributi disponibili per un determinato **oggetto Media.** I numeri di indice possono quindi essere usati con **il metodo getAttributeName** per determinare il nome di ogni attributo disponibile. I nomi dei singoli attributi possono essere passati **a getItemInfo.**

Per recuperare attributi con più valori e attributi con valori complessi, usare il **metodo getItemInfoByType.**

Per usare questo metodo, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [Accesso alla libreria.](library-access.md)

Per condividere le Windows multimediali su UPnP, Windows Media Player crea un servizio di directory del contenuto (CDS) esposto tramite UPnP. Gli altri dispositivi possono quindi esplorare ed esplorare le librerie.

In Windows 7 un'applicazione può usare gli attributi Windows Media Player [**TrackingID**](trackingid-attribute.md) e [**MediaType**](mediatype-attribute.md) per costruire l'ID oggetto di ogni elemento in CDS. Si noti che questa costruzione potrebbe cambiare nelle versioni future di Windows. L'applicazione passa ognuna di queste stringhe di attributo nel *parametro name* in una chiamata a **getItemInfo.** **getItemInfo** restituisce il valore per ogni attributo nel valore restituito. L'applicazione usa quindi la sintassi seguente per costruire ogni ID oggetto:

*TrackingID*.0. *MediaTypeID*

Questa sintassi ha il significato seguente:

-   *TrackingID* è la stringa archiviata nell'Windows Media Player [**TrackingID**](trackingid-attribute.md) dell'elemento multimediale.
-   *MediaTypeID* dipende dal valore [**dell'attributo MediaType,**](mediatype-attribute.md) come illustrato nella tabella seguente:

    | Attributo MediaType                      | MediaTypeID |
    |------------------------------------------|-------------|
    | [Elementi audio](audio-item-attributes.md) | 4           |
    | [Elementi foto](photo-item-attributes.md) | B           |
    | [Elementi video](video-item-attributes.md) | 8           |

    

     

**Windows Media Player 10 Mobile:** Gli attributi per un elemento multimediale sono disponibili solo durante la riproduzione, a meno che non vengano recuperati dall'elemento tramite la raccolta multimediale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto multimediale**](media-object.md)
</dt> <dt>

[**Media.attributeCount**](media-attributecount.md)
</dt> <dt>

[**Media.getAttributeName**](media-getattributename.md)
</dt> <dt>

[**Media.getItemInfoByType**](media-getiteminfobytype.md)
</dt> <dt>

[**Media.setItemInfo**](media-setiteminfo.md)
</dt> <dt>

[**Lettura dei valori degli attributi**](reading-attribute-values.md)
</dt> <dt>

[**Impostazioni.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Impostazioni.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





