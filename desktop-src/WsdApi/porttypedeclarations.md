---
description: Genera dichiarazioni di costanti C per i tipi di porta.
ms.assetid: 05a06206-3cc4-428d-b9f2-b7945e63922c
title: elemento portTypeDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e19780d4a48c95cd47872b0428b368e6b7e99887
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996558"
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
| [**Codename**](codename.md)<br/>   | Specifica il nome da utilizzare per il tipo di porta nel codice generato. Per impostazione predefinita, il nome in codice viene generato dal nome completo del tipo di porta.<br/> <br/> |
| [**Operazione**](operation.md)<br/> | Specifica un'operazione per la quale deve essere generato il codice.<br/> <br/>                                                                                          |
| [**Porttype**](porttype.md)<br/>   | Specifica il tipo di porta per cui deve essere generato il codice.<br/> <br/>                                                                                         |



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
| [**ﬁle**](file.md)<br/> | Restituisce un file dal generatore di codice.<br/> <br/> |



## <a name="remarks"></a>Commenti

L'applicazione fa riferimento alle dichiarazioni del tipo di porta e gran parte del codice generato. Questo elemento viene usato per generare file di inclusione.

## <a name="element-information"></a>Informazioni sull'elemento



| Label | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




