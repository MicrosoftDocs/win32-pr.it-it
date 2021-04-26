---
description: Genera definizioni della struttura C per i tipi noti.
ms.assetid: 38ba2e8a-d5b1-47b2-b410-ae161f5039bf
title: Elemento structDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26f680db18b06253362f932cc7d34d5b85f7c1b5
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996458"
---
# <a name="structdefinitions-element"></a>Elemento structDefinitions

Genera definizioni della struttura C per i tipi noti.

## <a name="usage"></a>Utilizzo

``` syntax
<structDefinitions/>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio

Non ci sono elementi figlio.

## <a name="parent-elements"></a>Elementi padre



| Elemento                         | Descrizione                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**ﬁle**](file.md)<br/> | Restituisce un file dal generatore di codice.<br/> <br/> |



## <a name="remarks"></a>Commenti

Gran parte del codice generato e del codice dell'applicazione fa riferimento alle strutture per i tipi noti. Questo elemento viene usato per generare file di inclusione. Questo elemento deve verificarsi dopo un [**elemento structDeclarations**](structdeclarations.md) in modo che i riferimenti tra strutture siano gestiti correttamente.

## <a name="element-information"></a>Informazioni sull'elemento



| Label | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




