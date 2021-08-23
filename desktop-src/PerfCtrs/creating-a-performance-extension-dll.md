---
description: Un provider è una DLL delle prestazioni che fornisce i dati dei contatori ai consumer.
ms.assetid: bbb777fe-b97e-4777-b797-ec8525065610
title: Creazione di una DLL dell'estensione per le prestazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1ef4509af77bcc1a4016e494a2834d40162305a837349e32a573cbf36d994d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011319"
---
# <a name="creating-a-performance-extension-dll"></a>Creazione di una DLL dell'estensione per le prestazioni

> [!IMPORTANT]
> A causa di limitazioni significative di prestazioni e affidabilità, il metodo per fornire i dati dei contatori delle prestazioni descritti in questo argomento potrebbe essere modificato o non disponibile in futuro. Microsoft consiglia invece di usare il metodo descritto in Fornire dati dei contatori usando la [versione 2.0 per](providing-counter-data-using-version-2-0.md) la creazione di nuovi contatori delle prestazioni e di eseguire la migrazione dei contatori delle prestazioni esistenti per usare anche tale metodo.

Un [provider V1](providing-counter-data.md) usa una DLL delle prestazioni che fornisce i dati dei contatori ai consumer. La DLL delle prestazioni deve esportare [**le funzioni OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)), [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc)e [**ClosePerformanceData.**](/windows/win32/api/winperf/nc-winperf-pm_close_proc) In genere, si usa un file di definizione del modulo (def) per esportare le funzioni dalla DLL. Il sistema chiama queste funzioni quando un consumer esegue query sui dati sulle prestazioni.

La prima volta che un consumer chiama [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa)o se il consumer usa la funzione [**RegOpenKey**](/windows/desktop/api/winreg/nf-winreg-regopenkeya) o [**RegConnectRegistry**](/windows/desktop/api/winreg/nf-winreg-regconnectregistrya) per aprire , il sistema chiama la funzione `HKEY_PERFORMANCE_DATA` [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) per ogni provider registrato nel computer. [](adding-performance-counters.md) L'eccezione è se il provider specifica l'elenco di oggetti supportati nella sezione del `[objects]` file .INI file. In questo caso, il sistema chiama il provider solo se uno degli oggetti sottoposti a query corrisponde a un oggetto dell'elenco.

La [**funzione OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) offre a ogni provider la possibilità di inizializzare le strutture dei dati sulle prestazioni. Quindi, se la **funzione OpenPerformanceData** restituisce correttamente, il sistema chiama la funzione [**CollectPerformanceData del**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) provider. Le chiamate successive [**a RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) causano la chiamata della **funzione CollectPerformanceData da** parte del sistema.

Al termine della raccolta dei dati sulle prestazioni, il consumer specifica `HKEY_PERFORMANCE_DATA` in una chiamata alla funzione [**RegCloseKey.**](/windows/desktop/api/winreg/nf-winreg-regclosekey) In questo modo il sistema chiama la [**funzione ClosePerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_close_proc) per ogni provider. I provider vengono quindi scaricati.

È possibile che più consumer raccolgono dati sulle prestazioni contemporaneamente. Il sistema chiama [**le funzioni OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) e [**ClosePerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_close_proc) solo una volta ogni volta che la DLL viene caricata o scaricata.

> [!Note]
> Assicurarsi di includere "C" extern nel codice C++ per impedire al compilatore di aggiungere elementi decorativi ai nomi delle funzioni. in caso contrario, il sistema potrebbe non riuscire a trovare le funzioni.

> [!Note]
> Se si verifica un errore durante il caricamento della DLL delle prestazioni, la ricerca delle funzioni o la chiamata delle funzioni, il sistema disabilita il provider per le raccolte successive all'interno dello stesso processo. Inoltre, se ciò si verifica durante l'esecuzione in un processo con  privilegi, il sistema aggiunge un valore **Disabilita** contatori delle prestazioni alla chiave Prestazioni per impedire il caricamento del provider in futuro.

Per altre informazioni sulla scrittura di una DLL delle prestazioni, vedere gli argomenti seguenti:

- [Implementazione della funzione OpenPerformanceData](implementing-openperformancedata.md)
- [Implementazione della funzione CollectPerformanceData](implementing-collectperformancedata.md)
- [Gestione degli errori nella DLL](error-handling-in-the-dll.md)
- [Limitazione dell'accesso alle DLL delle estensioni delle prestazioni](restricting-access-to-performance-extension--dlls.md)
- [Esempi di DLL delle prestazioni](performance-dll-samples.md)
