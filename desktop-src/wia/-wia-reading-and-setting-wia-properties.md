---
description: L'interfaccia IWiaPropertyStorage fornisce metodi per la lettura e la scrittura delle proprietà di un elemento di acquisizione immagini Windows (WIA). Le proprietà dell'elemento includono comandi del dispositivo, informazioni sul formato dell'elemento e informazioni sul dispositivo.
ms.assetid: 268d2298-bc9c-479b-b078-a8180cd38bc3
title: Lettura e impostazione delle proprietà WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51df3e8fdb4b29abb6f64743ab8f7f2dd3776358
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129402"
---
# <a name="reading-and-setting-wia-properties"></a>Lettura e impostazione delle proprietà WIA

L'interfaccia [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) fornisce metodi per la lettura e la scrittura delle proprietà di un elemento di acquisizione immagini Windows (WIA). Le proprietà dell'elemento includono comandi del dispositivo, informazioni sul formato dell'elemento e informazioni sul dispositivo.

Un'applicazione può ottenere un puntatore a un'interfaccia [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) di un elemento enumerando le informazioni sul dispositivo dell'elemento o le informazioni sull'evento chiamando [**IWiaItem:: EnumDeviceCapabilities**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumdevicecapabilities) o [**IWiaItem:: EnumRegisterEventInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumregistereventinfo) o eseguendo una query sull'interfaccia [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) dell'elemento. (In WIA 2,0, effettuare questa operazione chiamando [**IWiaItem2:: EnumDeviceCapabilities**](-wia-iwiaitem2-enumdevicecapabilities.md) o [**IWiaItem2:: EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) o eseguendo una query sull'interfaccia [**IWiaItem2**](-wia-iwiaitem2.md) dell'elemento).

[**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) eredita da [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) e i metodi ereditati vengono implementati come descritto nella sezione di riferimento di archiviazione strutturata in Windows Software Development Kit (SDK).

> [!Note]
>
> Le applicazioni WIA devono leggere sempre le intestazioni dei dati dell'immagine per ottenere informazioni accurate sulle immagini. Il driver WIA può modificare le proprietà WIA e le intestazioni dei dati di immagine durante il trasferimento dei dati.
>
> Se non è presente alcuna intestazione dati immagine fornita con il formato specificato, l'applicazione WIA deve usare le proprietà WIA come origine informazioni sul trasferimento dei dati. L'applicazione WIA deve rileggere le proprietà WIA necessarie dopo il completamento dell'analisi o dell'acquisizione per ottenere le impostazioni aggiornate.

 

Le sezioni seguenti descrivono le varie proprietà WIA:

-   [Convalida della proprietà WIA](-wia-wia-property-validation.md)
-   [Proprietà informazioni sul dispositivo](-wia-device-information-properties-wia-dip-xxxx.md)
-   [Proprietà dispositivo](-wia-device-properties.md)
-   [Proprietà degli elementi](-wia-item-properties.md)
-   [Proprietà WIA aggiuntive](-wia-additional-wia-properties.md)
-   [Definizione di proprietà personalizzate](-wia-defining-custom-properties.md)
-   [Utilizzo di proprietà personalizzate](-wia-using-custom-properties.md)
-   [Schema del profilo di analisi](-wia-scan-profile-schema.md)

 

 
