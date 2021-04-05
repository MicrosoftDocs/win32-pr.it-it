---
description: Il provider WDM (Windows Driver Model) concede l'accesso alle classi, alle istanze, ai metodi e agli eventi dei driver hardware conformi al modello WDM.
ms.assetid: 2f9749ff-b318-4228-80fd-e3846dde21d2
title: Provider WDM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d96ce356214f2788d3608b2ba85943e607394cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753711"
---
# <a name="wdm-provider"></a>Provider WDM

Il provider WDM (Windows Driver Model) concede l'accesso alle classi, alle istanze, ai metodi e agli eventi dei driver hardware conformi al modello WDM. Le classi per i driver hardware si trovano nello " \\ spazio dei nomi WMI radice".

Le classi WDM sono definite principalmente in WMI. mof.

WDM è un'interfaccia del sistema operativo tramite la quale i componenti hardware forniscono informazioni e notifiche degli eventi. Il provider WDM è una classe, un'istanza, un evento e un provider di metodi che consente alle applicazioni di gestione di accedere a dati ed eventi da driver di dispositivo abilitati per WMI per WDM. Le classi create dal provider WDM per rappresentare i dati dei driver di dispositivo risiedono solo nello \\ spazio dei nomi "WMI radice". Questo spazio dei nomi deve esistere già prima che il provider WDM elabori i driver WDM installati.

Il provider WDM registra le informazioni sulle operazioni WDM nel file WmiProv. log. Per ulteriori informazioni, vedere [file di log WMI](/windows/desktop/WmiSdk/wmi-log-files).

Come classe, istanza, metodo e provider di eventi, il provider WDM implementa l'interfaccia [**IWbemProviderInit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) standard, oltre ai metodi [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) seguenti:

-   [**CreateClassEnumAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createclassenumasync)
-   [**CreateInstanceEnumAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenumasync)
-   [**GetObjectAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-getobjectasync)
-   [**ExecMethodAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethodasync)
-   [**ExecNotificationQueryAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execnotificationqueryasync)
-   [**ExecQueryAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execqueryasync)
-   [**PutInstanceAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-putinstanceasync)

Il provider WDM supporta l'evento estrinseco [**WmiEvent**](/windows/desktop/WmiCoreProv/wmievent) , che informa WMI sugli eventi di driver basati su WDM. È possibile registrare i consumer di eventi per gli eventi **WmiEvent** come per qualsiasi altro evento. Per ulteriori informazioni, vedere [ricezione di un evento WMI](/windows/desktop/WmiSdk/receiving-a-wmi-event). Quando si avvia un driver non viene generato alcun evento di creazione della classe.

Il provider WDM supporta la classe seguente:

-   [**WMIBinaryMofResource**](wmibinarymofresource.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Provider WMI](/windows/desktop/WmiSdk/wmi-providers)
</dt> <dt>

[Accesso ai dati dai driver di dispositivo](/windows/desktop/WmiSdk/accessing-data-from-device-drivers)
</dt> </dl>

 

 
