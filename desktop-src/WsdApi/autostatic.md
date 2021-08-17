---
description: Indica se WsdCodeGen deve tentare di contrassegnare automaticamente determinati campi generati come statici.
ms.assetid: 0c858567-e17a-46a0-b3ff-a0dc8089b0cd
title: Elemento autoStatic
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f6b9a447e964c90354c909fc0399276d8ed69e7d1dfb3a493d5590a6470d0cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117738674"
---
# <a name="autostatic-element"></a>Elemento autoStatic

Indica se WsdCodeGen deve tentare di contrassegnare automaticamente determinati campi generati come statici. Questo comportamento è abilitato per impostazione predefinita.

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

**L'elemento autoStatic** non è obbligatorio e può essere omesso dal file di configurazione XML. L'elemento può essere usato per disabilitare il flag dei campi generati come statici o per forzare in modo esplicito il flag di determinati campi generati come statici.

I valori possibili sono 1 (abilitato, predefinito) e 0 (disabilitato). **L'abilitazione di autoStatic** può causare problemi di compilazione a seconda del modo in cui il generatore di codice viene indirizzato ai dati di output.

## <a name="element-information"></a>Informazioni sull'elemento



| Etichetta | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




