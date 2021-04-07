---
description: A partire da Windows XP, è possibile creare un assembly privato e renderlo disponibile per un'applicazione specifica.
ms.assetid: 08cebffc-6856-4dac-8600-5e7fecb5c69b
title: Correggere un'applicazione esistente utilizzando un assembly privato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 095c3eefc5f166ad09643a363ec4308d190e6586
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049428"
---
# <a name="fixing-an-existing-application-using-a-private-assembly"></a>Correzione di un'applicazione esistente mediante un assembly privato

A partire da Windows XP, è possibile creare un assembly privato e renderlo disponibile per un'applicazione specifica. Questa funzionalità può essere usata per correggere un'applicazione che diventa incompatibile con un aggiornamento. Un esempio è un'applicazione che diventa incompatibile con la versione più recente di MSVCRT.DLL dopo l'aggiornamento del sistema operativo. In questo caso, non è possibile sostituire la versione del sistema perché MSVCRT.DLL è un file protetto da Windows. Anziché dover riscrivere l'applicazione in modo che funzioni con la nuova versione di MSVCRT, è possibile creare un assembly privato per MSVCRT e installarlo nella cartella dell'applicazione. Si noti che non tutti i componenti condivisi sono un candidato adatto per un assembly side-by-side privato e che alcuni componenti presentano restrizioni di licenza sulla posizione in cui possono essere installati i componenti. Il componente deve soddisfare i criteri per un componente affiancato. Richiedere all'autore del componente se è possibile fornire un assembly adatto.

Il manifesto dell'assembly privato e il manifesto dell'applicazione devono essere installati nella stessa cartella del file eseguibile dell'applicazione. Quando l'applicazione viene eseguita, viene consultato il manifesto dell'applicazione e viene caricata la versione di MSVCRT privata per l'applicazione.

Per questo esempio, l'assembly privato include sia MSVCRT.DLL che MSVCIRT.DLL come nel seguente manifesto dell'assembly:

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity type="win32"
      name="Microsoft.Windows.PrivateCPlusPlusRuntime" 
version="6.0.0.0" 
processorArchitecture="x86"/>
    <file name="msvcrt.dll"/>
    <file name="msvcirt.dll"/>
</assembly>
```

Di seguito è riportato un esempio di un possibile manifesto dell'applicazione.

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0"> 
<assemblyIdentity 
    version="1.0.0.0" 
    processorArchitecture="x86" 
    name="APPLICATION" 
    type="win32" 
/> 
<description>Description of Application</description> 
<dependency> 
    <dependentAssembly> 
       <assemblyIdentity 
           type="win32"
           name="Microsoft.Windows.PrivateCPlusPlusRuntime" 
           version="6.0.0.0" 
           processorArchitecture="x86"/> 
    </dependentAssembly> 
</dependency> 
</assembly>
```

 

 



