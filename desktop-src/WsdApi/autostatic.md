---
description: Indica se WsdCodeGen deve provare a contrassegnare automaticamente determinati campi generati come statici.
ms.assetid: 0c858567-e17a-46a0-b3ff-a0dc8089b0cd
title: elemento autostatic
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32591c43c850af05014ff92fc4023e228b371fc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310313"
---
# <a name="autostatic-element"></a>elemento autostatic

Indica se WsdCodeGen deve provare a contrassegnare automaticamente determinati campi generati come statici. Questo comportamento è abilitato per impostazione predefinita.

## <a name="usage"></a>Utilizzo

``` syntax
<autoStatic/>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio

Non ci sono elementi figlio.

## <a name="parent-elements"></a>Elementi padre



| Elemento                                     | Descrizione                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [**wsdCodeGen**](wsdcodegen.md)<br/> | Elemento radice di un file di script XML del generatore di codice WSDAPI.<br/> <br/> |



## <a name="remarks"></a>Commenti

L'elemento **autostatic** non è obbligatorio e può essere omesso dal file di configurazione XML. L'elemento può essere utilizzato per disabilitare il contrassegno dei campi generati come statici o per forzare in modo esplicito l'contrassegno di determinati campi generati come statici.

I valori possibili sono 1 (abilitato, predefinito) e 0 (disabilitato). L'abilitazione di **autostatic** può causare problemi di compilazione a seconda della modalità con cui il generatore di codice viene indirizzato ai dati di output.

## <a name="element-information"></a>Informazioni sull'elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




