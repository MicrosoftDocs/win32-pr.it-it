---
description: Genera costanti C per i tipi di porta.
ms.assetid: 6ad0d163-df51-48b6-aad7-a4b018688872
title: elemento portTypeDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60f55408df938ed95af14c69b2676473ac1bda71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231667"
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
| [**codeName**](codename.md)<br/>                   | Specifica il nome da utilizzare per il tipo di porta nel codice generato. Per impostazione predefinita, il nome del codice viene generato dal nome completo del tipo di porta.<br/> <br/>         |
| [**eventStubFunction**](eventstubfunction.md)<br/> | Specifica se i riferimenti alle funzioni Stub devono essere inclusi nelle strutture dell'operazione nelle definizioni dei tipi di porta per le operazioni di notifica.<br/> <br/>        |
| [**operazione**](operation.md)<br/>                 | Specifica un'operazione per la quale deve essere generato il codice.<br/> <br/>                                                                                                  |
| [**portType**](porttype.md)<br/>                   | Specifica il tipo di porta per il quale deve essere generato il codice.<br/> <br/>                                                                                                 |
| [**stubFunction**](stubfunction.md)<br/>           | Specifica se i riferimenti alle funzioni Stub devono essere inclusi nelle strutture dell'operazione nelle definizioni dei tipi di porta per le operazioni unidirezionali e bidirezionali.<br/> <br/> |



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
| [**file**](file.md)<br/> | Restituisce un file dal generatore di codice.<br/> <br/> |



## <a name="remarks"></a>Commenti

Questo elemento viene in genere usato nei file di origine C per fornire le costanti del tipo di porta dichiarate da [**portTypeDeclarations**](porttypedeclarations.md).

## <a name="element-information"></a>Informazioni sull'elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




