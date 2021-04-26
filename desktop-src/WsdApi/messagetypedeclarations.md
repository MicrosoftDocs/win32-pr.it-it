---
description: Genera dichiarazioni di costanti C per le tabelle di XML Schema per i tipi di messaggio.
ms.assetid: 17556708-9350-444f-84a3-d982270b31d1
title: elemento messageTypeDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 696cd6d30e6a791f68c152e0d0c5d0b1a7300769
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998728"
---
# <a name="messagetypedeclarations-element"></a>elemento messageTypeDeclarations

Genera dichiarazioni di costanti C per le tabelle di XML Schema per i tipi di messaggio.

## <a name="usage"></a>Utilizzo

``` syntax
<messageTypeDeclarations>
  child elements
</messageTypeDeclarations>
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

Le definizioni dei tipi di porta fanno riferimento alle tabelle dello schema. Questo elemento viene quindi usato in genere prima degli [**elementi portTypeDefinitions.**](porttypedefinitions.md)

## <a name="element-information"></a>Informazioni sull'elemento



| Label | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




