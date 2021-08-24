---
title: Elemento Application
description: Rappresenta l'elemento di primo livello nella specifica Windows markup del framework della barra multifunzione.
ms.assetid: 05396d8b-fbd1-40bb-8d0f-8ac11506e7db
keywords:
- Elemento Application Windows ribbon
topic_type:
- apiref
api_name:
- Application
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4055e271ecf3313596b73aa36a5cbea37250416d9b517fb4512b89fbc203293a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810811"
---
# <a name="application-element"></a>Elemento Application

Rappresenta l'elemento di primo livello nella specifica Windows markup del framework della barra multifunzione.

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
| [**Application.Commands**](windowsribbon-element-application-commands.md)<br/> | Può verificarsi al massimo una volta<br/> <br/>  |
| [**Application.Views**](windowsribbon-element-application-views.md)<br/>       | Deve verificarsi esattamente una volta<br/> <br/> |



## <a name="parent-elements"></a>Elementi padre

Non ci sono elementi padre.

## <a name="remarks"></a>Commenti

Obbligatorio.

Deve essere eseguito esattamente una volta come contenitore per tutto il markup della barra multifunzione.

Gli elementi figlio **dell'elemento Application** devono essere presenti nell'ordine specificato:

1.  [**Application.Commands**](windowsribbon-element-application-commands.md)
2.  [**Application.Views**](windowsribbon-element-application-views.md)

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrata una **dichiarazione di** elemento Application.


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

 

 





