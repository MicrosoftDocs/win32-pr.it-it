---
description: Genera dichiarazioni di costanti C per i tipi di porta.
ms.assetid: 05a06206-3cc4-428d-b9f2-b7945e63922c
title: elemento portTypeDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c4e202f1451d93b519bd59ea51f591c37a92957
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310280"
---
# <a name="porttypedeclarations-element"></a>elemento portTypeDeclarations

Genera dichiarazioni di costanti C per i tipi di porta.

## <a name="usage"></a>Utilizzo

``` syntax
<portTypeDeclarations>
  child elements
</portTypeDeclarations>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio



| Elemento                                   | Descrizione                                                                                                                                                               |
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**codeName**](codename.md)<br/>   | Specifica il nome da utilizzare per il tipo di porta nel codice generato. Per impostazione predefinita, il nome del codice viene generato dal nome completo del tipo di porta.<br/> <br/> |
| [**operazione**](operation.md)<br/> | Specifica un'operazione per la quale deve essere generato il codice.<br/> <br/>                                                                                          |
| [**portType**](porttype.md)<br/>   | Specifica il tipo di porta per il quale deve essere generato il codice.<br/> <br/>                                                                                         |



### <a name="child-element-sequence"></a>Sequenza di elementi figlio

``` syntax
(
  portType?, 
  operation*, 
  codeName?
)
```

## <a name="parent-elements"></a>Elementi padre



| Elemento                         | Descrizione                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**file**](file.md)<br/> | Restituisce un file dal generatore di codice.<br/> <br/> |



## <a name="remarks"></a>Commenti

L'applicazione fa riferimento alle dichiarazioni dei tipi di porta e gran parte del codice generato. Questo elemento viene utilizzato per generare file di inclusione.

## <a name="element-information"></a>Informazioni sull'elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




