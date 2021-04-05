---
title: Elemento Application
description: Rappresenta l'elemento di livello principale nella specifica di markup del Framework della barra multifunzione di Windows.
ms.assetid: 05396d8b-fbd1-40bb-8d0f-8ac11506e7db
keywords:
- Barra multifunzione Windows elemento applicazione
topic_type:
- apiref
api_name:
- Application
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9b116879a918ca0437c7f2bdd201ef4ffd6d3c61
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "103734714"
---
# <a name="application-element"></a>Elemento Application

Rappresenta l'elemento di livello principale nella specifica di markup del Framework della barra multifunzione di Windows.

## <a name="usage"></a>Utilizzo

``` syntax
<Application
  xmlns = "xs:string">
  child elements
</Application>
```

## <a name="attributes"></a>Attributi



| Attributo            | Type                 | Obbligatoria       | Descrizione                                                                                                                                                                                                       |
|----------------------|----------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **xmlns**<br/> | xs:string<br/> | Sì<br/> | <dt>`http://schemas.microsoft.com/windows/2009/Ribbon`<br/> </dt> <dd> URI per l'associazione dello spazio dei nomi di markup della barra multifunzione. <br/> </dd> </dl> |



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                               | Descrizione                                    |
|---------------------------------------------------------------------------------------|------------------------------------------------|
| [**Application. Commands**](windowsribbon-element-application-commands.md)<br/> | Può verificarsi al massimo una volta<br/> <br/>  |
| [**Application. views**](windowsribbon-element-application-views.md)<br/>       | Deve verificarsi esattamente una volta<br/> <br/> |



## <a name="parent-elements"></a>Elementi padre

Non ci sono elementi padre.

## <a name="remarks"></a>Commenti

Obbligatorio.

Deve verificarsi esattamente una volta come contenitore per tutto il markup della barra multifunzione.

Gli elementi figlio dell'elemento dell' **applicazione** devono essere presenti nell'ordine specificato:

1.  [**Application. Commands**](windowsribbon-element-application-commands.md)
2.  [**Application. views**](windowsribbon-element-application-views.md)

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrata una dichiarazione di elemento **dell'applicazione** .


```XML
<Application xmlns="http://schemas.microsoft.com/windows/2009/Ribbon">
...
</Application>
```



## <a name="element-information"></a>Informazioni sull'elemento



|                                     |           |
|-------------------------------------|-----------|
| Sistema minimo supportato<br/> | Windows 7 |
| Può essere vuoto                        | No        |



## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Dichiarazione di comandi e controlli con markup della barra multifunzione](windowsribbon-schema.md)
</dt> </dl>

 

 





