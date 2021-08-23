---
description: Il provider WDM (Windows Driver Model) concede l'accesso a classi, istanze, metodi ed eventi dei driver hardware conformi al modello WDM.
ms.assetid: 2f9749ff-b318-4228-80fd-e3846dde21d2
title: WDM Provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54ba187680ec371f331aa6394c5a2408c23080259e6b275e74cee496dd5125cb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794621"
---
# <a name="wdm-provider"></a>WDM Provider

Il provider WDM (Windows Driver Model) concede l'accesso a classi, istanze, metodi ed eventi dei driver hardware conformi al modello WDM. Le classi per i driver hardware si trovano nello "spazio dei \\ nomi WMI radice".

Le classi WDM sono definite principalmente in Wmi.mof.

WDM è un'interfaccia del sistema operativo tramite la quale i componenti hardware forniscono informazioni e notifiche degli eventi. Il provider WDM è un provider di classi, istanze, eventi e metodi che consente alle applicazioni di gestione di accedere ai dati e agli eventi dai driver di dispositivo abilitati per WMI per WDM. Le classi create dal provider WDM per rappresentare i dati dei driver di dispositivo risiedono solo nello spazio dei nomi \\ "Root WMI". Questo spazio dei nomi deve esistere già prima che il provider WDM eelaborare i driver WDM installati.

Il provider WDM registra informazioni sulle operazioni WDM nel file WmiProv.log. Per altre informazioni, vedere [File di log WMI.](/windows/desktop/WmiSdk/wmi-log-files)

Come classe, istanza, metodo e provider di eventi, il provider WDM implementa [**l'interfaccia IWbemProviderInit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) standard, nonché i metodi [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) seguenti:

-   [**CreateClassEnumAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createclassenumasync)
-   [**CreateInstanceEnumAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenumasync)
-   [**GetObjectAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-getobjectasync)
-   [**ExecMethodAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethodasync)
-   [**ExecNotificationQueryAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execnotificationqueryasync)
-   [**ExecQueryAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execqueryasync)
-   [**PutInstanceAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-putinstanceasync)

Il provider WDM supporta l'evento estrinsic [**WMIEvent,**](/windows/desktop/WmiCoreProv/wmievent) che invia una notifica a WMI in merito agli eventi dei driver basati su WDM. È possibile registrare i consumer di eventi **per gli eventi WMIEvent** come qualsiasi altro evento. Per altre informazioni, vedere [Ricezione di un evento WMI.](/windows/desktop/WmiSdk/receiving-a-wmi-event) All'avvio di un driver non vengono generati eventi di creazione di classi.

Il provider WDM supporta la classe seguente:

-   [**WMIBinaryMofResource**](wmibinarymofresource.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Provider WMI](/windows/desktop/WmiSdk/wmi-providers)
</dt> <dt>

[Accesso ai dati dai driver di dispositivo](/windows/desktop/WmiSdk/accessing-data-from-device-drivers)
</dt> </dl>

 

 
