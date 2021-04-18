---
description: Lo strumento unlodctr rimuove le voci del registro di sistema create da lodctr.
ms.assetid: 83c0fb91-857c-40d9-8fb8-8734c1b573c4
title: Rimozione di nomi e descrizioni di contatori dal registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04ea8c0a8efbe9a798f980a061c6cfc65745b89b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312090"
---
# <a name="removing-counter-names-and-descriptions-from-the-registry"></a>Rimozione di nomi e descrizioni di contatori dal registro di sistema

Lo strumento **unlodctr** rimuove le voci del registro di sistema create da **lodctr**. Il nome dell'applicazione passato a **unlodctr** deve corrispondere al [nome della chiave dell'applicazione](creating-the-applications-performance-key.md) creata nella chiave **Services** . Per informazioni dettagliate sull'esecuzione di **unlodctr** , vedere Guida e supporto tecnico.

## <a name="using-unlodctr"></a>Uso di unlodctr

Lo strumento **unlodctr** Cerca il primo e l'ultimo contatore e consente di indicizzare i valori usando i valori del registro di sistema like denominati nella chiave **delle prestazioni** dell'applicazione. Lo strumento **unlodctr** utilizza l'intervallo di valori di indice per rimuovere il testo dai **contatori** e i valori della **Guida** per ogni identificatore di lingua.

Con i valori di indice, **unlodctr** apporta le modifiche seguenti al registro di sistema.

```
HKEY_LOCAL_MACHINE
   \SOFTWARE
      \Microsoft
         \Windows NT
            \CurrentVersion
               \Perflib
                  Last Counter = updated if changed
                  Last Help = updated if changed
                  \009
                     Counters = application text removed
                     Help = application text removed
                  \supported language, other than English
                     Counters = application text removed
                     Help = application text removed
```

Lo strumento **unlodctr** rimuove inoltre i valori del **primo contatore**, dell' **ultimo contatore**, della **prima guida**, dell' **Ultima Guida** e dell' **elenco di oggetti** dalla chiave **delle prestazioni** dell'applicazione che si trova in **HKEY \_ Local \_ computer** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ *Application-Name* \\ **performance**.

> [!Note]  
> La funzione di scaricamento di **unlodctr**, [**UnloadPerfCounterTextStrings**](/windows/desktop/api/Loadperf/nf-loadperf-unloadperfcountertextstringsa), è dichiarata in loadperf. h ed esportata da Loadperf.dll. In questo modo è possibile chiamare questa funzione direttamente dal programma di disinstallazione.

 

 

 



