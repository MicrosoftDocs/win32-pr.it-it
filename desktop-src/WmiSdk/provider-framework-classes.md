---
description: Informazioni sulle classi C++ WMI che fanno parte di WMI Provider Framework e sono ora considerate in stato finale.
ms.assetid: 062a7724-0589-4e9d-af7a-39fd9c08e40b
ms.tgt_platform: multiple
title: Classi del framework del provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bf4ef94b25e51b7f012987552babd30a93e7792
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120446"
---
# <a name="provider-framework-classes"></a>Classi del framework del provider

\[Le classi C++ WMI che fanno parte di WMI Provider Framework sono ora considerate in stato finale e non saranno disponibili altri aggiornamenti, miglioramenti o sviluppo per problemi non correlati alla sicurezza che interessano queste librerie. Le [API MI devono essere](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) usate per tutti i nuovi sviluppi.\]

Il framework del provider implementa le classi seguenti.



| Classe framework                                | Descrizione                                                                                                                                                                                                         |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CFrameworkQuery**](/windows/desktop/api/FrQuery/nl-frquery-cframeworkquery)     | Contiene metodi per l'elaborazione delle query.                                                                                                                                                                              |
| [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance)                 | Contiene metodi per impostare e recuperare proprietà ed è un incapsulamento [**dell'interfaccia IWbemClassObject.**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) L'implementatore non deve accedere direttamente ai **metodi IWbemClassObject.** |
| [**CThreadBase**](/windows/desktop/api/ThrdBase/nl-thrdbase-cthreadbase)             | Classe di base che fornisce i meccanismi thread safety per il framework del provider WMI.                                                                                                                    |
| [**CWbemGlueFactory**](/windows/desktop/api/WbemGlue/nl-wbemglue-cwbemgluefactory)   | Parte del framework del provider WMI. Il framework del provider implementa internamente i metodi di questa interfaccia per creare nuove istanze di classi per il provider.                                                     |
| [**CWbemProviderGlue**](/windows/desktop/api/WbemGlue/nl-wbemglue-cwbemproviderglue) | Implementa [**IWbemProviderInit e**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) i metodi che controllano il caricamento e lo scaricamento del provider di framework.                                                                             |
| [**Provider**](/windows/desktop/api/Provider/nl-provider-provider)                   | Contiene funzioni helper e fornisce implementazioni predefinite dei metodi di [**IWbemServices.**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)                                                                                            |



 

Si noti che molti dei metodi del framework usano [**parametri CHString.**](chstring.md) **CHString** supporta molti degli stessi metodi e proprietà di Microsoft Foundation Classes (MFC), ma senza l'overhead di MFC. Per altre informazioni su **CHString,** vedere **Riferimento alla classe CHString**.

 

 
