---
description: Specifica se gli eventi correlati vengono inclusi nelle funzioni generate.
ms.assetid: 23ca463c-b305-496b-a1e3-58dbb793f17e
title: elemento events
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fea6d4d3c87ac15ee14864f7e12c419f13d97503eeab27d28c5bdec5dbcc1414
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049689"
---
# <a name="events-element"></a>elemento events

Specifica se gli eventi correlati vengono inclusi nelle funzioni generate.

## <a name="usage"></a>Utilizzo

``` syntax
<events/>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio

Non ci sono elementi figlio.

## <a name="parent-elements"></a>Elementi padre



| Elemento                                                                         | Descrizione                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**functionDeclarations**](functiondeclarations.md)<br/>                 | Genera dichiarazioni di implementazione per le funzioni proxy per le operazioni sul tipo di porta.<br/> <br/> |
| [**idlFunctionDeclarations**](idlfunctiondeclarations.md)<br/>           | Genera dichiarazioni IDL per le funzioni proxy per le operazioni sul tipo di porta.<br/> <br/>            |
| [**proxyFunctionImplementations**](proxyfunctionimplementations.md)<br/> | Genera implementazioni per le funzioni proxy per le operazioni sul tipo di porta.<br/> <br/>             |
| [**stubDeclarations**](stubdeclarations.md)<br/>                         | Genera dichiarazioni per le funzioni stub per le operazioni sul tipo di porta.<br/> <br/>                 |
| [**stubDefinitions**](stubdefinitions.md)<br/>                           | Genera implementazioni per le funzioni stub per le operazioni sul tipo di porta.<br/> <br/>              |



## <a name="remarks"></a>Commenti

I valori possibili sono 1 (eventi inclusi) e 0 (impostazione predefinita, eventi esclusi).

## <a name="element-information"></a>Informazioni sull'elemento



| Etichetta | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




