---
description: WIA fornisce varie interfacce per l'enumerazione di varie funzionalità, proprietà e informazioni.
ms.assetid: d46d4c18-79cc-4f3c-9745-522ab2635068
title: Uso di enumeratori WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ee42f99718cb36071b828e87e3a71de6d70ab5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226139"
---
# <a name="using-wia-enumerators"></a>Uso di enumeratori WIA

WIA fornisce varie interfacce per l'enumerazione di varie funzionalità, proprietà e informazioni. Le interfacce di enumerazione Windows Image Acquisition (WIA) sono tutte implementazioni specifiche dell'interfaccia di enumerazione standard Component Object Model (COM). Per informazioni dettagliate, vedere [IEnumXXXX](/previous-versions//ms680089(v=vs.85)).

Nella tabella seguente vengono fornite informazioni sulle interfacce di enumerazione WIA. 

| Interfaccia                                                   | Come ottenere un puntatore                                                                                                                                                                                    | Utilizzo                                                                                                                             |
|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**IEnumWIA di \_ sviluppo \_**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)       | Chiamare un metodo [**IWiaItem:: EnumDeviceCapabilities**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumdevicecapabilities) o [**IWiaItem2:: EnumDeviceCapabilities**](-wia-iwiaitem2-enumdevicecapabilities.md) di un elemento radice WIA. | Enumera le funzionalità di un dispositivo hardware WIA, ad esempio i comandi e gli eventi del dispositivo.                                            |
| [**Informazioni su IEnumWIA \_ dev \_**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info)       | Chiamare il metodo [**IWiaDevMgr:: EnumDeviceInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) o [**IWiaDevMgr2:: EnumDeviceInfo**](-wia-iwiadevmgr2-enumdeviceinfo.md) .                                            | Enumera i dispositivi WIA disponibili e fornisce i puntatori alle interfacce [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) . |
| [**\_Informazioni sul formato IEnumWIA \_**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info) | Chiamare un metodo [**IWiaDataTransfer:: idtEnumWIA \_ Format \_ info**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtenumwia_format_info) per un elemento.                                                                              | Enumera tutte le informazioni sul formato di immagine fornite da un elemento WIA.                                                                    |
| [**IEnumWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwiaitem)                   | Chiamare un metodo [**IWiaItem:: EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) o [**IWiaItem2:: ENUMCHILDITEMS**](-wia-iwiaitem2-enumchilditems.md) dell'elemento WIA.                                          | Enumera gli elementi figlio di un elemento WIA che rappresenta un dispositivo o una cartella.                                                |



 

 

 
