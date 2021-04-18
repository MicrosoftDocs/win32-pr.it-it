---
description: Non è consigliabile scrivere un provider WMI a prestazioni elevate per creare contatori delle prestazioni.
ms.assetid: 6a22d6f7-d9e2-45fa-876d-921a4bc4f574
ms.tgt_platform: multiple
title: Creazione di un provider di istanze in un provider di High-Performance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10744b110463a3207f76bb55d48a8045ec22783d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312692"
---
# <a name="making-an-instance-provider-into-a-high-performance-provider"></a>Creazione di un provider di istanze in un provider di High-Performance

Non è consigliabile scrivere un provider WMI a prestazioni elevate per creare contatori delle prestazioni. A partire da Windows Vista, le [classi del contatore delle prestazioni](/windows/desktop/CIMWin32Prov/performance-counter-classes) WMI non vengono più migrate nelle librerie delle prestazioni di Windows tramite l'adattatore inverso AutoDiscovery/AutoPurge (ADAP). Per creare un provider del contatore delle prestazioni, utilizzare i [contatori delle prestazioni versione 2,0](/windows/desktop/PerfCtrs/performance-counters-portal). Dopo aver creato gli oggetti della libreria di prestazioni, il [provider WMIPerfClass](wmiperfclass-provider.md) analizza gli oggetti e crea o aggiorna una classe WMI derivata da [**\_ Perf Win32**](/windows/desktop/CIMWin32Prov/win32-perf) per ogni oggetto prestazione. Il [provider WMIPerfInst](wmiperfinst-provider.md) fornisce quindi dinamicamente i dati dei contatori delle prestazioni non elaborati e formattati alle classi di prestazioni WMI.

Nella procedura di alto livello riportata di seguito vengono illustrati i passaggi necessari per creare un provider a prestazioni elevate.

**Per creare un provider a prestazioni elevate**

1.  Registrare il provider con WMI. Per ulteriori informazioni, vedere la pagina relativa alla [registrazione di un provider di High-Performance](registering-a-high-performance-provider.md).
2.  Implementare il provider. Per ulteriori informazioni, vedere [scrittura di un provider di istanze](writing-an-instance-provider.md).
3.  Implementare l'interfaccia a prestazioni elevate. Per ulteriori informazioni, vedere [implementazione dell'interfaccia High-Performance](implementing-the-high-performance-interface.md).
4.  Derivare e scrivere lo schema di Managed Object Format (MOF) per ottenere i dati sulle prestazioni non elaborati. Per ulteriori informazioni, vedere [supporto della \_ classe Win32 PerfRawData](supporting-the-win32-perfrawdata-class.md).
5.  Derivare e scrivere lo schema MOF per ottenere i dati precalcolati. Grazie al supporto di questa classe, il provider non è necessario per eseguire i calcoli. Questi dati saranno gli stessi visualizzati in monitoraggio di sistema in Perfmon. Per ulteriori informazioni, vedere [supporto della \_ classe Win32 PerfFormattedData](supporting-the-win32-perfformatteddata-class.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sviluppo di un provider WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Librerie di prestazioni e WMI](performance-libraries-and-wmi.md)
</dt> </dl>

 

 
