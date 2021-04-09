---
description: Definisce gli elementi ServiceID e types per l'host del servizio.
ms.assetid: 95066c04-5bdc-4c97-98b8-1da9928d9395
title: elemento host
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec073a89cf1911ab363d757d36cd264c85c8a5c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880637"
---
# <a name="host-element"></a>elemento host

Definisce gli elementi [**ServiceID**](serviceid.md) e [**types**](types.md) per l'host del servizio.

## <a name="usage"></a>Utilizzo

``` syntax
<host>
  child elements
</host>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio



| Elemento                                   | Descrizione                                                                 |
|-------------------------------------------|-----------------------------------------------------------------------------|
| [**ServiceID**](serviceid.md)<br/> | Definisce l'identificatore del servizio per l'host del servizio.<br/> <br/> |
| [**Tipi**](types.md)<br/>         | Definisce un elenco di nomi completi XSD.<br/> <br/>               |



### <a name="child-element-sequence"></a>Sequenza di elementi figlio

``` syntax
(
  ServiceID, 
  Types
)
```

## <a name="parent-elements"></a>Elementi padre



| Elemento                                         | Descrizione                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------|
| [**hostMetadata**](hostmetadata.md)<br/> | Metadati di hosting per il dispositivo da implementare.<br/> <br/> |



## <a name="element-information"></a>Informazioni sull'elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | No            |



 

 




