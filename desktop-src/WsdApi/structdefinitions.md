---
description: Genera definizioni di struttura C per tipi noti.
ms.assetid: 38ba2e8a-d5b1-47b2-b410-ae161f5039bf
title: structDefinitions - elemento
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c4c8ad894a42bbafd183031849e458ad5f3bf155a9ccba4e704321e875163c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119611561"
---
# <a name="structdefinitions-element"></a>structDefinitions - elemento

Genera definizioni di struttura C per tipi noti.

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
| [**File**](file.md)<br/> | Restituisce un file dal generatore di codice.<br/> <br/> |



## <a name="remarks"></a>Commenti

Gran parte del codice generato e del codice dell'applicazione fa riferimento alle strutture per i tipi noti. Questo elemento viene usato per generare file di inclusione. Questo elemento deve verificarsi dopo un [**elemento structDeclarations**](structdeclarations.md) in modo che i riferimenti tra strutture siano gestiti correttamente.

## <a name="element-information"></a>Informazioni sull'elemento



| Etichetta | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




