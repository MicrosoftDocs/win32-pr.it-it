---
description: Se l'applicazione ospita una DLL di terze parti, un'estensione, un plug-in o un pannello di controllo, potrebbe essere necessario abilitare un assembly nell'applicazione&\# 8212; senza abilitare anche questo assembly per i componenti ospitati.
ms.assetid: 832957ca-82fc-4600-b469-512621dde921
title: Abilitazione di un assembly in un'applicazione che ospita una DLL, un'estensione o un pannello di controllo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b04dd19b18c2cdce4783be47333b9afe53dd1ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313307"
---
# <a name="enabling-an-assembly-in-an-application-hosting-a-dll-extension-or-control-panel"></a>Abilitazione di un assembly in un'applicazione che ospita una DLL, un'estensione o un pannello di controllo

Se l'applicazione ospita una DLL di terze parti, un'estensione, un plug-in o un pannello di controllo, è possibile abilitare un assembly nell'applicazione, senza abilitare anche questo assembly per i componenti ospitati. Questo può essere il caso in cui un componente ospitato richiede modifiche al codice per usare l'assembly. Lo sviluppatore dell'applicazione potrebbe non essere in grado di apportare modifiche a questi componenti di terze parti. In questo caso, è necessario seguire la procedura descritta in questa sezione in modo che l'applicazione possa usare l'assembly senza influire sui componenti ospitati.

-   Per abilitare un assembly in un'applicazione senza influire sulle dll, le estensioni, i plug-in o i pannelli di controllo ospitati, un manifesto che descrive la dipendenza dell'applicazione dall'assembly deve essere incluso nell'applicazione come risorsa. I componenti ospitati che non sono abilitati con l'assembly non devono includere manifesti che descrivono questa dipendenza.
-   Per abilitare un assembly in un'applicazione e le relative dll, estensioni, plug-in o pannelli di controllo ospitati, includere i manifesti come risorse nell'applicazione e nei relativi componenti ospitati. I manifesti inclusi nell'applicazione e nei componenti ospitati dovrebbero descrivere una dipendenza dall'assembly. In genere, lo sviluppatore dell'applicazione aggiunge un manifesto all'applicazione e lo sviluppatore di componenti ospitati aggiunge un manifesto alla DLL, all'estensione, al plug-in o al pannello di controllo.

Il metodo seguente può essere usato per aggiungere un manifesto a un'applicazione o a un componente ospitato che è una DLL, un'estensione, un plug-in o un pannello di controllo.

**Per abilitare un assembly in un'applicazione o in un componente ospitato.**

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

2.  Creare una risorsa nell'applicazione o nell'estensione di tipo RT \_ manifest ID 2.

    Ad esempio, se il nome dell'applicazione è YourApp, l'applicazione deve contenere quanto segue:

    ``` syntax
    #define MANIFEST_RESOURCE_ID 2
    MANIFEST_RESOURCE_ID RT_MANIFEST "YourApp.manifest"
    ```

3.  Compilare l'applicazione con il flag di \_ Abilitazione di-DISOLATION \_ o inserire questa istruzione prima dell' \# istruzione include "Windows. h". Nel caso di un'applicazione con più moduli, il flag-DISOLATION \_ Aware \_ Enabled è obbligatorio in tutti i moduli.

    ``` syntax
    #define ISOLATION_AWARE_ENABLED 1
    ```

4.  Eseguire un test per assicurarsi che gli assembly usati dall'applicazione funzionino correttamente nell'applicazione e nel componente ospitato.

Per ulteriori informazioni sull'aggiunta di un assembly alle applicazioni senza estensioni, vedere [Abilitazione di un assembly in un'applicazione senza estensioni](enabling-an-assembly-in-an-application-without-extensions.md).

 

 



