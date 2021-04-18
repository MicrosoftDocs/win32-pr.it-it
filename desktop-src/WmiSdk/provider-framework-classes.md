---
description: Le classi C++ WMI che fanno parte del Framework del provider WMI sono ora considerate in stato finale.
ms.assetid: 062a7724-0589-4e9d-af7a-39fd9c08e40b
ms.tgt_platform: multiple
title: Classi del Framework del provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1562d00e6b3b1563ece933ba7dd9361dd8a5d94f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313181"
---
# <a name="provider-framework-classes"></a>Classi del Framework del provider

\[Le classi WMI C++ che fanno parte del Framework del provider WMI sono ora considerate in stato finale e non sono disponibili ulteriori attività di sviluppo, miglioramenti o aggiornamenti per i problemi non correlati alla sicurezza che interessano queste librerie. Le [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devono essere usate per tutte le nuove attività di sviluppo.\]

Il Framework del provider implementa le classi seguenti.



| Classe Framework                                | Descrizione                                                                                                                                                                                                         |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CFrameworkQuery**](/windows/desktop/api/FrQuery/nl-frquery-cframeworkquery)     | Contiene i metodi per l'elaborazione delle query.                                                                                                                                                                              |
| [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance)                 | Contiene i metodi per impostare e recuperare le proprietà ed è un incapsulamento dell'interfaccia [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) . L'implementatore non deve necessariamente accedere direttamente ai metodi **IWbemClassObject** . |
| [**CThreadBase**](/windows/desktop/api/ThrdBase/nl-thrdbase-cthreadbase)             | Classe di base che fornisce i meccanismi di thread safety interni per il Framework del provider WMI.                                                                                                                    |
| [**CWbemGlueFactory**](/windows/desktop/api/WbemGlue/nl-wbemglue-cwbemgluefactory)   | Parte del Framework del provider WMI. Il Framework del provider implementa i metodi di questa interfaccia internamente per creare nuove istanze delle classi per il provider.                                                     |
| [**CWbemProviderGlue**](/windows/desktop/api/WbemGlue/nl-wbemglue-cwbemproviderglue) | Implementa [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) e i metodi che controllano il caricamento e lo scaricamento del provider del Framework.                                                                             |
| [**Provider**](/windows/desktop/api/Provider/nl-provider-provider)                   | Contiene funzioni helper e fornisce implementazioni predefinite dei metodi di [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices).                                                                                            |



 

Si noti che molti dei metodi del Framework usano i parametri [**CHString**](chstring.md) . **CHString** supporta molti degli stessi metodi e proprietà del Microsoft Foundation Classes (MFC), ma senza l'overhead di MFC. Per ulteriori informazioni su **CHString**, vedere la pagina relativa al **riferimento alla classe CHString**.

 

 
