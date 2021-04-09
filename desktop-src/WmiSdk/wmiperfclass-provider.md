---
description: A partire da Windows Vista, questo provider crea le classi del contatore delle prestazioni WMI.
ms.assetid: 5bb3d5e0-cdeb-4fea-a8ca-cf934e056206
ms.tgt_platform: multiple
title: Provider WmiPerfClass
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 941422211ac9892406181ac0271e0d50239eef1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050118"
---
# <a name="wmiperfclass-provider"></a>Provider WmiPerfClass

A partire da Windows Vista, questo provider crea le [classi del contatore delle prestazioni](/windows/desktop/CIMWin32Prov/performance-counter-classes)WMI. I dati vengono forniti dinamicamente a queste classi di prestazioni WMI dal provider [wmiperfinst](wmiperfinst-provider.md) . Il processo di individuazione automatica/AutoPurge (ADAP) non trasferisce più gli oggetti contatore delle prestazioni in classi di prestazioni WMI nel repository WMI. Per ulteriori informazioni, vedere [librerie di prestazioni e WMI](performance-libraries-and-wmi.md).

Per ulteriori informazioni, vedere [librerie di prestazioni e WMI](performance-libraries-and-wmi.md).

Sebbene non sia consigliabile sviluppare nuovi oggetti prestazione creando un provider WMI a prestazioni elevate e dipendono dal processo di [*adattamento dell'adattatore ADAP*](gloss-r.md) per trasferire i dati alle librerie di prestazioni, l'eccezione riguarda lo sviluppo di un driver Windows Driver Model che fornisce dati sulle prestazioni. Mentre il processo dell'adattatore inverso continua a funzionare per la compatibilità con le versioni precedenti, il metodo consigliato prevede l'uso dei [contatori delle prestazioni versione 6,0](/windows/desktop/PerfCtrs/performance-counters-portal).

Il nome dell'istanza di [**\_ \_ Win32Provider**](--win32provider.md) di questo provider è "wmiperfclass".

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Provider WMI](wmi-providers.md)
</dt> <dt>

[Librerie di prestazioni e WMI](performance-libraries-and-wmi.md)
</dt> <dt>

[Monitoraggio dei dati sulle prestazioni](monitoring-performance-data.md)
</dt> </dl>

 

 
