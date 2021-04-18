---
title: Evento External. OnChangeViewOnlineListError
description: Si noti che in questo argomento viene descritta la funzionalità progettata per l'utilizzo da punti vendita online. | Evento External. OnChangeViewOnlineListError
ms.assetid: f53dfc80-a7d7-42b1-b390-e90aa108145f
keywords:
- Media Player di Windows dell'evento External. OnChangeViewOnlineListError
topic_type:
- apiref
api_name:
- External.OnChangeViewOnlineListError Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09e9ff854893268a00cb7b5f2fb35409be2e70e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331228"
---
# <a name="externalonchangeviewonlinelisterror-event"></a>Evento External. OnChangeViewOnlineListError

> [!Note]  
> Questo argomento descrive la funzionalità progettata per l'uso da punti vendita online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

L'evento **OnChangeViewOnlineListError** si verifica quando una chiamata al metodo [External. changeViewOnlineList](external-changeviewonlinelist.md) genera un errore.

``` syntax
window.external.OnChangeViewOnlineListError = functionname
```

## <a name="possible-values"></a>Valori possibili

Si tratta di una proprietà di sola scrittura che specifica il nome della funzione nello script che Windows Media Player chiama quando si verifica l'evento.

## <a name="parameters"></a>Parametri

La funzione che gestisce questo errore presenta i parametri seguenti.

<dl> <dt>

<span id="hr"></span><span id="HR"></span>*HR*
</dt> <dd>

Codice di errore **HRESULT** che indica il motivo dell'errore.

</dd> <dt>

<span id="LibraryLocationType"></span><span id="librarylocationtype"></span><span id="LIBRARYLOCATIONTYPE"></span>*LibraryLocationType*
</dt> <dd>

La stessa stringa passata nel parametro **LibraryLocationType** di **changeViewOnlineList**.

</dd> <dt>

<span id="LibraryLocationID"></span><span id="librarylocationid"></span><span id="LIBRARYLOCATIONID"></span>*LibraryLocationID*
</dt> <dd>

La stessa stringa passata nel parametro **LibraryLocationID** di **changeViewOnlineList**.

</dd> <dt>

<span id="Params"></span><span id="params"></span><span id="PARAMS"></span>*Params*
</dt> <dd>

La stessa stringa passata nel parametro **params** di **changeViewOnlineList**.

</dd> <dt>

<span id="FriendlyName"></span><span id="friendlyname"></span><span id="FRIENDLYNAME"></span>*FriendlyName*
</dt> <dd>

La stessa stringa passata nel parametro **FriendlyName** di **changeViewOnlineList**.

</dd> <dt>

<span id="ListType"></span><span id="listtype"></span><span id="LISTTYPE"></span>*ListType*
</dt> <dd>

La stessa stringa passata nel parametro **ListType** di **changeViewOnlineList**.

</dd> <dt>

<span id="ViewMode"></span><span id="viewmode"></span><span id="VIEWMODE"></span>*ViewMode*
</dt> <dd>

La stessa stringa passata nel parametro **ViewMode** di **changeViewOnlineList**.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto esterno per i negozi di tipo 1 online**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





