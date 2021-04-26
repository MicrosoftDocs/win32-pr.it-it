---
description: Specifica se le operazioni asincrone vengono incluse nelle funzioni proxy generate.
ms.assetid: 7b57d5c6-589b-4e03-bfcf-1faa671ebd77
title: elemento async
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6cbc68d0a5dea30f4b4d179a54539ac3f9516a4
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994958"
---
# <a name="async-element"></a>elemento async

Specifica se le operazioni asincrone vengono incluse nelle funzioni proxy generate.

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
| [**functionDeclarations**](functiondeclarations.md)<br/>                 | Genera dichiarazioni di implementazione per le funzioni proxy per le operazioni sul tipo di porta.<br/> <br/> |
| [**idlFunctionDeclarations**](idlfunctiondeclarations.md)<br/>           | Genera dichiarazioni IDL per le funzioni proxy per le operazioni sul tipo di porta.<br/> <br/>            |
| [**proxyFunctionImplementations**](proxyfunctionimplementations.md)<br/> | Genera implementazioni per le funzioni proxy per le operazioni sul tipo di porta.<br/> <br/>             |



## <a name="remarks"></a>Commenti

I valori possibili sono 1 (operazioni asincrone incluse) e 0 (impostazione predefinita, operazioni asincrone escluse).

Un proxy può avere versioni asincrone e sincrone delle stesse operazioni.

## <a name="element-information"></a>Informazioni sull'elemento



| Label | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




