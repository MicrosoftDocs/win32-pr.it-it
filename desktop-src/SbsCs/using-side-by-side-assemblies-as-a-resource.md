---
description: Uso di assembly side-by-side come risorsa
ms.assetid: f7963d37-93c4-49d6-af7d-fc692f632894
title: Uso di assembly side-by-side come risorsa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b97265b48f4ce8f3c87a87ec4ca9ea2b8252819
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966596"
---
# <a name="using-side-by-side-assemblies-as-a-resource"></a>Uso di assembly side-by-side come risorsa

È possibile aggiungere un manifesto a un'applicazione come risorsa nel file di intestazione eseguibile binario dell'applicazione. Il valore dell'ID di \_ risorsa del manifesto \_ determina il modo in cui le dipendenze dell'assembly affiancato descritte nel manifesto vengono usate dal caricatore.

Se si imposta l' \_ ID di risorsa del manifesto \_ su 1, il caricatore usa le dipendenze di assembly affiancate specificate nel manifesto come impostazione predefinita del processo. Anche tutti i plug-in usano questo processo predefinito.

La tabella seguente riepiloga il modo in cui il caricatore usa il manifesto per i diversi valori dell'ID di risorsa di manifesto \_ \_ quando l'applicazione viene compilata con il flag-DISOLATION \_ Aware \_ Enabled. Si noti che i valori 1-16 sono riservati per l'utilizzo da parte di Windows XP. Uno sviluppatore può usare altri valori se vogliono gestire i contesti di attivazione usando le funzioni descritte nel riferimento al [contesto di attivazione](activation-context-reference.md).



| Valore dell' \_ ID risorsa \_ manifesto | Il manifesto specifica l'impostazione predefinita del processo? | Usare per le importazioni statiche? | Usare per un file EXE? | Usare per una DLL? | Usa la versione side-by-side degli assembly se compilata con-DISOLATION \_ Aware \_ abilitato? |
|---------------------------------|-----------------------------------------|-------------------------|-----------------|----------------|---------------------------------------------------------------------------------------|
| 1                               | Sì                                     | Sì                     | Sì             | No             | Sì                                                                                   |
| 2                               | No                                      | Sì                     | Sì             | Sì            | Sì                                                                                   |
| 3                               | No                                      | No                      | Sì             | Sì            | Sì                                                                                   |



 

\_ \_ È consigliabile usare l'ID di risorsa del manifesto 1 per le applicazioni che non ospitano plug-in. Usare \_ \_ l'ID di risorsa del manifesto 1 quando tutte le parti dell'applicazione devono usare la versione dell'assembly affiancato specificato nel manifesto. Per altre informazioni, vedere [Abilitazione di un assembly in un'applicazione senza estensioni](enabling-an-assembly-in-an-application-without-extensions.md).

\_ \_ Per le applicazioni che ospitano controlli o plug-in di terze parti, è necessario usare l'ID di risorsa del manifesto 2. In questo caso, il manifesto influiscono su tutti gli assembly affiancati caricati dal caricamento statico, le chiamate a DllMain e le chiamate reindirizzate da-DISOLATION \_ Aware \_ Enabled. Per ulteriori informazioni, vedere [Abilitazione di un assembly in un'applicazione che ospita una dll, un'estensione o un pannello di controllo](enabling-an-assembly-in-an-application-hosting-a-dll-extension-or-control-panel.md).

L' \_ ID di risorsa del manifesto \_ 3 deve essere usato per il reindirizzamento delle chiamate da-DISOLATION \_ Aware \_ only abilitato. Il caricamento da altri metodi non è interessato.

 

 



