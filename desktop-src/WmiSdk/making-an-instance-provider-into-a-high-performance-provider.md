---
description: Non è consigliabile scrivere un provider WMI ad alte prestazioni per creare contatori delle prestazioni.
ms.assetid: 6a22d6f7-d9e2-45fa-876d-921a4bc4f574
ms.tgt_platform: multiple
title: Creazione di un provider di istanze in un provider High-Performance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2b6326c0af270088c37bb2a1798951ba0a9de7afe65ec593f5f7ab6768b83b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996491"
---
# <a name="making-an-instance-provider-into-a-high-performance-provider"></a>Creazione di un provider di istanze in un provider High-Performance

Non è consigliabile scrivere un provider WMI ad alte prestazioni per creare contatori delle prestazioni. A partire da Windows Vista, le classi dei contatori delle prestazioni [WMI](/windows/desktop/CIMWin32Prov/performance-counter-classes) non vengono più migrate nelle librerie delle prestazioni di Windows dalla scheda inversa AutoDiscovery/AutoPurge (ADAP). Per creare un provider di contatori delle prestazioni, [usare i contatori delle prestazioni versione 2.0.](/windows/desktop/PerfCtrs/performance-counters-portal) Dopo aver creato gli oggetti della libreria delle prestazioni, il [provider WMIPerfClass](wmiperfclass-provider.md) analizza gli oggetti e crea o aggiorna una classe WMI derivata da [**Win32 \_ Perf**](/windows/desktop/CIMWin32Prov/win32-perf) per ogni oggetto prestazioni. Il [provider WMIPerfInst fornisce](wmiperfinst-provider.md) quindi dinamicamente i dati dei contatori delle prestazioni non elaborati e formattati alle classi di prestazioni WMI.

La procedura di alto livello seguente illustra i passaggi necessari per creare un provider a prestazioni elevate.

**Per creare un provider ad alte prestazioni**

1.  Registrare il provider con WMI. Per altre informazioni, vedere [Registrazione di un provider High-Performance .](registering-a-high-performance-provider.md)
2.  Implementare il provider. Per altre informazioni, vedere [Scrittura di un provider di istanze.](writing-an-instance-provider.md)
3.  Implementare l'interfaccia ad alte prestazioni. Per altre informazioni, vedere [Implementing the High-Performance Interface](implementing-the-high-performance-interface.md).
4.  Derivare e scrivere lo schema Managed Object Format (MOF) per ottenere dati sulle prestazioni non elaborati. Per altre informazioni, vedere [Supporto della classe \_ PerfRawData Win32.](supporting-the-win32-perfrawdata-class.md)
5.  Derivare e scrivere lo schema MOF per ottenere dati precalcolati. Supportando questa classe, il provider non è necessario per eseguire i calcoli. Questi dati saranno gli stessi visualizzati in Monitoraggio di sistema in Perfmon. Per altre informazioni, vedere [Supporto della classe \_ PerfFormattedData Win32.](supporting-the-win32-perfformatteddata-class.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sviluppo di un provider WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Librerie delle prestazioni e WMI](performance-libraries-and-wmi.md)
</dt> </dl>

 

 
