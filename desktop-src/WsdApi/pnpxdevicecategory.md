---
description: Specifica la categoria PnP-X a cui appartiene il dispositivo. È possibile specificare più di una categoria.
ms.assetid: 1ca46000-4700-4326-8f49-1b9a22d45bfa
title: Elemento PnPXDeviceCategory
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42a34a3f63333a2d33266991c0e028e7d42a7244c962617974c9cc15e290d03c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897361"
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
| [**thisModelMetadata**](thismodelmetadata.md)<br/> | Definisce i metadati del produttore e del modello per il dispositivo da implementazione.<br/> <br/> |



## <a name="remarks"></a>Commenti

I dispositivi possono anche specificare una sottocategoria del dispositivo per una categoria di dispositivi più descrittiva. Ad esempio, "Phones.WindowsMobile Cameras.DigitalStillCamera MediaDevices.MusicPlayer" identifica un dispositivo che è un dispositivo Microsoft Windows Mobile con una fotocamera e un lettore musicale. La categoria di dispositivi principale per questo dispositivo è "Telefoni".

Per specificare più categorie di dispositivi, separare le categorie con uno spazio. Ad esempio, "Printers Archiviazione" identifica un dispositivo con una categoria primaria "Stampanti" e una categoria secondaria "Archiviazione".

Se è presente un elemento **PnPXDeviceCategory,** almeno un elemento [**ospitato**](hosted.md) deve contenere entrambi gli elementi [**PnPXHardwareId**](pnpxhardwareid.md) e [**PnPXCompatibleId.**](pnpxcompatibleid.md) Analogamente, se gli elementi **PnPXHardwareId** e **PnPXCompatibleId** sono presenti in un elemento **ospitato,** all'interno dell'elemento [**thisModelMetadata**](thismodelmetadata.md) deve essere presente almeno un elemento **PnPXDeviceCategory.**

## <a name="element-information"></a>Informazioni sull'elemento



| Etichetta | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




