---
description: Specifica se gli eventi correlati sono inclusi nelle funzioni generate.
ms.assetid: 23ca463c-b305-496b-a1e3-58dbb793f17e
title: Elemento Events
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2571cc8e9820ca38beb649b3c227fb1c01f61c50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226927"
---
# <a name="events-element"></a>Elemento Events

Specifica se gli eventi correlati sono inclusi nelle funzioni generate.

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
| [**functionDeclarations**](functiondeclarations.md)<br/>                 | Genera dichiarazioni di implementazione per le funzioni proxy per le operazioni del tipo di porta.<br/> <br/> |
| [**idlFunctionDeclarations**](idlfunctiondeclarations.md)<br/>           | Genera dichiarazioni IDL per le funzioni proxy per le operazioni del tipo di porta.<br/> <br/>            |
| [**proxyFunctionImplementations**](proxyfunctionimplementations.md)<br/> | Genera implementazioni per le funzioni proxy per le operazioni del tipo di porta.<br/> <br/>             |
| [**stubDeclarations**](stubdeclarations.md)<br/>                         | Genera dichiarazioni per le funzioni stub per le operazioni del tipo di porta.<br/> <br/>                 |
| [**stubDefinitions**](stubdefinitions.md)<br/>                           | Genera implementazioni per le funzioni stub per le operazioni del tipo di porta.<br/> <br/>              |



## <a name="remarks"></a>Commenti

I valori possibili sono 1 (eventi inclusi) e 0 (impostazione predefinita, eventi esclusi).

## <a name="element-information"></a>Informazioni sull'elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




