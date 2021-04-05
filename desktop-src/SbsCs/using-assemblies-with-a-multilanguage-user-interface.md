---
description: Se si vuole che gli utenti dell'applicazione, o DLL principale, siano in grado di modificare la lingua dell'interfaccia utente, è consigliabile inserire le risorse di lingua in DLL separate di risorse satellite.
ms.assetid: fcadd7e8-cab8-43cb-9c67-af8ebe0e3a5b
title: Utilizzo di assembly con un'interfaccia utente multilingue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77f501f40715dc2335f02c044aa48ada9741411d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750946"
---
# <a name="using-assemblies-with-a-multilanguage-user-interface"></a>Utilizzo di assembly con un'interfaccia utente multilingue

Se si vuole che gli utenti dell'applicazione, o DLL principale, siano in grado di modificare la lingua dell'interfaccia utente, è consigliabile inserire le risorse di lingua in DLL separate di risorse satellite. Per altre informazioni sull'uso delle DLL di risorse satellite, vedere [interfaccia utente multilingue (MUI)](/windows/desktop/Intl/multilingual-user-interface).

Ogni DLL satellite contiene le risorse per un linguaggio diverso. La DLL di base può essere fornita come assembly e ognuna delle DLL satellite può essere fornita come assembly satellite distinti. In questo caso, ogni assembly satellite deve avere il proprio manifesto di assembly autodescrittivo. Il manifesto dell'assembly satellite non deve descrivere alcuna dipendenza da altri assembly. Tutte le dipendenze degli assembly satellite negli altri assembly devono invece essere descritte nel manifesto dell'assembly principale.

La versione [MUI (Multilingual User Interface)](/windows/desktop/Intl/multilingual-user-interface) di Windows consente agli utenti di specificare la lingua dell'interfaccia utente in base alle proprie preferenze, purché al sistema sia stata aggiunta la lingua richiesta. Un assembly di base può supportare più lingue utilizzando più assembly MUI. In questo caso, ogni assembly MUI deve avere il proprio manifesto e tutte le dipendenze da altri assembly devono essere descritte solo nel manifesto dell'assembly principale.

Ad esempio, proseware. Sample. pop può essere un assembly side-by-side di base che dipende dall'assembly proseware. Research. SampleAssembly. Se proseware. Sample. pop USA MUI per supportare più lingue, è possibile fornire assembly MUI distinti per ogni lingua. Ogni assembly MUI deve avere un proprio manifesto che descrive questa specifica DLL di risorse satellite. I manifesti dell'assembly MUI non devono includere riferimenti alle dipendenze da altri assembly. Il manifesto che descrive l'assembly principale, proseware. Sample. pop, dovrebbe descrivere la dipendenza di proseware. Sample. pop nell'assembly proseware. Research. SampleAssembly.

Gli attributi dell'elemento **assemblyIdentity** di un assembly satellite sono simili a quelli del manifesto dell'assembly di base. L'attributo **Name** deve corrispondere all'assembly di base con l'aggiunta di "Resources". Ad esempio, se il nome è "proseware. Tools. SpellCheck. Runtime-Libraries" nell'assembly di base, il nome nell'assembly di risorse sarà "proseware. Tools. SpellCheck. Runtime-Libraries. resources". L'attributo **Language** dovrebbe identificare la lingua dell'assembly di risorse. L'attributo **file** deve includere l'elenco dei file che sono dll di risorse.

Di seguito è riportato un esempio del manifesto per l'assembly di risorse proseware. Tools. SpellCheck. Runtime-Libraries.

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

L'assembly di base descrive una dipendenza facoltativa dall'assembly di risorse. In questo esempio, se un utente esegue Windows con le impostazioni locali indicate come tedesco, un'applicazione che utilizza l'assembly proseware. Tools. SpellCheck visualizzerà il testo in tedesco.

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

 

 
