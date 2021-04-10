---
description: Creazione del file di risorse della lingua di base
ms.assetid: 770e1f4b-5258-4b6b-afa4-5c19743daaaa
title: Creazione del file di risorse della lingua di base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b96d566625025c105e123e0e2edf9f4f20721274
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058146"
---
# <a name="creating-the-base-language-resource-file"></a>Creazione del file di risorse della lingua di base

Le risorse per gli elementi dell'interfaccia utente sono definite per il linguaggio di base supportato dall'applicazione, ad esempio inglese (Stati Uniti). Un esempio di file di risorse PE Win32 è un file RC, creato con il compilatore RC. Per informazioni dettagliate sulla creazione di file RC, vedere [informazioni sui file di risorse](../menurc/about-resource-files.md).

Se si usa un file RC per le risorse della lingua di base, è possibile usare un file di configurazione delle risorse per una rappresentazione XML dei dati di configurazione delle risorse. Per creare questo file, vedere [preparazione di un file di configurazione delle risorse](preparing-a-resource-configuration-file.md).

È anche possibile usare un file PE non Win32 per definire le risorse della lingua di base. È ad esempio possibile utilizzare un file con estensione XML o txt a questo scopo.

> [!Note]  
> Quando si definiscono le risorse della lingua di base usando un file PE non Win32, non è possibile usare il compilatore RC per la definizione di risorsa. Si definisce invece il proprio formato di risorsa e l'applicazione deve fornire le proprie funzionalità per individuare e caricare le risorse necessarie.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Preparazione delle risorse](preparing-resources.md)
</dt> <dt>

[Preparazione di un file di configurazione delle risorse](preparing-a-resource-configuration-file.md)
</dt> </dl>

 

 
