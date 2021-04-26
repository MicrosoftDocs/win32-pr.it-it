---
description: Definisce i metadati del produttore e del modello per il dispositivo da implementazione. Questo elemento viene usato solo per le implementazioni del dispositivo (host).
ms.assetid: 2ebd3092-39aa-469c-a8c9-23f373ba0e66
title: Elemento thisModelMetadata
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 872bcdfcf3f93bfc8fe307684c31cdebb2000b05
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995338"
---
# <a name="thismodelmetadata-element"></a>Elemento thisModelMetadata

Definisce i metadati del produttore e del modello per il dispositivo da implementazione. Questo elemento viene usato solo per le implementazioni del dispositivo (host).

## <a name="usage"></a>Utilizzo

``` syntax
<thisModelMetadata>
  child elements
</thisModelMetadata>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                     | Descrizione                                                                                                                                                                        |
|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Produttore**](manufacturer.md)<br/>             | Nome del produttore. Almeno uno dei [](manufacturerls.md) [**produttori deve**](manufacturer.md) essere presente nei metadati.<br/> <br/> |
| [**manufacturerLS**](manufacturerls.md)<br/>         | Versione localizzata del nome del produttore.<br/> <br/>                                                                                                                 |
| [**manufacturerURL**](manufacturerurl.md)<br/>       | Indirizzo URL del produttore.<br/> <br/>                                                                                                                                   |
| [**Modelname**](modelname.md)<br/>                   | Nome del dispositivo. Nei metadati deve essere presente almeno uno di [**modelName**](modelname.md) o [**modelNameLS.**](modelnamels.md)<br/> <br/>                   |
| [**modelNameLS**](modelnamels.md)<br/>               | Versione localizzata del nome del dispositivo.<br/> <br/>                                                                                                                       |
| [**modelNumber**](modelnumber.md)<br/>               | Numero di modello del dispositivo.<br/> <br/>                                                                                                                                 |
| [**modelURL**](modelurl.md)<br/>                     | Indirizzo URL per il modello di dispositivo.<br/> <br/>                                                                                                                           |
| [**PnPXDeviceCategory**](pnpxdevicecategory.md)<br/> | Categoria PnP-X a cui appartiene il dispositivo. <br/> <br/>                                                                                                                |
| [**presentationURL**](presentationurl.md)<br/>       | Indirizzo URL dei dati di presentazione del modello di dispositivo.<br/> <br/>                                                                                                        |



### <a name="child-element-sequence"></a>Sequenza di elementi figlio

``` syntax
(
  manufacturer?, 
  manufacturerLS*, 
  manufacturerURL?, 
  modelName?, 
  modelNameLS*, 
  modelNumber, 
  modelURL?, 
  PnPXDeviceCategory?, 
  presentationURL?
)
```

## <a name="parent-elements"></a>Elementi padre



| Elemento                                     | Descrizione                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [**wsdCodeGen**](wsdcodegen.md)<br/> | Elemento radice di un file script XML del generatore di codice WSDAPI.<br/> <br/> |



## <a name="remarks"></a>Commenti

I metadati del produttore corrispondono alla sezione dei metadati del produttore descritta nel profilo del dispositivo . Per informazioni dettagliate, vedere il profilo del dispositivo. È necessario specificare il nome del produttore o almeno una versione localizzata del nome del produttore. È necessario specificare il nome del modello o almeno una versione localizzata del nome del modello.

[**L'elemento thisModelMetadataDefinition**](thismodelmetadatadefinition.md) viene successivamente usato per generare una costante C contenente queste informazioni.

Se è presente un elemento [**PnPXDeviceCategory,**](pnpxdevicecategory.md) almeno un elemento ospitato deve contenere entrambi gli elementi [**PnPXHardwareId**](pnpxhardwareid.md) [**e PnPXCompatibleId.**](pnpxcompatibleid.md) [](hosted.md) Analogamente, se gli elementi **PnPXHardwareId** e **PnPXCompatibleId** sono presenti in un elemento ospitato, un elemento **PnPXDeviceCategory** deve essere presente all'interno dell'elemento **thisModelMetadata.** 

## <a name="element-information"></a>Informazioni sull'elemento



| Label | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | No            |



 

 




