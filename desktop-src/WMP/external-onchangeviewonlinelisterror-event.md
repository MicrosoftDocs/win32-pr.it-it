---
title: Evento External.OnChangeViewOnlineListError
description: Nota Questo argomento descrive le funzionalità progettate per l'uso da parte dei negozi online. | Evento External.OnChangeViewOnlineListError
ms.assetid: f53dfc80-a7d7-42b1-b390-e90aa108145f
keywords:
- Evento External.OnChangeViewOnlineListError Windows Media Player
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
ms.openlocfilehash: 3ed6191de129bffea0e11abb24f1e271fc0b2873d2b306430a4e7eafe39b214d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648801"
---
# <a name="externalonchangeviewonlinelisterror-event"></a>Evento External.OnChangeViewOnlineListError

> [!Note]  
> In questo argomento vengono descritte le funzionalità progettate per l'utilizzo da parte dei negozi online. L'uso di questa funzionalità al di fuori del contesto di uno store online non è supportato.

 

**L'evento OnChangeViewOnlineListError** si verifica quando una chiamata al [metodo External.changeViewOnlineList](external-changeviewonlinelist.md) restituisce un errore.

``` syntax
window.external.OnChangeViewOnlineListError = functionname
```

## <a name="possible-values"></a>Valori possibili

Si tratta di una proprietà di sola scrittura che specifica il nome della funzione nello script che Windows Media Player chiama quando si verifica l'evento.

## <a name="parameters"></a>Parametri

La funzione che gestisce questo errore ha i parametri seguenti.

<dl> <dt>

<span id="hr"></span><span id="HR"></span>*Hr*
</dt> <dd>

Codice **di errore HRESULT** che indica il motivo dell'errore.

</dd> <dt>

<span id="LibraryLocationType"></span><span id="librarylocationtype"></span><span id="LIBRARYLOCATIONTYPE"></span>*LibraryLocationType*
</dt> <dd>

Stessa stringa passata nel parametro **LibraryLocationType** di **changeViewOnlineList.**

</dd> <dt>

<span id="LibraryLocationID"></span><span id="librarylocationid"></span><span id="LIBRARYLOCATIONID"></span>*LibraryLocationID*
</dt> <dd>

Stessa stringa passata nel parametro **LibraryLocationID** di **changeViewOnlineList.**

</dd> <dt>

<span id="Params"></span><span id="params"></span><span id="PARAMS"></span>*Params*
</dt> <dd>

Stessa stringa passata nel parametro **Params** di **changeViewOnlineList.**

</dd> <dt>

<span id="FriendlyName"></span><span id="friendlyname"></span><span id="FRIENDLYNAME"></span>*Friendlyname*
</dt> <dd>

Stessa stringa passata nel parametro **FriendlyName** di **changeViewOnlineList.**

</dd> <dt>

<span id="ListType"></span><span id="listtype"></span><span id="LISTTYPE"></span>*ListType*
</dt> <dd>

Stessa stringa passata nel parametro **ListType** di **changeViewOnlineList.**

</dd> <dt>

<span id="ViewMode"></span><span id="viewmode"></span><span id="VIEWMODE"></span>*Viewmode*
</dt> <dd>

Stessa stringa passata nel parametro **ViewMode** di **changeViewOnlineList.**

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto esterno per i negozi online di tipo 1**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





