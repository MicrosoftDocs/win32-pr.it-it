---
description: La formula del tipo di contatore della varianza del COOKer \_ fornisce la variabilità che consente di caratterizzare la dispersione per un set di osservazioni non elaborate di una proprietà in un'istanza di Win32 \_ PerfRawData.
ms.assetid: 6b184a36-7d22-41ab-98e7-b185d1063bcb
ms.tgt_platform: multiple
title: COOKER_VARIANCE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef0f9de6c5241ccd486e4da76864139e3e54f5a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049816"
---
# <a name="cooker_variance"></a>varianza del COOKer \_

La formula del tipo di contatore della varianza del COOKer \_ fornisce la variabilità che consente di caratterizzare la dispersione per un set di osservazioni non elaborate di una proprietà in un'istanza di [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) . La varianza viene calcolata dividendo la somma del quadrato della deviazione dalla media di ogni contatore per il numero di contatori. In altre parole, la varianza corrisponde alla media delle deviazioni al quadrato dalla media per ogni contatore. Questo tipo di contatore viene definito solo all'interno di WMI e non è disponibile per le tecnologie di monitoraggio delle prestazioni, ad esempio i [contatori delle prestazioni versione 6,0](/windows/desktop/PerfCtrs/performance-counters-portal).

Per ulteriori informazioni sulla formula del tipo di contatore, vedere [tipi di contatori](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)).

Per ulteriori informazioni sui provider a prestazioni elevate e sullo scripting, vedere [tipi di contatori delle prestazioni WMI](wmi-performance-counter-types.md).

## <a name="example-code"></a>Codice di esempio

Per esempi di codice, vedere [ottenere dati statistici sulle prestazioni](obtaining-statistical-performance-data.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di contatori statistici](statistical-counter-types.md)
</dt> <dt>

[Monitoraggio dei dati sulle prestazioni](monitoring-performance-data.md)
</dt> </dl>

 

 
