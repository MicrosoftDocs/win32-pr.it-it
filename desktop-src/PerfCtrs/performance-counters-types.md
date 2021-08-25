---
description: PDH definisce i tipi di dati seguenti.
ms.assetid: 8a2e8683-502a-4893-8b4f-5e2cf464a933
title: Tipi di dati dei contatori delle prestazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23208978cfc3c0a67c7547598f26e506a5571a54d0d5ddfc93b7ecff38f9c559
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674741"
---
# <a name="performance-counters-data-types"></a>Tipi di dati dei contatori delle prestazioni

## <a name="performance-data-helper-pdh-types"></a>Tipi PDH (Performance Data Helper)

I consumer che usano [le funzioni PDH (Performance Data Helper)](using-the-pdh-functions-to-consume-counter-data.md) usano i tipi seguenti:

| Tipo di dati | Descrizione
|-----------|------------
| **PDH \_ HQUERY**   | Handle per una query. La [**funzione PdhOpenQuery**](/windows/win32/api/pdh/nf-pdh-pdhopenqueryw) restituisce questo handle. Chiudere l'handle [**usando PdhCloseQuery**](/windows/win32/api/pdh/nf-pdh-pdhclosequery).
| **PDH \_ HCOUNTER** | Handle per un contatore. La [**funzione PdhAddCounter**](/windows/win32/api/pdh/nf-pdh-pdhaddcounterw) restituisce questo handle. Chiudere l'handle [**usando PdhRemoveCounter**](/windows/win32/api/pdh/nf-pdh-pdhremovecounter) o chiudendo l'handle per la query che contiene il contatore. Non chiamare **PdhRemoveCounter** su un contatore se la query corrispondente è già stata chiusa. PDH mantiene il collegamento tra contatori e query e chiude automaticamente gli handle dei contatori alla chiusura dell'handle di query corrispondente.
| **PDH \_ HLOG**     | Handle per un file di log. Le [**funzioni PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga) e [**PdhBindInputDataSource**](/windows/desktop/api/Pdh/nf-pdh-pdhbindinputdatasourcea) restituiscono questo handle. Chiudere l'handle [**usando PdhCloseLog**](/windows/win32/api/pdh/nf-pdh-pdhcloselog).
| **STATO \_ PDH**   | Valore di stato PDH. Tutte le funzioni PDH restituiscono un valore di **tipo PDH \_ STATUS**. Se la funzione ha esito positivo, il valore restituito è ERROR \_ SUCCESS. In caso contrario, la funzione restituisce un [codice di errore di sistema](/windows/desktop/Debug/system-error-codes) o un codice di errore [PDH](pdh-error-codes.md).
