---
description: Specifica se le operazioni asincrone sono incluse nelle funzioni proxy generate.
ms.assetid: 7b57d5c6-589b-4e03-bfcf-1faa671ebd77
title: Async (elemento)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea04eaa66fbdadfc784650c1a451cebf171f6372
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058131"
---
# <a name="async-element"></a>Async (elemento)

Specifica se le operazioni asincrone sono incluse nelle funzioni proxy generate.

## <a name="usage"></a>Utilizzo

``` syntax
<async/>
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



## <a name="remarks"></a>Commenti

I valori possibili sono 1 (operazioni asincrone incluse) e 0 (le operazioni asincrone predefinite sono escluse).

Un proxy può includere sia versioni asincrone che sincrone delle stesse operazioni.

## <a name="element-information"></a>Informazioni sull'elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




