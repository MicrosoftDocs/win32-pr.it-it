---
description: Definisce gli elementi ServiceID, types, PnPXHardwareId e PnPXCompatibleId per i servizi definiti dall'host del servizio.
ms.assetid: f901a88f-7e01-4e7f-a0f2-59f2a01b03cd
title: elemento Hosted
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e4d46549898f0a95de362467c759c3d95eb806a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316979"
---
# <a name="hosted-element"></a>elemento Hosted

Definisce gli elementi [**ServiceID**](serviceid.md), [**types**](types.md),[**PnPXHardwareId**](pnpxhardwareid.md)e [**PnPXCompatibleId**](pnpxcompatibleid.md) per i servizi definiti dall'host del servizio.

## <a name="usage"></a>Utilizzo

``` syntax
<hosted>
  child elements
</hosted>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                 | Descrizione                                                                      |
|---------------------------------------------------------|----------------------------------------------------------------------------------|
| [**PnPXCompatibleId**](pnpxcompatibleid.md)<br/> | Specifica l'identificatore compatibile PnP-X del servizio.<br/> <br/> |
| [**PnPXHardwareId**](pnpxhardwareid.md)<br/>     | Specifica l'identificatore hardware PnP-X del servizio.<br/> <br/>   |
| [**ServiceID**](serviceid.md)<br/>               | Definisce un identificatore del servizio per l'host del servizio.<br/> <br/>        |
| [**Tipi**](types.md)<br/>                       | Definisce un elenco di nomi completi XSD.<br/> <br/>                    |



### <a name="child-element-sequence"></a>Sequenza di elementi figlio

``` syntax
(
  ServiceID, 
  Types, 
  PnPXHardwareId?, 
  PnPXCompatibleId?
)
```

## <a name="parent-elements"></a>Elementi padre



| Elemento                                         | Descrizione                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------|
| [**hostMetadata**](hostmetadata.md)<br/> | Metadati di hosting per il dispositivo da implementare.<br/> <br/> |



## <a name="remarks"></a>Commenti

Ogni servizio fornito da un host del servizio deve disporre di informazioni relative all'elemento **ospitato** per garantire che il servizio venga pubblicato correttamente nelle risposte alle richieste di metadati.

Gli elementi [**PnPXHardwareId**](pnpxhardwareid.md) e [**PnPXCompatibleId**](pnpxcompatibleid.md) sono facoltativi, ma se usati devono essere usati insieme. Se è presente un oggetto, deve essere presente anche l'altro.

Se è presente un elemento [**PnPXDeviceCategory**](pnpxdevicecategory.md) , almeno un elemento **Hosted** deve contenere entrambi gli elementi [**PnPXHardwareId**](pnpxhardwareid.md) e [**PnPXCompatibleId**](pnpxcompatibleid.md) . Analogamente, se gli elementi **PnPXHardwareId** e **PnPXCompatibleId** sono presenti in un elemento **Hosted** , è necessario che sia presente almeno un elemento **PnPXDeviceCategory** all'interno dell'elemento [**thisModelMetadata**](thismodelmetadata.md) .

## <a name="element-information"></a>Informazioni sull'elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | No            |



 

 




