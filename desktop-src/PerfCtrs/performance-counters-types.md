---
description: PDH definisce i tipi di dati seguenti.
ms.assetid: 8a2e8683-502a-4893-8b4f-5e2cf464a933
title: Tipi di dati dei contatori delle prestazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38f9800288494eb82f675265b6e0b801c783668d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312107"
---
# <a name="performance-counters-data-types"></a>Tipi di dati dei contatori delle prestazioni

## <a name="performance-data-helper-pdh-types"></a>Tipi PDH (Performance Data Helper)

I consumer che utilizzano le funzioni [PDH (Performance Data Helper)](using-the-pdh-functions-to-consume-counter-data.md) utilizzano i tipi seguenti:

| Tipo di dati | Descrizione
|-----------|------------
| **\_HQUERY PDH**   | Handle per una query. La funzione [**PdhOpenQuery**](/windows/win32/api/pdh/nf-pdh-pdhopenqueryw) restituisce questo handle. Chiudere l'handle utilizzando [**PdhCloseQuery**](/windows/win32/api/pdh/nf-pdh-pdhclosequery).
| **\_HCOUNTER PDH** | Handle per un contatore. La funzione [**chiamata PdhAddCounter**](/windows/win32/api/pdh/nf-pdh-pdhaddcounterw) restituisce questo handle. Chiudere l'handle utilizzando [**PdhRemoveCounter**](/windows/win32/api/pdh/nf-pdh-pdhremovecounter) o chiudendo l'handle alla query che contiene il contatore. Non chiamare **PdhRemoveCounter** su un contatore se la query corrispondente è già stata chiusa. PDH gestisce il collegamento tra contatori e query e chiude automaticamente gli handle del contatore quando viene chiuso l'handle di query corrispondente.
| **\_numero PDH**     | Handle per un file di log. Le funzioni [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga) e [**PdhBindInputDataSource**](/windows/desktop/api/Pdh/nf-pdh-pdhbindinputdatasourcea) restituiscono questo handle. Chiudere l'handle utilizzando [**PdhCloseLog**](/windows/win32/api/pdh/nf-pdh-pdhcloselog).
| **\_stato PDH**   | Valore di stato di PDH. Tutte le funzioni PDH restituiscono un valore di tipo **PDH \_**. Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success. In caso contrario, la funzione restituisce un [codice di errore di sistema](/windows/desktop/Debug/system-error-codes) o un codice di [errore PDH](pdh-error-codes.md).
