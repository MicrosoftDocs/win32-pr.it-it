---
description: Definisce gli elementi ServiceID, Types, PnPXHardwareId e PnPXCompatibleId per i servizi definiti dall'host del servizio.
ms.assetid: f901a88f-7e01-4e7f-a0f2-59f2a01b03cd
title: elemento ospitato
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afc3ea8dae3e705800cb4a1d2733bc86bcd491a25f2888ca258a47d6e765b796
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117738421"
---
# <a name="hosted-element"></a>elemento ospitato

Definisce gli elementi [**ServiceID**](serviceid.md), [**Types**](types.md),[**PnPXHardwareId**](pnpxhardwareid.md)e [**PnPXCompatibleId**](pnpxcompatibleid.md) per i servizi definiti dall'host del servizio.

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
| [**Tipi**](types.md)<br/>                       | Definisce un elenco di nomi qualificati XSD.<br/> <br/>                    |



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
| [**hostMetadata**](hostmetadata.md)<br/> | Metadati di hosting per il dispositivo da implementazione.<br/> <br/> |



## <a name="remarks"></a>Commenti

Ogni servizio fornito da un host  del servizio deve avere informazioni sull'elemento ospitato per garantire che il servizio venga pubblicato correttamente in risposta alle richieste di metadati.

Gli [**elementi PnPXHardwareId**](pnpxhardwareid.md) e [**PnPXCompatibleId**](pnpxcompatibleid.md) sono facoltativi, ma quando vengono usati devono essere usati insieme. Se è presente uno, deve essere presente anche l'altro.

Se è presente un elemento [**PnPXDeviceCategory,**](pnpxdevicecategory.md) almeno un elemento **ospitato** deve contenere entrambi gli elementi [**PnPXHardwareId**](pnpxhardwareid.md) e [**PnPXCompatibleId.**](pnpxcompatibleid.md) Analogamente, se gli elementi **PnPXHardwareId** e **PnPXCompatibleId** sono presenti in un elemento **ospitato,** all'interno dell'elemento [**thisModelMetadata**](thismodelmetadata.md) deve essere presente almeno un elemento **PnPXDeviceCategory.**

## <a name="element-information"></a>Informazioni sull'elemento



| Etichetta | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | No            |



 

 




