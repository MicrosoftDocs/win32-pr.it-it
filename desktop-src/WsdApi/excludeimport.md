---
description: 'Impedisce la generazione di istruzioni Import per destinazioni specificate denominate in un <elemento WSDL: Import> in un file WSDL.'
ms.assetid: 9a50ee38-fadf-4112-8430-cb5a07ae04ce
title: elemento excludeImport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c08d8880029d9e03917e48b61561e3ab3eb2815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880642"
---
# <a name="excludeimport-element"></a>elemento excludeImport

Impedisce la generazione di istruzioni Import per destinazioni specificate denominate in un <elemento WSDL: Import> in un file WSDL. Questa operazione può essere utilizzata per impedire a WsdCodeGen di importare destinazioni note, ad esempio le specifiche WS-Addressing e WS-Eventing, anche se in WSDL viene fatto riferimento a tali destinazioni.

Il valore di questo elemento deve essere impostato sullo spazio dei nomi denominato nell'elemento <WSDL: Import> da escludere.

## <a name="usage"></a>Utilizzo

``` syntax
<excludeImport/>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio

Non ci sono elementi figlio.

## <a name="parent-elements"></a>Elementi padre



| Elemento                         | Descrizione                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------|
| [**WSDL**](wsdl.md)<br/> | Specifica un file WSDL da elaborare per le informazioni sul contratto.<br/> <br/> |



## <a name="element-information"></a>Informazioni sull'elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




