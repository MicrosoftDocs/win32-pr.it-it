---
description: L'interfaccia IWiaPropertyStorage fornisce metodi per la lettura e la scrittura delle proprietà di un Windows di acquisizione di immagini (WIA). Le proprietà degli elementi includono i comandi del dispositivo, le informazioni sul formato degli elementi e le informazioni sul dispositivo.
ms.assetid: 268d2298-bc9c-479b-b078-a8180cd38bc3
title: Lettura e impostazione delle proprietà WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 607e319723023a00c4159687c3dff13fedab8275a0522fdb2254b36b8e62edb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118439875"
---
# <a name="reading-and-setting-wia-properties"></a>Lettura e impostazione delle proprietà WIA

[**L'interfaccia IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) fornisce metodi per la lettura e la scrittura delle proprietà di un elemento Windows Image Acquisition (WIA). Le proprietà degli elementi includono i comandi del dispositivo, le informazioni sul formato degli elementi e le informazioni sul dispositivo.

Un'applicazione può ottenere un puntatore a un'interfaccia [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) di un elemento enumerando le informazioni sul dispositivo o sull'evento dell'elemento chiamando [**IWiaItem::EnumDeviceCapabilities**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumdevicecapabilities) o [**IWiaItem::EnumRegisterEventInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumregistereventinfo) o tramite query sull'interfaccia [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) dell'elemento. In WIA 2.0 eseguire questa operazione chiamando [**IWiaItem2::EnumDeviceCapabilities**](-wia-iwiaitem2-enumdevicecapabilities.md) o [**IWiaItem2::EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) o tramite query sull'interfaccia [**IWiaItem2**](-wia-iwiaitem2.md) dell'elemento.

[**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) eredita da [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) e i metodi ereditati vengono implementati come descritto nella sezione di riferimento di Structured Archiviazione in Windows Software Development Kit (SDK).

> [!Note]
>
> Le applicazioni WIA devono sempre leggere le intestazioni dei dati delle immagini per ottenere informazioni accurate sull'immagine. Il driver WIA può modificare le proprietà WIA e le intestazioni dei dati di immagine durante il trasferimento dei dati.
>
> Se non è presente alcuna intestazione di dati di immagine fornita con il formato specificato, l'applicazione WIA deve usare le proprietà WIA come origine informazioni sul trasferimento dei dati. L'applicazione WIA deve rileggere le proprietà WIA necessarie al termine dell'analisi o dell'acquisizione per ottenere le impostazioni aggiornate.

 

Le sezioni seguenti descrivono le varie proprietà wi-fi:

-   [Convalida delle proprietà WIA](-wia-wia-property-validation.md)
-   [Proprietà delle informazioni sul dispositivo](-wia-device-information-properties-wia-dip-xxxx.md)
-   [Proprietà dispositivo](-wia-device-properties.md)
-   [Proprietà degli elementi](-wia-item-properties.md)
-   [Proprietà WIA aggiuntive](-wia-additional-wia-properties.md)
-   [Definizione di proprietà personalizzate](-wia-defining-custom-properties.md)
-   [Utilizzo di proprietà personalizzate](-wia-using-custom-properties.md)
-   [Schema del profilo di analisi](-wia-scan-profile-schema.md)

 

 
