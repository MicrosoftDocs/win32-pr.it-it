---
description: Un provider è una DLL di prestazioni che fornisce ai clienti i dati del contatore.
ms.assetid: bbb777fe-b97e-4777-b797-ec8525065610
title: Creazione di una DLL di estensione prestazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d397f1581454aca1b25c447b35f250eefd215f57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881769"
---
# <a name="creating-a-performance-extension-dll"></a>Creazione di una DLL di estensione prestazioni

> [!IMPORTANT]
> A causa di limitazioni significative in merito a prestazioni e affidabilità, il metodo per fornire i dati dei contatori delle prestazioni descritti in questo argomento può essere modificato o non disponibile in futuro. Microsoft consiglia invece di usare il metodo descritto in [fornire i dati del contatore usando la versione 2,0](providing-counter-data-using-version-2-0.md) per creare nuovi contatori delle prestazioni e migrare i contatori delle prestazioni esistenti per usare anche tale metodo.

Un [provider v1](providing-counter-data.md) utilizza una DLL di prestazioni che fornisce ai clienti dati del contatore. La DLL di prestazioni deve esportare le funzioni [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)), [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc)e [**ClosePerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_close_proc) . In genere, si usa un file di definizione del modulo (con estensione def) per esportare le funzioni dalla DLL. Il sistema chiama queste funzioni quando un consumer esegue una query dei dati sulle prestazioni.

La prima volta che un consumer chiama [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa)o se il consumer usa la funzione [**RegOpenKey**](/windows/desktop/api/winreg/nf-winreg-regopenkeya) o [**RegConnectRegistry**](/windows/desktop/api/winreg/nf-winreg-regconnectregistrya) per aprire `HKEY_PERFORMANCE_DATA` , il sistema chiama la funzione [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) per ogni provider [registrato](adding-performance-counters.md) nel computer. L'eccezione è rappresentata dal provider che specifica l'elenco di oggetti supportati nella `[objects]` sezione di. File INI. In questo caso, il sistema chiama il provider solo se uno degli oggetti sottoposti a query corrisponde a un oggetto dell'elenco.

La funzione [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) offre a ogni provider la possibilità di inizializzare le strutture dei dati sulle prestazioni. Quindi, se la funzione **OpenPerformanceData** restituisce correttamente, il sistema chiama la funzione [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) del provider. Le chiamate successive a [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) provocano la chiamata della funzione **CollectPerformanceData** da parte del sistema.

Al termine della raccolta dei dati sulle prestazioni, il consumer specifica `HKEY_PERFORMANCE_DATA` in una chiamata alla funzione [**RegCloseKey**](/windows/desktop/api/winreg/nf-winreg-regclosekey) . In questo modo il sistema chiama la funzione [**ClosePerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_close_proc) per ogni provider. I provider vengono quindi scaricati.

È possibile che più consumer raccolgano i dati sulle prestazioni nello stesso momento. Il sistema chiama le funzioni [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) e [**ClosePerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_close_proc) solo una volta ogni volta che la dll viene caricata o scaricata.

> [!Note]
> Assicurarsi di includere extern "C" nel codice C++ per impedire al compilatore di aggiungere decorazioni ai nomi di funzione; in caso contrario, il sistema potrebbe non riuscire a trovare le funzioni.

> [!Note]
> Se si verifica un errore durante il caricamento della DLL di prestazioni, la ricerca delle funzioni o la chiamata delle funzioni, il sistema Disabilita il provider per le raccolte successive nello stesso processo. Inoltre, se questa situazione si verifica durante l'esecuzione in un processo con privilegi, il sistema aggiunge un valore **Disabilita contatori delle prestazioni** alla chiave **prestazioni** per impedire che il provider venga caricato in futuro.

Per ulteriori informazioni sulla scrittura di una DLL di prestazioni, vedere gli argomenti seguenti:

- [Implementazione della funzione OpenPerformanceData](implementing-openperformancedata.md)
- [Implementazione della funzione CollectPerformanceData](implementing-collectperformancedata.md)
- [Gestione degli errori nella DLL](error-handling-in-the-dll.md)
- [Limitazione dell'accesso alle DLL dell'estensione per le prestazioni](restricting-access-to-performance-extension--dlls.md)
- [Esempi di DLL di prestazioni](performance-dll-samples.md)
