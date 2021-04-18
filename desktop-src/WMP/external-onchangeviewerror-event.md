---
title: Evento External. OnChangeViewError
description: Si noti che in questo argomento viene descritta la funzionalità progettata per l'utilizzo da punti vendita online. | Evento External. OnChangeViewError
ms.assetid: d6370629-5f50-434d-8eb5-5b43d1b2f7fe
keywords:
- Media Player di Windows dell'evento External. OnChangeViewError
topic_type:
- apiref
api_name:
- External.OnChangeViewError Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91bcbb71e1c5324a9907d735492364561be49a60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331229"
---
# <a name="externalonchangeviewerror-event"></a>Evento External. OnChangeViewError

> [!Note]  
> Questo argomento descrive la funzionalità progettata per l'uso da punti vendita online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

L'evento **OnChangeViewError** si verifica quando una chiamata al metodo [External. changeView](external-changeview.md) genera un errore.

``` syntax
window.external.OnChangeViewError = FunctionName
```

## <a name="possible-values"></a>Valori possibili

Si tratta di una proprietà di sola scrittura che specifica il nome della funzione nello script che Windows Media Player chiama quando si verifica l'evento.

## <a name="parameters"></a>Parametri

La funzione che gestisce questo evento presenta i parametri seguenti.

<dl> <dt>

<span id="hr"></span><span id="HR"></span>*HR*
</dt> <dd>

Codice di errore **HRESULT** che indica il motivo dell'errore.

</dd> <dt>

<span id="LibraryLocationType"></span><span id="librarylocationtype"></span><span id="LIBRARYLOCATIONTYPE"></span>*LibraryLocationType*
</dt> <dd>

La stessa stringa passata nel parametro **LibraryLocationType** di **changeView**.

</dd> <dt>

<span id="LibraryLocationID"></span><span id="librarylocationid"></span><span id="LIBRARYLOCATIONID"></span>*LibraryLocationID*
</dt> <dd>

La stessa stringa questofosse passata nel parametro **LibraryLocationID** di **changeView**.

</dd> <dt>

<span id="Filter"></span><span id="filter"></span><span id="FILTER"></span>*Filtro*
</dt> <dd>

La stessa stringa passata nel parametro **Filter** di **changeView**.

</dd> <dt>

<span id="ViewParams"></span><span id="viewparams"></span><span id="VIEWPARAMS"></span>*ViewParams*
</dt> <dd>

La stessa stringa passata nel parametro **ViewParams** di **changeView**.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ExternalObject per i negozi di tipo 1 online**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





