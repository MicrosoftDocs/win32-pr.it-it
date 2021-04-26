---
description: Genera definizioni di struttura C per i tipi di messaggio.
ms.assetid: 68459b22-0f35-444a-969e-29695e735774
title: elemento messageStructureDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a116658fc7ce7f985b7b717c7a7b4ce38be4637
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993668"
---
# <a name="messagestructuredefinitions-element"></a>elemento messageStructureDefinitions

Genera definizioni di struttura C per i tipi di messaggio.

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
| [**Operazione**](operation.md)<br/> | Specifica un'operazione per la quale deve essere generato il codice.<br/> <br/>  |
| [**Porttype**](porttype.md)<br/>   | Specifica il tipo di porta per cui deve essere generato il codice.<br/> <br/> |



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
| [**ﬁle**](file.md)<br/> | Restituisce un file dal generatore di codice.<br/> <br/> |



## <a name="remarks"></a>Commenti

Il proxy generato e il codice stub fanno riferimento alle strutture dei messaggi. Questo elemento viene usato per generare file di inclusione.

## <a name="element-information"></a>Informazioni sull'elemento



| Label | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




