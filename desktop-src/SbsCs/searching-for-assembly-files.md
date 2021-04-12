---
description: Ricerca di file di assembly
ms.assetid: 6e6c1104-5cde-4c07-9ee2-d87062675dac
title: Ricerca di file di assembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7be73b162ea41fd9eeb0a042a1fc2e202b8115
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233295"
---
# <a name="searching-for-assembly-files"></a>Ricerca di file di assembly

I contesti di attivazione possono aiutare il caricatore a trovare i file di assembly. Quando il caricatore cerca un file da caricare in base al nome, cerca innanzitutto i file con il nome specificato a cui fanno riferimento gli assembly membri del contesto di attivazione attualmente attivo. Una chiamata a [**SearchPath**](/windows/desktop/api/processenv/nf-processenv-searchpathw) individua anche questi file per primi. I file con il nome specificato e il contesto di attivazione corrente vengono trovati e caricati prima dei file con il nome nella directory locale o nella variabile di ambiente PATH. Ciò significa che quando si creano manifesti è necessario elencare tutti i file che si prevede di usare con **SearchPath**, [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)o le importazioni statiche.

Si noti che questi file non vengono individuati automaticamente quando si usa [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) o altre funzioni che non eseguono la ricerca di file. Per usare questi file con **CreateFile**, usare prima [**SearchPath**](/windows/desktop/api/processenv/nf-processenv-searchpathw) per trovare il percorso del file isolato, quindi usare **CreateFile** sul percorso restituito.

Questo metodo di ricerca di file consente di rendere separate le applicazioni isolate in quanto più file con lo stesso nome possono quindi differire solo per la loro associazione con assembly con numeri di versione diversi. Il sistema operativo è in grado di trovare il file corretto da utilizzare durante le operazioni sui file.

Se una DLL viene caricata in questo modo utilizzando [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya), il punto di ingresso della dll (DllMain) viene chiamato mentre il contesto di attivazione originale viene mantenuto attivo, tranne nel caso in cui la dll contenga un manifesto a un determinato ID di risorsa ( \_ ID di risorsa del manifesto ISOLATIONAWARE \_ \_ o 2)

 

 
