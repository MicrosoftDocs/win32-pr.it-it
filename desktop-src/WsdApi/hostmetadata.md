---
description: Definisce i metadati di hosting per il dispositivo da implementazione. Questo elemento viene usato solo per le implementazioni del dispositivo (host).
ms.assetid: ca7bc5ea-8ab2-4233-86d2-5b793021b8ee
title: elemento hostMetadata
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9cf6fa139a2723ed90dfe281fc7b054016386fa
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994798"
---
# <a name="hostmetadata-element"></a>elemento hostMetadata

Definisce i metadati di hosting per il dispositivo da implementazione. Questo elemento viene usato solo per le implementazioni del dispositivo (host).

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
| [**Host**](host.md)<br/>     | Definisce gli elementi ServiceID e [**Types per**](types.md) l'host del servizio. Se non viene specificato in modo esplicito, WSDAPI non fornisce dati predefiniti in risposta alle richieste di metadati.<br/> <br/>                                                                                                                                          |
| [**Ospitato da**](hosted.md)<br/> | Definisce gli elementi [**ServiceID**](serviceid.md) e [**Types**](types.md) per i servizi forniti da questo host del servizio. Ogni servizio fornito da questo host [](hosted.md) del servizio deve avere le proprie informazioni sugli elementi ospitati per garantire che il servizio venga pubblicato correttamente in risposta alle richieste di metadati.<br/> <br/> |



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

I metadati di hosting vengono visualizzati in questo elemento in un formato simile a quello specificato nel profilo del dispositivo. **hostMetadata** è leggermente diverso dal formato descritto nel profilo del dispositivo in quanto l'unica proprietà di riferimento che supporta è l'ID servizio.

[**L'elemento relationshipMetadataDefinition**](relationshipmetadatadefinition.md) viene usato successivamente per generare una costante C contenente queste informazioni.

## <a name="element-information"></a>Informazioni sull'elemento



| Label | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | No            |



 

 




