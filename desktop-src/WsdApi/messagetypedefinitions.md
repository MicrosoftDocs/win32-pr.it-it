---
description: Genera costanti C per le tabelle di XML Schema per i tipi di messaggio.
ms.assetid: 0b322acb-3326-42a2-a852-07251585b314
title: elemento messageTypeDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a94fabdd2ceb2d32052a692f6daa1abba0a52f16d5d1b7dd0a4cef07d33de09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757081"
---
# <a name="messagetypedefinitions-element"></a>elemento messageTypeDefinitions

Genera costanti C per le tabelle di XML Schema per i tipi di messaggio.

## <a name="usage"></a>Utilizzo

``` syntax
<messageTypeDefinitions>
  child elements
</messageTypeDefinitions>
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
| [**File**](file.md)<br/> | Restituisce un file dal generatore di codice.<br/> <br/> |



## <a name="remarks"></a>Commenti

Questo elemento viene in genere usato nei file di origine C per fornire le tabelle dello schema dichiarate da [**messageTypeDeclarations.**](messagetypedeclarations.md)

## <a name="element-information"></a>Informazioni sull'elemento



| Etichetta | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




