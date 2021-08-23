---
description: Definisce i metadati del produttore e del modello per il dispositivo da implementazione. Questo elemento viene usato solo per le implementazioni del dispositivo (host).
ms.assetid: 2ebd3092-39aa-469c-a8c9-23f373ba0e66
title: Elemento thisModelMetadata
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01d074e7e9c8d43e078ebc477366d88608e7c4f3fade6c0be3dbc6fda23f006b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991551"
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
| [**Produttore**](manufacturer.md)<br/>             | Nome del produttore. Nei metadati [**deve**](manufacturer.md) essere presente almeno un produttore o un [**produttoreLS.**](manufacturerls.md)<br/> <br/> |
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



| Etichetta | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | No            |



 

 




