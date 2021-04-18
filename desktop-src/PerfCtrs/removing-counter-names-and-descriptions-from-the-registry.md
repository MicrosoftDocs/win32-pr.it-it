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
# <a name="removing-counter-names-and-descriptions-from-the-registry"></a><span data-ttu-id="305ce-103">Rimozione di nomi e descrizioni di contatori dal registro di sistema</span><span class="sxs-lookup"><span data-stu-id="305ce-103">Removing Counter Names and Descriptions from the Registry</span></span>

<span data-ttu-id="305ce-104">Lo strumento **unlodctr** rimuove le voci del registro di sistema create da **lodctr**.</span><span class="sxs-lookup"><span data-stu-id="305ce-104">The **unlodctr** tool removes the registry entries created by **lodctr**.</span></span> <span data-ttu-id="305ce-105">Il nome dell'applicazione passato a **unlodctr** deve corrispondere al [nome della chiave dell'applicazione](creating-the-applications-performance-key.md) creata nella chiave **Services** .</span><span class="sxs-lookup"><span data-stu-id="305ce-105">The application name that you pass to **unlodctr** must match the [name of the application key](creating-the-applications-performance-key.md) that you created under the **Services** key.</span></span> <span data-ttu-id="305ce-106">Per informazioni dettagliate sull'esecuzione di **unlodctr** , vedere Guida e supporto tecnico.</span><span class="sxs-lookup"><span data-stu-id="305ce-106">For details on running **unlodctr** see, Help and Support Center.</span></span>

## <a name="using-unlodctr"></a><span data-ttu-id="305ce-107">Uso di unlodctr</span><span class="sxs-lookup"><span data-stu-id="305ce-107">Using unlodctr</span></span>

<span data-ttu-id="305ce-108">Lo strumento **unlodctr** Cerca il primo e l'ultimo contatore e consente di indicizzare i valori usando i valori del registro di sistema like denominati nella chiave **delle prestazioni** dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="305ce-108">The **unlodctr** tool looks up the first and last counter and help index values using the like named registry values under your application's **Performance** key.</span></span> <span data-ttu-id="305ce-109">Lo strumento **unlodctr** utilizza l'intervallo di valori di indice per rimuovere il testo dai **contatori** e i valori della **Guida** per ogni identificatore di lingua.</span><span class="sxs-lookup"><span data-stu-id="305ce-109">The **unlodctr** tool uses the range of index values to remove the text from **Counters** and **Help** values for each language identifier.</span></span>

<span data-ttu-id="305ce-110">Con i valori di indice, **unlodctr** apporta le modifiche seguenti al registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="305ce-110">Using the index values, **unlodctr** makes the following changes to the registry.</span></span>

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

<span data-ttu-id="305ce-111">Lo strumento **unlodctr** rimuove inoltre i valori del **primo contatore**, dell' **ultimo contatore**, della **prima guida**, dell' **Ultima Guida** e dell' **elenco di oggetti** dalla chiave **delle prestazioni** dell'applicazione che si trova in **HKEY \_ Local \_ computer** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ *Application-Name* \\ **performance**.</span><span class="sxs-lookup"><span data-stu-id="305ce-111">The **unlodctr** tool also removes the **First Counter**, **Last Counter**, **First Help**, **Last Help**, and **Object List** values from the application's **Performance** key located at **HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Services**\\*application-name*\\**Performance**.</span></span>

> [!Note]  
> <span data-ttu-id="305ce-112">La funzione di scaricamento di **unlodctr**, [**UnloadPerfCounterTextStrings**](/windows/desktop/api/Loadperf/nf-loadperf-unloadperfcountertextstringsa), è dichiarata in loadperf. h ed esportata da Loadperf.dll.</span><span class="sxs-lookup"><span data-stu-id="305ce-112">The unloading function of **unlodctr**, [**UnloadPerfCounterTextStrings**](/windows/desktop/api/Loadperf/nf-loadperf-unloadperfcountertextstringsa), is declared in Loadperf.h and exported from Loadperf.dll.</span></span> <span data-ttu-id="305ce-113">In questo modo è possibile chiamare questa funzione direttamente dal programma di disinstallazione.</span><span class="sxs-lookup"><span data-stu-id="305ce-113">This allows you to call this function directly from your uninstall program.</span></span>

 

 

 



