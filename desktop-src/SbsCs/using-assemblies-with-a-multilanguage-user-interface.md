---
description: Se si vuole che gli utenti dell'applicazione o della DLL principale siano in grado di modificare la lingua dell'interfaccia utente, è consigliabile inserire le risorse della lingua in DLL di risorse satellite separate.
ms.assetid: fcadd7e8-cab8-43cb-9c67-af8ebe0e3a5b
title: Uso di assembly con più lingue Interfaccia utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4cd857cca0188b10f02ba44b5631895a9345ce7926cae78376edd554035ccfc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141774"
---
# <a name="using-assemblies-with-a-multilanguage-user-interface"></a>Uso di assembly con più lingue Interfaccia utente

Se si vuole che gli utenti dell'applicazione o della DLL principale siano in grado di modificare la lingua dell'interfaccia utente, è consigliabile inserire le risorse della lingua in DLL di risorse satellite separate. Per altre informazioni sull'uso delle DLL di risorse satellite, vedere [Multilanguage Interfaccia utente (MUI).](/windows/desktop/Intl/multilingual-user-interface)

Ogni DLL satellite contiene le risorse per una lingua diversa. La DLL principale può essere fornita come assembly e ognuna delle DLL satellite può essere fornita come assembly satellite separati. In questo caso, ogni assembly satellite deve avere il proprio manifesto dell'assembly autodescritto. Il manifesto dell'assembly satellite non deve descrivere alcuna dipendenza da altri assembly. Qualsiasi dipendenza di assembly satellite da altri assembly deve essere invece descritta nel manifesto dell'assembly principale.

La [versione MUI (Multilanguage Interfaccia utente)](/windows/desktop/Intl/multilingual-user-interface) di Windows consente agli utenti di specificare la lingua dell'interfaccia utente in base alle proprie preferenze, a condizione che la lingua richiesta sia stata aggiunta al sistema. Un assembly principale può supportare più linguaggi usando più assembly MUI. In questo caso, ogni assembly MUI deve avere un proprio manifesto e tutte le dipendenze da altri assembly devono essere descritte solo nel manifesto dell'assembly principale.

Ad esempio, Proseware.Sample.Pop può essere un assembly side-by-side di base che dipende dall'assembly Proseware.Research.SampleAssembly. Se Proseware.Sample.Pop usa MUI per supportare più lingue, è possibile specificare assembly MUI separati per ogni lingua. Ogni assembly MUI deve avere il proprio manifesto che descrive la DLL della risorsa satellite specifica. I manifesti dell'assembly MUI non devono includere riferimenti alle dipendenze da altri assembly. Il manifesto che descrive l'assembly principale, Proseware.Sample.Pop, deve descrivere la dipendenza di Proseware.Sample.Pop nell'assembly Proseware.Research.SampleAssembly.

Gli attributi **dell'elemento assemblyIdentity** di un assembly satellite sono simili a quelli nel manifesto dell'assembly di base. **L'attributo** name deve essere uguale all'assembly di base con l'aggiunta di "Resources". Ad esempio, se il nome è "Proseware.Tools.SpellCheck.Runtime-Libraries" nell'assembly di base, il nome nell'assembly di risorse sarà "Proseware.Tools.SpellCheck.Runtime-Libraries.Resources". **L'attributo** language deve identificare la lingua dell'assembly di risorse. **L'attributo file** deve includere l'elenco di file che sono DLL di risorse.

Di seguito è riportato un esempio del manifesto per l'assembly di risorse Proseware.Tools.SpellCheck.Runtime-Libraries.

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        type="win32"
        name="Proseware.Tools.SpellCheck.Runtime-Libraries.Resources"
        version="6.0.0.0"
        processorArchitecture="X86"
        language="DE"
        publicKeyToken="0000000000000000"
    />
    <file name="sample.dll"/>
</assembly>
```

L'assembly di base descrive una dipendenza facoltativa dall'assembly di risorse. In questo esempio, se un utente esegue un Windows con le impostazioni locali designate come tedesco, un'applicazione che usa l'assembly Proseware.Tools.SpellCheck visualizza il testo in tedesco.

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity type="win32" 
    name="Proseware.Tools.SpellCheck.Runtime-Libraries"
    version="6.0.0.0" processorArchitecture="x86"
    publicKeyToken="0000000000000000"/>
    <dependency optional="yes">
        <dependentAssembly>
            <assemblyIdentity type="win32" 
                              name="Proseware.Tools.SpellCheck.Runtime-Libraries.Resources" 
                              version="6.0.0.0" 
                              processorArchitecture="x86" 
                              publicKeyToken="0000000000000000" 
                              language="*"
            />
        </dependentAssembly>
    </dependency>
```

 

 
