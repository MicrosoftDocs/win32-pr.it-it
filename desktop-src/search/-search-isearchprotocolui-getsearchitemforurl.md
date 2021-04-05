---
description: Ottiene l'elemento di ricerca per i dati specificati. Questo metodo viene chiamato una volta per ogni URL elaborato dal gatherer e recupera un puntatore all'oggetto ISearchItem.
ms.assetid: 35893bc9-8327-44f9-a9fc-7855c5c063e3
title: 'Metodo ISearchProtocolUI:: GetSearchItemForUrl'
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
ms.openlocfilehash: f8a9bbe3459109946b7a4789d9b9f0fb7473ff05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750399"
---
# <a name="isearchprotocoluigetsearchitemforurl-method"></a>Metodo ISearchProtocolUI:: GetSearchItemForUrl

Ottiene l'elemento di ricerca per i dati specificati. Questo metodo viene chiamato una volta per ogni URL elaborato dal gatherer e recupera un puntatore all'oggetto [**ISearchItem**](-search-isearchitem.md) .

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

*pcwszURL* \[ in\]
</dt> <dd>

Tipo: **LPCOLESTR**

Puntatore a una stringa Unicode con terminazione di dati null contenente l'elemento di ricerca per l'URL a cui si accede.

</dd> <dt>

*pPropertyBag* \[ in\]
</dt> <dd>

Tipo: **IItemPropertyBag \** _

Puntatore a un oggetto [_ *IItemPropertyBag* *](iitempropertybag.md) che contiene informazioni sull'elemento di ricerca, incluse le proprietà dell'elemento.

</dd> <dt>

*ppSearchItem* \[ out, retval\]
</dt> <dd>

Tipo: **[ **ISearchItem**](-search-isearchitem.md)\*\***

Riceve l'indirizzo di un puntatore all'oggetto [**ISearchItem**](-search-isearchitem.md) creato da questo metodo. Questo oggetto contiene informazioni sull'elemento di ricerca, ad esempio il nome del file dell'elemento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Il metodo **ISearchProtocolUI:: GetSearchItemForUrl** è supportato solo in Windows XP e windows Server 2003 e non deve più essere usato.

Per visualizzare in anteprima gli allegati con un gestore di protocollo di terze parti in computer che eseguono Windows XP o Windows Server 2003, potrebbe essere necessario usare l'interfaccia [**ISearchProtocolUI**](-search-isearchprotocolui.md) e le API seguenti: le interfacce [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md) e [**ISearchItem**](-search-isearchitem.md) , la struttura [**LINKINFO**](-search-linkinfo.md) e l'enumerazione [**LinkType**](-search-linktype.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP con SP2 \[\]<br/> |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/> |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 3,0<br/>          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISearchProtocolUI**](-search-isearchprotocolui.md)
</dt> </dl>

 

 




