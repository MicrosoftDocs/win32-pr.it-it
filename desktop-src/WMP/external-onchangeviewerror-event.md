---
title: Evento External.OnChangeViewError
description: Nota In questo argomento vengono descritte le funzionalità progettate per l'uso da parte dei negozi online. | Evento External.OnChangeViewError
ms.assetid: d6370629-5f50-434d-8eb5-5b43d1b2f7fe
keywords:
- Evento External.OnChangeViewError Windows Media Player
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
ms.openlocfilehash: aaa1152c753501b2e2385de8c56af614d62cfb367fcca8468aaa032e9536e8d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648831"
---
# <a name="externalonchangeviewerror-event"></a>Evento External.OnChangeViewError

> [!Note]  
> Questo argomento descrive le funzionalità progettate per l'uso da parte dei negozi online. L'uso di questa funzionalità all'esterno del contesto di un negozio online non è supportato.

 

**L'evento OnChangeViewError** si verifica quando una chiamata al [metodo External.changeView](external-changeview.md) restituisce un errore.

``` syntax
window.external.OnChangeViewError = FunctionName
```

## <a name="possible-values"></a>Valori possibili

Si tratta di una proprietà di sola scrittura che specifica il nome della funzione nello script che Windows Media Player chiamate quando si verifica l'evento.

## <a name="parameters"></a>Parametri

La funzione che gestisce questo evento ha i parametri seguenti.

<dl> <dt>

<span id="hr"></span><span id="HR"></span>*Hr*
</dt> <dd>

Codice **di errore HRESULT** che indica il motivo dell'errore.

</dd> <dt>

<span id="LibraryLocationType"></span><span id="librarylocationtype"></span><span id="LIBRARYLOCATIONTYPE"></span>*LibraryLocationType*
</dt> <dd>

La stessa stringa passata nel **parametro LibraryLocationType** di **changeView**.

</dd> <dt>

<span id="LibraryLocationID"></span><span id="librarylocationid"></span><span id="LIBRARYLOCATIONID"></span>*LibraryLocationID*
</dt> <dd>

La stessa stringa passata nel **parametro LibraryLocationID** di **changeView**.

</dd> <dt>

<span id="Filter"></span><span id="filter"></span><span id="FILTER"></span>*Filtro*
</dt> <dd>

La stessa stringa passata nel **parametro Filter** di **changeView**.

</dd> <dt>

<span id="ViewParams"></span><span id="viewparams"></span><span id="VIEWPARAMS"></span>*ViewParams*
</dt> <dd>

La stessa stringa passata nel **parametro ViewParams** di **changeView**.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ExternalObject per i negozi online di tipo 1**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





