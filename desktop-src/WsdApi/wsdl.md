---
description: Specifica un file WSDL da elaborare per le informazioni sul contratto.
ms.assetid: d8f630cd-0541-431b-86a8-792846a85ea0
title: elemento WSDL
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb54f946f32fb4962b8384dea7c6cf4b3c0ebe3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231655"
---
# <a name="wsdl-element"></a>elemento WSDL

Specifica un file WSDL da elaborare per le informazioni sul contratto.

## <a name="usage"></a>Utilizzo

``` syntax
<wsdl>
  child elements
</wsdl>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio



| Elemento                                           | Descrizione                                                                                                                                       |
|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [**excludeImport**](excludeimport.md)<br/> | Impedisce la generazione di istruzioni Import per destinazioni specificate denominate in un <elemento WSDL: Import> in un file WSDL. <br/> <br/> |
| [**importHint**](importhint.md)<br/>       | Specifica il percorso di download per un <WSDL: Import> direttiva che non specifica in modo esplicito una posizione.<br/> <br/>           |
| [**percorso**](path.md)<br/>                   | File e percorso del file di input WSDL.<br/> <br/>                                                                                      |



### <a name="child-element-sequence"></a>Sequenza di elementi figlio

``` syntax
(
  importHint*, 
  excludeImport*, 
  path
)
```

## <a name="parent-elements"></a>Elementi padre



| Elemento                                     | Descrizione                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [**wsdCodeGen**](wsdcodegen.md)<br/> | Elemento radice di un file di script XML del generatore di codice WSDAPI.<br/> <br/> |



## <a name="remarks"></a>Commenti

Qualsiasi elemento [**importHint**](importhint.md) o [**excludeImport**](excludeimport.md) visualizzato dopo l'elemento [**path**](path.md) in un file di configurazione XML verrà ignorato.

## <a name="element-information"></a>Informazioni sull'elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | No            |



 

 




