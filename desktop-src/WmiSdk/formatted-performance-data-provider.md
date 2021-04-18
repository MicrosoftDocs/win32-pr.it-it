---
description: Fornisce calcolato (&\# 0034; cotto&\# 0034;) dati del contatore delle prestazioni. Fornisce dati dinamici alle classi WMI derivate da Win32 \_ PerfFormattedData. Noto anche come provider di contatori cotti.
ms.assetid: 59823f7c-3046-4608-99df-1f43e2934e7e
ms.tgt_platform: multiple
title: provider di dati delle prestazioni formattate
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0db075ebdafcd31c7aa0980d191ed565873f686f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310352"
---
# <a name="formatted-performance-data-provider"></a>provider di dati delle prestazioni formattate

\[Il provider di dati delle prestazioni formattato, noto anche come "provider del contatore cotto", non è più disponibile per l'uso. Usare invece il provider [wmiperfinst](wmiperfinst-provider.md) .\]

Il provider di dati prestazioni formattato a prestazioni elevate fornisce dati del contatore delle prestazioni calcolati (cotti), ad esempio la percentuale di tempo impiegato da un disco per la scrittura dei dati. Questo provider fornisce dati dinamici alle classi WMI derivate da [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata). La differenza tra questo provider e il [provider del contatore delle](performance-counter-provider.md) prestazioni è che il provider del contatore delle prestazioni fornisce dati non elaborati e il provider del contatore cotto fornisce dati sulle prestazioni che vengono visualizzati esattamente come in [*Monitor di sistema*](gloss-s.md). Il nome dell'istanza di [**\_ \_ Win32Provider**](--win32provider.md) è "HiPerfCooker \_ V1".

Il nome della classe formattata WMI per un oggetto contatore è nel formato " \_ nome \_ *oggetto \_ nome servizio* PerfFormattedData Win32 \_ *\_*". Ad esempio, il nome della classe WMI che contiene i contatori del disco logico è **Win32 \_ PerfFormattedData \_ perfdisk \_ disco logico**. Queste classi si trovano nello \\ spazio dei nomi "root CIMv2".

Poiché le classi di dati sulle prestazioni vengono aggiunte e modificate in modo dinamico in un determinato sistema, non è possibile documentare formalmente le proprietà di tutti gli oggetti prestazioni noti. Per determinare quali classi sono disponibili e per identificare i membri di tali classi, vedere [recupero della documentazione per oggetti dati sulle prestazioni non elaborati e formattati](retrieving-raw-and-formatted-performance-data.md).

Le classi [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) utilizzano il qualificatore **CookingType** nei [tipi di contatori delle prestazioni WMI](wmi-performance-counter-types.md) per specificare la formula per il calcolo dei dati sulle prestazioni. Questo qualificatore è uguale al qualificatore **CounterType** nelle classi [**\_ PerfRawData Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) .

Come provider a prestazioni elevate, il provider del contatore cotto implementa l'interfaccia [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) standard, nonché il metodo [**IWbemRefresher:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) e i metodi [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) seguenti:

-   [**CreateRefreshableEnum**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableenum)
-   [**CreateRefreshableObject**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableobject)
-   [**CreateRefresher**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefresher)
-   [**GetObjects**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-getobjects)
-   [**QueryInstances**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-queryinstances)
-   [**StopRefreshing**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-stoprefreshing)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Provider WMI](wmi-providers.md)
</dt> </dl>

 

 
