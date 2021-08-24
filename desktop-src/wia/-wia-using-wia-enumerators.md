---
description: WIA offre diverse interfacce per l'enumerazione di varie funzionalità, proprietà e informazioni.
ms.assetid: d46d4c18-79cc-4f3c-9745-522ab2635068
title: Uso degli enumeratori WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47b6e822d38c73171767d43afd416d09648bd6b82095b9408e2f17827751b0cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813471"
---
# <a name="using-wia-enumerators"></a>Uso degli enumeratori WIA

WIA offre diverse interfacce per l'enumerazione di varie funzionalità, proprietà e informazioni. Le Windows di enumerazione WIA (Image Acquisition) sono tutte implementazioni specifiche dell'interfaccia Component Object Model (COM) standard. Per informazioni dettagliate, vedere [IEnumXXXX](/previous-versions//ms680089(v=vs.85)).

Nella tabella seguente vengono fornite informazioni sulle interfacce di enumerazione WIA. 

| Interfaccia                                                   | Come ottenere un puntatore                                                                                                                                                                                    | Utilizzo                                                                                                                             |
|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**IEnumWIA \_ DEV \_ CAPS**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)       | Chiamare un [**metodo IWiaItem::EnumDeviceCapabilities**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumdevicecapabilities) o [**IWiaItem2::EnumDeviceCapabilities**](-wia-iwiaitem2-enumdevicecapabilities.md) di un elemento radice WIA. | Enumera le funzionalità di un dispositivo hardware WIA, ad esempio i comandi e gli eventi del dispositivo.                                            |
| [**IEnumWIA \_ DEV \_ INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info)       | Chiamare il [**metodo IWiaDevMgr::EnumDeviceInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) o [**IWiaDevMgr2::EnumDeviceInfo.**](-wia-iwiadevmgr2-enumdeviceinfo.md)                                            | Enumera i dispositivi WIA disponibili e fornisce puntatori alle interfacce [**IWiaPropertyStorage.**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) |
| [**INFORMAZIONI SUL FORMATO IEnumWIA \_ \_**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info) | Chiamare un [**metodo IWiaDataTransfer::idtEnumWIA \_ FORMAT \_ INFO**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtenumwia_format_info) di un elemento.                                                                              | Enumera tutte le informazioni sul formato dell'immagine fornite da un elemento WIA.                                                                    |
| [**IEnumWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwiaitem)                   | Chiamare un [**metodo IWiaItem::EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) o [**IWiaItem2::EnumChildItems**](-wia-iwiaitem2-enumchilditems.md) dell'elemento WIA.                                          | Enumera gli elementi figlio di un elemento WIA che rappresenta un dispositivo o una cartella.                                                |



 

 

 
