---
description: Ottiene l'elemento di ricerca per i dati specificati. Questo metodo viene chiamato una volta per ogni URL elaborato dal gatherer e recupera un puntatore all'oggetto ISearchItem.
ms.assetid: 35893bc9-8327-44f9-a9fc-7855c5c063e3
title: Metodo ISearchProtocolUI::GetSearchItemForUrl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchProtocolUI.GetSearchItemForUrl
api_type:
- COM
api_location: ''
ms.openlocfilehash: 8636f42026fe44131e149b0e378089b70c7d4f49b9e23b5d48ebe50aa5721d79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119594811"
---
# <a name="isearchprotocoluigetsearchitemforurl-method"></a>Metodo ISearchProtocolUI::GetSearchItemForUrl

Ottiene l'elemento di ricerca per i dati specificati. Questo metodo viene chiamato una volta per ogni URL elaborato dal gatherer e recupera un puntatore [**all'oggetto ISearchItem.**](-search-isearchitem.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSearchItemForUrl(
  [in]          LPCOLESTR        pcwszURL,
  [in]          IItemPropertyBag *pPropertyBag,
  [out, retval] ISearchItem      **ppSearchItem
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pcwszURL* \[ Pollici\]
</dt> <dd>

Tipo: **LPCOLESTR**

Puntatore a una stringa Unicode con terminazione di dati Null contenente l'elemento di ricerca per l'URL a cui si accede.

</dd> <dt>

*pPropertyBag* \[ Pollici\]
</dt> <dd>

Tipo: **IItemPropertyBag \***

Puntatore a [**un oggetto IItemPropertyBag**](iitempropertybag.md) che contiene informazioni sull'elemento di ricerca, incluse le proprietà dell'elemento.

</dd> <dt>

*ppSearchItem* \[ out, retval\]
</dt> <dd>

Tipo: **[ **ISearchItem**](-search-isearchitem.md)\*\***

Riceve l'indirizzo di un puntatore [**all'oggetto ISearchItem**](-search-isearchitem.md) creato da questo metodo. Questo oggetto contiene informazioni sull'elemento di ricerca, ad esempio il nome file dell'elemento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Il **metodo ISearchProtocolUI::GetSearchItemForUrl** è supportato solo in Windows XP e Windows Server 2003 e non deve più essere usato.

Per visualizzare in anteprima gli allegati con un gestore di protocollo di terze parti nei computer che eseguono Windows XP o Windows Server 2003, potrebbe essere necessario usare l'interfaccia [**ISearchProtocolUI**](-search-isearchprotocolui.md) e le API seguenti: le interfacce [**IItemPreviewerExt,**](-search-iitempreviewerext.md) [**IItemPropertyBag**](iitempropertybag.md) e [**ISearchItem,**](-search-isearchitem.md) la struttura [**LINKINFO**](-search-linkinfo.md) e l'enumerazione [**LINKTYPE.**](-search-linktype.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP solo con app desktop SP2 \[\]<br/> |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/> |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 3.0<br/>          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISearchProtocolUI**](-search-isearchprotocolui.md)
</dt> </dl>

 

 




