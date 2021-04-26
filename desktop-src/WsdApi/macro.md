---
description: Definisce il testo o CDATA che deve essere riutilizzato dall'elemento include.
ms.assetid: bf5cc1e2-b08e-45b6-8e07-5c69865b695b
title: elemento macro
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f794566b0fd789c463d404289644976c8301a2e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994328"
---
# <a name="macro-element"></a>elemento macro

Definisce il testo o CDATA che deve essere riutilizzato [**dall'elemento include.**](include.md)

## <a name="usage"></a>Utilizzo

``` syntax
<macro
  name = "character_string"/>
```

## <a name="attributes"></a>Attributi



| Attributo           | Type                         | Obbligatoria       | Descrizione                                   |
|---------------------|------------------------------|----------------|-----------------------------------------------|
| **nome**<br/> | stringa di \_ caratteri<br/> | Sì<br/> | Nome della macro.<br/> <br/> |



## <a name="child-elements"></a>Elementi figlio

Non ci sono elementi figlio.

## <a name="parent-elements"></a>Elementi padre



| Elemento                                     | Descrizione                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------------------|
| [**wsdCodeGen**](wsdcodegen.md)<br/> | Elemento radice di un file di script XML del generatore di codice WSDAPI.<br/> <br/> |



## <a name="remarks"></a>Commenti

WsdCodeGen definisce una macro denominata **DoNotModify**. Quando questa macro è inclusa, il codice generato contiene un blocco di commenti ad alta visibilità che indica agli sviluppatori di non modificare il codice generato.

Il codice XML seguente illustra come includere la macro **DoNotModify.** Questo codice XML può essere aggiunto a un file di configurazione XML per WsdCodeGen.

``` syntax
<include macro="DoNotModify">
```

## <a name="element-information"></a>Informazioni sull'elemento



| Label | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




