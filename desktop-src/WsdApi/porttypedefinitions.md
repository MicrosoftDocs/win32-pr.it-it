---
description: Genera costanti C per i tipi di porta.
ms.assetid: 6ad0d163-df51-48b6-aad7-a4b018688872
title: elemento portTypeDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff073eb7b0f9cbc4b0b6df87c8f9fc84d4f62882
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996548"
---
# <a name="porttypedefinitions-element"></a>elemento portTypeDefinitions

Genera costanti C per i tipi di porta.

## <a name="usage"></a>Utilizzo

``` syntax
<portTypeDefinitions>
  child elements
</portTypeDefinitions>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                   | Descrizione                                                                                                                                                                       |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Codename**](codename.md)<br/>                   | Specifica il nome da utilizzare per il tipo di porta nel codice generato. Per impostazione predefinita, il nome in codice viene generato dal nome completo del tipo di porta.<br/> <br/>         |
| [**eventStubFunction**](eventstubfunction.md)<br/> | Specifica se i riferimenti alle funzioni stub devono essere inclusi nelle strutture delle operazioni nelle definizioni dei tipi di porta per le operazioni di notifica.<br/> <br/>        |
| [**Operazione**](operation.md)<br/>                 | Specifica un'operazione per la quale deve essere generato il codice.<br/> <br/>                                                                                                  |
| [**Porttype**](porttype.md)<br/>                   | Specifica il tipo di porta per cui deve essere generato il codice.<br/> <br/>                                                                                                 |
| [**StubFunction**](stubfunction.md)<br/>           | Specifica se i riferimenti alle funzioni stub devono essere inclusi nelle strutture delle operazioni nelle definizioni dei tipi di porta per le operazioni unidirezionale e bidirezionale.<br/> <br/> |



### <a name="child-element-sequence"></a>Sequenza di elementi figlio

``` syntax
(
  portType?, 
  operation*, 
  stubFunction?, 
  eventStubFunction?, 
  codeName?
)
```

## <a name="parent-elements"></a>Elementi padre



| Elemento                         | Descrizione                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**ﬁle**](file.md)<br/> | Restituisce un file dal generatore di codice.<br/> <br/> |



## <a name="remarks"></a>Commenti

Questo elemento viene in genere usato nei file di origine C per fornire le costanti del tipo di porta dichiarate da [**portTypeDeclarations.**](porttypedeclarations.md)

## <a name="element-information"></a>Informazioni sull'elemento



| Label | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




