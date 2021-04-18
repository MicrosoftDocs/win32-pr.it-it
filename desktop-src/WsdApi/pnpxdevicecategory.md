---
description: Specifica la categoria PnP-X a cui appartiene il dispositivo. È possibile specificare più di una categoria.
ms.assetid: 1ca46000-4700-4326-8f49-1b9a22d45bfa
title: Elemento PnPXDeviceCategory
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 731dd78fbe366fc9c7923686d3d9ac90b772c23d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312679"
---
# <a name="pnpxdevicecategory-element"></a>Elemento PnPXDeviceCategory

Specifica la categoria PnP-X a cui appartiene il dispositivo. È possibile specificare più di una categoria.

## <a name="usage"></a>Utilizzo

``` syntax
<PnPXDeviceCategory/>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio

Non ci sono elementi figlio.

## <a name="parent-elements"></a>Elementi padre



| Elemento                                                   | Descrizione                                                                                          |
|-----------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**thisModelMetadata**](thismodelmetadata.md)<br/> | Definisce il produttore e i metadati del modello per il dispositivo da implementare.<br/> <br/> |



## <a name="remarks"></a>Commenti

I dispositivi possono inoltre specificare una sottocategoria del dispositivo per una categoria di dispositivi più descrittiva. Ad esempio, "phones. WindowsMobile cameras. DigitalStillCamera MediaDevices. MusicPlayer" identifica un dispositivo che è un dispositivo Microsoft Windows Mobile con una fotocamera e Music Player. La categoria del dispositivo primario per questo dispositivo è "phones".

Per specificare più di una categoria di dispositivi, separare le categorie con uno spazio. Ad esempio, "stampanti archiviazione" identifica un dispositivo con una categoria primaria di "stampanti" e una categoria secondaria di "archiviazione".

Se è presente un elemento **PnPXDeviceCategory** , almeno un elemento [**Hosted**](hosted.md) deve contenere entrambi gli elementi [**PnPXHardwareId**](pnpxhardwareid.md) e [**PnPXCompatibleId**](pnpxcompatibleid.md) . Analogamente, se gli elementi **PnPXHardwareId** e **PnPXCompatibleId** sono presenti in un elemento **Hosted** , è necessario che sia presente almeno un elemento **PnPXDeviceCategory** all'interno dell'elemento [**thisModelMetadata**](thismodelmetadata.md) .

## <a name="element-information"></a>Informazioni sull'elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




