---
description: Definisce i metadati di hosting per il dispositivo da implementare. Questo elemento viene usato solo per le implementazioni dei dispositivi (host).
ms.assetid: ca7bc5ea-8ab2-4233-86d2-5b793021b8ee
title: elemento hostMetadata
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: becd6bc3eab6b1aa1d95414c6348288e0d29dbd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318152"
---
# <a name="hostmetadata-element"></a>elemento hostMetadata

Definisce i metadati di hosting per il dispositivo da implementare. Questo elemento viene usato solo per le implementazioni dei dispositivi (host).

## <a name="usage"></a>Utilizzo

``` syntax
<hostMetadata>
  child elements
</hostMetadata>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio



| Elemento                             | Descrizione                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**host**](host.md)<br/>     | Definisce gli elementi ServiceID e [**types**](types.md) per l'host del servizio. Se non viene specificato in modo esplicito, WSDAPI non fornirà dati predefiniti in risposta alle richieste di metadati.<br/> <br/>                                                                                                                                          |
| [**ospitato**](hosted.md)<br/> | Definisce gli elementi [**ServiceID**](serviceid.md) e [**types**](types.md) per i servizi forniti da questo host del servizio. Ogni servizio fornito da questo host del servizio deve disporre di informazioni relative all'elemento [**ospitato**](hosted.md) per garantire che il servizio venga pubblicato correttamente nelle risposte alle richieste di metadati.<br/> <br/> |



### <a name="child-element-sequence"></a>Sequenza di elementi figlio

``` syntax
(
  host?, 
  hosted+
)
```

## <a name="parent-elements"></a>Elementi padre



| Elemento                                                         | Descrizione                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**relationshipMetadata**](relationshipmetadata.md)<br/> | Descrive l'host e i metadati ospitati per il dispositivo.<br/> <br/> |



## <a name="remarks"></a>Commenti

I metadati di hosting vengono visualizzati in questo elemento in un formato simile a quello specificato nel profilo di dispositivo. **hostMetadata** è leggermente diverso dal formato descritto nel profilo del dispositivo perché l'unica proprietà di riferimento supportata è l'ID del servizio.

L'elemento [**relationshipMetadataDefinition**](relationshipmetadatadefinition.md) viene usato in seguito per generare una costante C che contiene queste informazioni.

## <a name="element-information"></a>Informazioni sull'elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | No            |



 

 




