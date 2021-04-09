---
description: Le classi dei contatori delle prestazioni consentono l'accesso allo script e al programma ai dati sulle prestazioni del sistema calcolati dai provider a prestazioni elevate esistenti.
ms.assetid: 71746363-6fec-4344-8c5e-5cc057ebdf76
ms.tgt_platform: multiple
title: Classi del contatore delle prestazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d147e5ebc18dfe532ceec7a2fb55bb21c6fa13f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878390"
---
# <a name="performance-counter-classes"></a>Classi del contatore delle prestazioni

Le classi dei contatori delle prestazioni consentono l'accesso allo script e al programma ai dati sulle prestazioni del sistema calcolati dai provider a prestazioni elevate esistenti. Queste classi sono costituite da classi di contatori delle prestazioni non elaborate e classi di contatori delle prestazioni formattate

Provider diversi forniscono dati della libreria delle prestazioni tramite WMI. I provider [wmiperfclass](/windows/desktop/WmiSdk/wmiperfclass-provider) e [wmiperfinst](/windows/desktop/WmiSdk/wmiperfinst-provider) forniscono classi per i [contatori delle prestazioni](/windows/desktop/PerfCtrs/performance-counters-portal)versione 1 e versione 2. Questi provider mantengono la compatibilità con le classi disponibili nei sistemi operativi precedenti.

Le classi in questa sezione sono le classi di base astratte utilizzate per creare classi dei contatori delle prestazioni. Non si tratta di un elenco completo delle classi che è possibile trovare nel sistema operativo. Per ulteriori informazioni, vedere [librerie di prestazioni e WMI](/windows/desktop/WmiSdk/performance-libraries-and-wmi).

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[**\_Prestazioni Win32**](win32-perf.md)
</dt> <dd>

Classe base per le classi del contatore delle prestazioni [**Win32 \_ PerfRawData**](win32-perfrawdata.md) e [**Win32 \_ PerfFormattedData**](win32-perfformatteddata.md).

</dd> <dt>

[**\_PerfFormattedData Win32**](win32-perfformatteddata.md)
</dt> <dd>

classe di base astratta per le classi di dati calcolate pre-installate.

</dd> <dt>

[**\_PerfRawData Win32**](win32-perfrawdata.md)
</dt> <dd>

Classe di base astratta per tutte le classi del contatore delle prestazioni raw concrete.

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Classi Win32](win32-provider.md)
</dt> </dl>

 

 
