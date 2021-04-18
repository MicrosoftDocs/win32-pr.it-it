---
description: Genera definizioni della struttura C per i tipi di messaggio.
ms.assetid: 68459b22-0f35-444a-969e-29695e735774
title: elemento messageStructureDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8840e4493cb97d33cb0dac8ce1ace97cc1789e4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310291"
---
# <a name="messagestructuredefinitions-element"></a>elemento messageStructureDefinitions

Genera definizioni della struttura C per i tipi di messaggio.

## <a name="usage"></a>Utilizzo

``` syntax
<messageStructureDefinitions>
  child elements
</messageStructureDefinitions>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio



| Elemento                                   | Descrizione                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------|
| [**operazione**](operation.md)<br/> | Specifica un'operazione per la quale deve essere generato il codice.<br/> <br/>  |
| [**portType**](porttype.md)<br/>   | Specifica il tipo di porta per il quale deve essere generato il codice.<br/> <br/> |



### <a name="child-element-sequence"></a>Sequenza di elementi figlio

``` syntax
(
  portType?, 
  operation*
)
```

## <a name="parent-elements"></a>Elementi padre



| Elemento                         | Descrizione                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**file**](file.md)<br/> | Restituisce un file dal generatore di codice.<br/> <br/> |



## <a name="remarks"></a>Commenti

Il codice stub e il proxy generato fanno riferimento a strutture di messaggio. Questo elemento viene utilizzato per generare file di inclusione.

## <a name="element-information"></a>Informazioni sull'elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




