---
description: Definisce gli elementi ServiceID e Types per l'host del servizio.
ms.assetid: 95066c04-5bdc-4c97-98b8-1da9928d9395
title: elemento host
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9f051f6665715ecaa519a060e18a3cbf4912210
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993798"
---
# <a name="host-element"></a>elemento host

Definisce gli elementi [**ServiceID**](serviceid.md) e [**Types per**](types.md) l'host del servizio.

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
| [**SERVICEID**](serviceid.md)<br/> | Definisce l'identificatore del servizio per l'host del servizio.<br/> <br/> |
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



| Label | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | No            |



 

 




