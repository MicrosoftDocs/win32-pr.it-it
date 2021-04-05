---
description: Definisce il produttore e i metadati del modello per il dispositivo da implementare. Questo elemento viene usato solo per le implementazioni dei dispositivi (host).
ms.assetid: 2ebd3092-39aa-469c-a8c9-23f373ba0e66
title: elemento thisModelMetadata
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c1a35d6449d4e8bba0ecf79e7dc87b00dee894b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884245"
---
# <a name="thismodelmetadata-element"></a>elemento thisModelMetadata

Definisce il produttore e i metadati del modello per il dispositivo da implementare. Questo elemento viene usato solo per le implementazioni dei dispositivi (host).

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
| [**Produttore**](manufacturer.md)<br/>             | Nome del produttore. Almeno un [**produttore**](manufacturer.md) o [**manufacturerLS**](manufacturerls.md) deve essere presente nei metadati.<br/> <br/> |
| [**manufacturerLS**](manufacturerls.md)<br/>         | Versione localizzata del nome del produttore.<br/> <br/>                                                                                                                 |
| [**manufacturerURL**](manufacturerurl.md)<br/>       | Indirizzo URL produttore.<br/> <br/>                                                                                                                                   |
| [**modelName**](modelname.md)<br/>                   | Nome del dispositivo. È necessario che nei metadati sia presente almeno un oggetto [**ModelName**](modelname.md) o [**modelNameLS**](modelnamels.md) .<br/> <br/>                   |
| [**modelNameLS**](modelnamels.md)<br/>               | Versione localizzata del nome del dispositivo.<br/> <br/>                                                                                                                       |
| [**modelNumber**](modelnumber.md)<br/>               | Numero del modello del dispositivo.<br/> <br/>                                                                                                                                 |
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
| [**wsdCodeGen**](wsdcodegen.md)<br/> | Elemento radice di un file di script XML del generatore di codice WSDAPI.<br/> <br/> |



## <a name="remarks"></a>Commenti

I metadati del produttore corrispondono alla sezione dei metadati del produttore descritta nel profilo del dispositivo. per informazioni dettagliate, vedere il profilo del dispositivo. È necessario fornire il nome del produttore o almeno una versione localizzata del nome del produttore. È necessario fornire il nome del modello o almeno una versione localizzata del nome del modello.

L'elemento [**thisModelMetadataDefinition**](thismodelmetadatadefinition.md) viene successivamente usato per generare una costante C che contiene queste informazioni.

Se è presente un elemento [**PnPXDeviceCategory**](pnpxdevicecategory.md) , almeno un elemento [**Hosted**](hosted.md) deve contenere entrambi gli elementi [**PnPXHardwareId**](pnpxhardwareid.md) e [**PnPXCompatibleId**](pnpxcompatibleid.md) . Analogamente, se gli elementi **PnPXHardwareId** e **PnPXCompatibleId** sono presenti in un elemento **Hosted** , è necessario che sia presente un elemento **PnPXDeviceCategory** all'interno dell'elemento **thisModelMetadata** .

## <a name="element-information"></a>Informazioni sull'elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | No            |



 

 




