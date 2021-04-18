---
description: Se l'applicazione non ospita una DLL, un'estensione, un plug-in o un pannello di controllo, è possibile usare il metodo descritto in questa sezione per abilitare un assembly per l'applicazione.
ms.assetid: d043ec1b-ac31-45fb-9232-eec42aef4ac3
title: Abilitazione di un assembly in un'applicazione senza estensioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a1bbcfe510f5a3cdbce323f01cb9342ce236c7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318641"
---
# <a name="enabling-an-assembly-in-an-application-without-extensions"></a>Abilitazione di un assembly in un'applicazione senza estensioni

Se l'applicazione non ospita una DLL, un'estensione, un plug-in o un pannello di controllo, è possibile usare il metodo descritto in questa sezione per abilitare un assembly per l'applicazione. Per ulteriori informazioni sull'aggiunta di un assembly alle applicazioni con estensioni, vedere [Abilitazione di un assembly in un'applicazione che ospita una dll, un'estensione o un pannello di controllo](enabling-an-assembly-in-an-application-hosting-a-dll-extension-or-control-panel.md).

**Per abilitare un assembly in un'applicazione senza componenti ospitati**

1.  Creare un manifesto che descriva la dipendenza dell'applicazione o dell'estensione nell'assembly.

    È ad esempio possibile creare il manifesto per "YourApplication" copiando il manifesto di esempio seguente e sostituendo i valori corretti per **assemblyIdentity**, **processorArchitecture** e **Description**. Impostare il valore di **processorArchitecture** su x86 se si compila su una piattaforma a 32 bit e su ia64 se si compila su una piattaforma a 64 bit. L'elemento **Description** contiene una descrizione dell'opzione dell'applicazione. Per ulteriori informazioni sul formato del manifesto, vedere [manifesti dell'applicazione](application-manifests.md).

    ``` syntax
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        version="1.0.0.0"
        processorArchitecture="x86"
        name="YourCompanyName.YourDivision.YourApp"
        type="win32"
    />
    <description>Your app description here</description>
    <dependency>
        <dependentAssembly>
            <assemblyIdentity
                type="win32"
                name="Proseware.Research.SampleAssembly"
                version="6.0.0.0"
                processorArchitecture="X86"
                publicKeyToken="0000000000000000"
                language="*"
            />
        </dependentAssembly>
    </dependency>
    </assembly>
    ```

2.  Aggiungere il manifesto all'applicazione come risorsa nel file di intestazione eseguibile binario dell'applicazione. Non è consigliabile aggiungere il manifesto all'applicazione come file manifesto esterno.

    Per aggiungere il manifesto come risorsa, creare una risorsa nell'applicazione di tipo RT \_ manifest ID 1. Ad esempio, se il nome dell'applicazione è YourApp, il file di intestazione dell'applicazione deve contenere quanto segue:

    ``` syntax
    #define MANIFEST_RESOURCE_ID 1
    MANIFEST_RESOURCE_ID RT_MANIFEST "YourApp.manifest"
    ```

    Se invece si aggiunge il manifesto come file manifesto esterno, assicurarsi che l'installazione copi il file manifesto nella cartella contenente il file eseguibile dell'applicazione.

3.  Eseguire un test per assicurarsi che gli assembly usati dall'applicazione funzionino correttamente nell'applicazione.

 

 



