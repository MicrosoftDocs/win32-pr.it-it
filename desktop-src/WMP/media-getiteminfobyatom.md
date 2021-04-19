---
title: Media. getItemInfoByAtom, metodo
description: Il metodo getItemInfoByAtom Recupera il valore dell'attributo con il numero di indice specificato.
ms.assetid: 6e2dea0c-c722-4737-9e8e-f5cb74156cea
keywords:
- Metodo getItemInfoByAtom Windows Media Player
- Metodo getItemInfoByAtom Windows Media Player, classe media
- Media class Media Player Windows, metodo getItemInfoByAtom
topic_type:
- apiref
api_name:
- Media.getItemInfoByAtom
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf54d2ae177a65e1a71b5726090bba90f4ee4e5e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332550"
---
# <a name="mediagetiteminfobyatom-method"></a>Media. getItemInfoByAtom, metodo

Il metodo **getItemInfoByAtom** Recupera il valore dell'attributo con il numero di indice specificato.

## <a name="syntax"></a>Sintassi


```JScript
strRetVal = Media.getItemInfoByAtom(
  index
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Indice* \[ di in\]
</dt> <dd>

**Numero** (**Long**) che specifica l'indice in corrispondenza del quale si trova un determinato attributo nel set di attributi disponibili.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce una **stringa** che rappresenta il valore dell'attributo specificato. Per gli attributi il cui valore sottostante è **booleano**, viene restituita la stringa "true" o "false".

## <a name="remarks"></a>Commenti

Questo metodo può essere utilizzato per recuperare i metadati per un elemento multimediale digitale specifico utilizzando un numero di indice dell'attributo. È possibile utilizzare la proprietà **attributeCount** per determinare il numero di attributi disponibili per l'elemento multimediale.

Il metodo **getMediaAtom** dell'oggetto **mediacollection** può essere utilizzato anche per recuperare l'indice di un attributo specifico. Questa tecnica è in genere più efficiente rispetto ai metodi **GetItemInfo** o **getItemInfoByType** quando si lavora con playlist di grandi dimensioni.

Per usare questo metodo, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

Per informazioni sugli attributi supportati da Windows Media Player, vedere le informazioni di [riferimento sull'attributo](attribute-reference.md)Windows Media Player.

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

[**Media. getItemInfo**](media-getiteminfo.md)
</dt> <dt>

[**Media. getItemInfoByType**](media-getiteminfobytype.md)
</dt> <dt>

[**Media. setItemInfo**](media-setiteminfo.md)
</dt> <dt>

[**Mediacollection. getMediaAtom**](mediacollection-getmediaatom.md)
</dt> <dt>

[**Lettura di valori di attributo**](reading-attribute-values.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





