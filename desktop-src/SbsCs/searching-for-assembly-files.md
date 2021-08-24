---
description: Ricerca di file di assembly
ms.assetid: 6e6c1104-5cde-4c07-9ee2-d87062675dac
title: Ricerca di file di assembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b55614278d58913c8fb92371e302ffd71fd28b48b7828351d8ce6b37ae0eddc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119884871"
---
# <a name="searching-for-assembly-files"></a>Ricerca di file di assembly

I contesti di attivazione consentono al caricatore di trovare i file di assembly. Quando il caricatore cerca un file da caricare in base al nome, cerca innanzitutto i file con il nome specificato a cui fanno riferimento gli assembly membri del contesto di attivazione attualmente attivo. Anche una chiamata [**a SearchPath**](/windows/desktop/api/processenv/nf-processenv-searchpathw) individua prima questi file. I file con il nome specificato e il contesto di attivazione corrente vengono trovati e caricati prima dei file con il nome nella directory locale o nella variabile di ambiente PATH. Ciò significa che quando si creano manifesti è necessario elencare tutti i file che si prevede di usare con **SearchPath,** [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)o importazioni statiche.

Si noti che questi file non vengono individuati automaticamente quando si usa [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) o altre funzioni che non esequistono i file. Per usare questi file con **CreateFile,** usare [**prima SearchPath**](/windows/desktop/api/processenv/nf-processenv-searchpathw) per trovare il percorso del file isolato e quindi **usare CreateFile** nel percorso restituito.

Questo metodo di ricerca di file consente di mantenere separate le applicazioni isolate perché più file con lo stesso nome possono quindi differire solo in base all'associazione con assembly con numeri di versione diversi. Il sistema operativo può trovare il file corretto da usare durante le operazioni sui file.

Se una DLL viene caricata in questo modo usando [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya), il punto di ingresso della DLL (DllMain) viene chiamato mentre il contesto di attivazione originale viene mantenuto attivo, tranne se la DLL stessa contiene un manifesto in corrispondenza di un determinato ID risorsa (ID RISORSA MANIFESTO ISOLATIONAWARE \_ o \_ \_ 2)

 

 
