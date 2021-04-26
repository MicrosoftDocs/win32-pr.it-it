---
description: Genera costanti C per le tabelle xml schema per i tipi di messaggio.
ms.assetid: 0b322acb-3326-42a2-a852-07251585b314
title: Elemento messageTypeDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54f1b6563254a93122960b4a990fe0bd18ab1453
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998708"
---
# <a name="messagetypedefinitions-element"></a>Elemento messageTypeDefinitions

Genera costanti C per le tabelle xml schema per i tipi di messaggio.

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
| [**Operazione**](operation.md)<br/> | Specifica un'operazione per cui deve essere generato il codice.<br/> <br/>  |
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

Questo elemento viene in genere usato nei file di origine C per fornire le tabelle dello schema dichiarate da [**messageTypeDeclarations**](messagetypedeclarations.md).

## <a name="element-information"></a>Informazioni sull'elemento



| Label | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




