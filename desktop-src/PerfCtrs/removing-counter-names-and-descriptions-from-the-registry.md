---
description: Lo strumento unlodctr rimuove le voci del Registro di sistema create da lodctr.
ms.assetid: 83c0fb91-857c-40d9-8fb8-8734c1b573c4
title: Rimozione di nomi e descrizioni dei contatori dal Registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c086520f1fb261a0b9850c03f2aee28065a03ee514df277fbf1cae602deed6a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962351"
---
# <a name="removing-counter-names-and-descriptions-from-the-registry"></a>Rimozione di nomi e descrizioni dei contatori dal Registro di sistema

Lo **strumento unlodctr** rimuove le voci del Registro di sistema create da **lodctr**. Il nome dell'applicazione passato **a unlodctr** deve corrispondere al nome della chiave dell'applicazione creata nella **chiave Services.** [](creating-the-applications-performance-key.md) Per informazioni dettagliate **sull'esecuzione di unlodctr,** vedere Guida e supporto tecnico.

## <a name="using-unlodctr"></a>Uso di unlodctr

Lo **strumento unlodctr** cerca il primo e l'ultimo contatore e consente di indicizzare i valori usando i valori del Registro di sistema denominati come nella chiave **Performance** dell'applicazione. Lo **strumento unlodctr** usa l'intervallo di valori di indice per rimuovere il testo dai **valori di Contatori** e **Guida** per ogni identificatore di lingua.

Usando i valori di indice, **unlodctr** apporta le modifiche seguenti al Registro di sistema.

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

Lo strumento **unlodctr** rimuove anche i valori First **Counter**, Last **Counter**, First  **Help**, **Last Help** e **Object List** dalla chiave performance dell'applicazione che si trova in **HKEY \_ LOCAL \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Services** \\ *application-name* \\ **Performance**.

> [!Note]  
> La funzione di scaricamento **di unlodctr**, [**UnloadPerfCounterTextStrings**](/windows/desktop/api/Loadperf/nf-loadperf-unloadperfcountertextstringsa)è dichiarata in Loadperf.h ed esportata da Loadperf.dll. In questo modo è possibile chiamare questa funzione direttamente dal programma di disinstallazione.

 

 

 



