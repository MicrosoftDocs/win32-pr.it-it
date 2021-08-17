---
description: Definisce gli elementi ServiceID e Types per l'host del servizio.
ms.assetid: 95066c04-5bdc-4c97-98b8-1da9928d9395
title: elemento host
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fe0637c358fabe27f2a1203306cd53407d85ab8b52f2dcd7a827dd49becffda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117738607"
---
# <a name="host-element"></a>elemento host

Definisce gli elementi [**ServiceID**](serviceid.md) e [**Types**](types.md) per l'host del servizio.

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
| [**Tipi**](types.md)<br/>         | Definisce un elenco di nomi qualificati XSD.<br/> <br/>               |



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
| [**hostMetadata**](hostmetadata.md)<br/> | Metadati di hosting per il dispositivo da implementazione.<br/> <br/> |



## <a name="element-information"></a>Informazioni sull'elemento



| Etichetta | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | No            |



 

 




