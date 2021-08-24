---
description: Le classi dei contatori delle prestazioni consentono l'accesso di script e programmi ai dati sulle prestazioni del sistema calcolati dai provider esistenti a prestazioni elevate.
ms.assetid: 71746363-6fec-4344-8c5e-5cc057ebdf76
ms.tgt_platform: multiple
title: Classi di contatori delle prestazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc66020fc7863153e3e663c7552ee6805b2a676772fdcbf01cd9683a9ec05486
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119701651"
---
# <a name="performance-counter-classes"></a>Classi di contatori delle prestazioni

Le classi dei contatori delle prestazioni consentono l'accesso di script e programmi ai dati sulle prestazioni del sistema calcolati dai provider esistenti a prestazioni elevate. Queste classi sono costituite da classi di contatori delle prestazioni non elaborati e classi di contatori delle prestazioni formattate.

Provider diversi forniscono dati della libreria delle prestazioni tramite WMI. I [provider WMIPerfClass](/windows/desktop/WmiSdk/wmiperfclass-provider) e [WMIPerfInst](/windows/desktop/WmiSdk/wmiperfinst-provider) forniscono classi sia per i contatori delle prestazioni versione 1 che [2.](/windows/desktop/PerfCtrs/performance-counters-portal) Questi provider mantengono la compatibilità con le classi disponibili nei sistemi operativi precedenti.

Le classi in questa sezione sono le classi di base astratte usate per creare classi di contatori delle prestazioni. Questo non è un elenco completo delle classi che è possibile trovare nel sistema operativo. Per altre informazioni, vedere [Librerie delle prestazioni e WMI.](/windows/desktop/WmiSdk/performance-libraries-and-wmi)

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[**Win32 \_ Perf**](win32-perf.md)
</dt> <dd>

Classe di base per le classi del contatore delle prestazioni [**Win32 \_ PerfRawData**](win32-perfrawdata.md) e [**Win32 \_ PerfFormattedData**](win32-perfformatteddata.md).

</dd> <dt>

[**Win32 \_ PerfFormattedData**](win32-perfformatteddata.md)
</dt> <dd>

classe di base astratta per le classi di dati calcolate preinstallato.

</dd> <dt>

[**Win32 \_ PerfRawData**](win32-perfrawdata.md)
</dt> <dd>

Classe di base astratta per tutte le classi di contatori delle prestazioni non elaborati concrete.

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Classi Win32](win32-provider.md)
</dt> </dl>

 

 
