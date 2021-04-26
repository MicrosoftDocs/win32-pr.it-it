---
description: Specifica se i parametri utilizzati per passare le informazioni sugli errori vengono inclusi nelle funzioni generate.
ms.assetid: aba78d50-f884-416a-b022-bb03416aad11
title: Elemento faultInfo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3788af9aeb31d1ed84522bc6b177143ec0607b2
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995858"
---
# <a name="faultinfo-element"></a>Elemento faultInfo

Specifica se i parametri utilizzati per passare le informazioni sugli errori vengono inclusi nelle funzioni generate.

## <a name="usage"></a>Utilizzo

``` syntax
<faultInfo/>
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
| [**stubDefinitions**](stubdefinitions.md)<br/>                           | Genera implementazioni per le funzioni stub per le operazioni sul tipo di porta.<br/> <br/>              |



## <a name="remarks"></a>Commenti

I valori possibili sono 1 (parametri di errore inclusi) e 0 (parametri di errore esclusi). Per impostazione predefinita, i parametri di errore sono esclusi.

## <a name="element-information"></a>Informazioni sull'elemento



| Label | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




