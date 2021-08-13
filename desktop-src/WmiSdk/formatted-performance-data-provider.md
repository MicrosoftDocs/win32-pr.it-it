---
description: Supplies calculated (&\# 0034;&\# 0034;) dati dei contatori delle prestazioni. Fornisce dati dinamici alle classi WMI derivate da \_ Win32 PerfFormattedData. Noto anche come provider di contatori delle prestazioni.
ms.assetid: 59823f7c-3046-4608-99df-1f43e2934e7e
ms.tgt_platform: multiple
title: Prestazioni formattate provider di dati
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ab8e931c3d03c619af5b1e37cadd8dacdccd21534513ed3a1aa1d7b9076acfb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118556614"
---
# <a name="formatted-performance-data-provider"></a>Prestazioni formattate provider di dati

\[Il provider di provider di dati formattato, noto anche come "provider di contatori delle prestazioni", non è più disponibile per l'uso. Usare invece il provider [WMIPerfInst.](wmiperfinst-provider.md)\]

Il provider di dati sulle prestazioni formattato a prestazioni elevate fornisce dati calcolati del contatore delle prestazioni ("a prestazioni elevate"), ad esempio la percentuale di tempo che un disco impiega per la scrittura dei dati. Questo provider fornisce dati dinamici alle classi WMI derivate da [**Win32 \_ PerfFormattedData.**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) La differenza tra questo provider e il [provider](performance-counter-provider.md) del contatore delle prestazioni è che il provider del contatore delle prestazioni fornisce dati non elaborati e il provider contatore delle prestazioni fornisce dati sulle prestazioni che vengono visualizzati esattamente come in [*Monitoraggio di sistema.*](gloss-s.md) Il [**\_ \_ nome dell'istanza Win32Provider**](--win32provider.md) è "HiPerfCooker \_ v1".

Il nome della classe formattata WMI per un oggetto contatore è nel formato "Win32 \_ PerfFormattedData \_ *service \_ name* \_ *object \_ name*". Ad esempio, il nome della classe WMI che contiene i contatori dei dischi logici è **\_ Win32 PerfFormattedData \_ PerfDisk \_ LogicalDisk**. Queste classi si trovano nello spazio dei nomi "Root \\ CIMv2".

Poiché le classi di dati delle prestazioni vengono aggiunte e modificate dinamicamente in un determinato sistema, non è possibile documentare formalmente le proprietà di tutti gli oggetti prestazioni noti. Per determinare le classi disponibili e per identificare i membri di tali classi, vedere Recupero della documentazione per oggetti dati non elaborati e formattati [delle prestazioni.](retrieving-raw-and-formatted-performance-data.md)

Le [**classi \_ PerfFormattedData Win32**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) usano il qualificatore PerfFormattedData in Tipi di contatori delle prestazioni [WMI](wmi-performance-counter-types.md) per specificare la formula per il calcolo dei dati sulle prestazioni.  Questo qualificatore corrisponde al qualificatore **CounterType** nelle [**classi \_ PerfRawData Win32.**](/windows/desktop/CIMWin32Prov/win32-perfrawdata)

In qualità di provider ad alte prestazioni, il provider del contatore delle operazioni di controllo delle prestazioni implementa l'interfaccia [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) standard, nonché il metodo [**IWbemRefresher::Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) e i metodi [**IWbemHiPerfProvider seguenti:**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider)

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

 

 
