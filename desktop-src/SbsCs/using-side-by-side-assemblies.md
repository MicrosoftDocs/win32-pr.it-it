---
description: Usare la procedura seguente per sviluppare una nuova applicazione o aggiornare un'applicazione esistente in modo da usare gli assembly side-by-side disponibili da Microsoft o da altri editori di assembly side-by-side.
ms.assetid: da6b6767-8a30-4a76-a030-615067a2cb17
title: Uso di assembly side-by-side
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a60170dc4873f03dfc17769f91106e02b591e0b1db81695d773a35b392a2c7dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141714"
---
# <a name="using-side-by-side-assemblies"></a>Uso di assembly side-by-side

Usare la procedura seguente per sviluppare una nuova applicazione o aggiornare un'applicazione esistente in modo da usare gli assembly [side-by-side](about-side-by-side-assemblies-.md) disponibili da Microsoft o da altri editori di assembly side-by-side. Per un elenco degli assembly side-by-side attualmente forniti da Microsoft, vedere [Assembly side-by-side Microsoft supportati.](supported-microsoft-side-by-side-assemblies.md) Si noti che l'applicazione deve essere eseguita almeno Windows XP per installare gli assembly come assembly side-by-side. Per altre informazioni, vedere [Linee guida per la creazione di assembly side-by-side.](guidelines-for-creating-side-by-side-assemblies.md)

**Per aggiungere un assembly side-by-side a un'applicazione**

1.  Identificare gli assembly side-by-side necessari per l'applicazione. A partire Windows XP, questi assembly side-by-side e i relativi manifesti di assembly vengono installati con il sistema operativo, ma non sono registrati a livello globale.
2.  Usare un editor XML per creare un manifesto [dell'applicazione](application-manifests.md). Vedere il manifesto dell'applicazione di esempio riportato di seguito. Per altre informazioni, vedere [Manifesti dell'applicazione](application-manifests.md) nelle informazioni [di riferimento sui file manifesto.](manifest-files-reference.md)
3.  Immettere i valori degli attributi nel [*sottoelemento DEF-context assemblyIdentity*](d-sbscs-gly.md) del manifesto dell'applicazione che definisce in modo univoco l'applicazione. Per altre informazioni su **def-context assemblyIdentity,** vedere [Manifesti dell'applicazione.](application-manifests.md)
4.  Se l'assembly contiene assembly dipendenti, immettere i valori degli attributi nei sottoelementi [*ref-context assemblyIdentity*](r-sbscs-gly.md) corrispondenti del manifesto dell'applicazione. Per altre informazioni sull'elemento **assemblyIdentity** del contesto REF, vedere [Manifesti dell'applicazione.](application-manifests.md)

    ``` syntax
    <dependentAssembly>
      <assemblyIdentity type="win32"
                        name="Microsoft.Windows.SampleAssembly"
                        version="6.0.0.0" processorArchitecture="x86"
                        publicKeyToken="a5aaf5ba15723d5"/>
    ```

5.  È possibile includere il manifesto dell'applicazione nel file di intestazione eseguibile binario dell'applicazione.

    In questo caso, aggiungere anche la riga seguente al file di intestazione dell'applicazione:

    <dl> CREATEPROCESS \_ MANIFEST RESOURCE ID RT MANIFEST \_ \_ \_ "YourApp.exe.manifest"  
    </dl>

    In alternativa, è possibile inserire un file manifesto separato nella stessa directory del file eseguibile dell'applicazione. Il sistema operativo carica prima il manifesto dal file system e quindi controlla la sezione resource del file eseguibile. La file system ha la precedenza.

6.  [Gli assembly condivisi](/windows/desktop/Msi/shared-assemblies) devono essere installati usando il Windows [Installer](../msi/windows-installer-portal.md) versione 2.0. Creare un pacchetto Windows Installer come descritto in How [Do I Install Win32 Assemblies for Side-by-side Sharing on Windows XP?](../msi/installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)( Come si installano gli assembly Win32 per la condivisione side-by-side in Windows XP? .
7.  [Gli assembly privati](/windows/desktop/Msi/private-assemblies) possono essere installati usando il Windows [Installer](../msi/windows-installer-portal.md) versione 2.0. Creare un pacchetto Windows Installer come descritto in How [Do I Install Win32 Assemblies for the Private Use of an Application on Windows XP?](../msi/installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)( Come installare assembly Win32 per l'uso privato di un'applicazione in Windows XP? . È anche possibile usare qualsiasi altro programma di installazione per copiare un assembly privato e il relativo manifesto nella stessa cartella del file eseguibile dell'applicazione.
8.  Testare l'applicazione per verificare i risultati. Si noti che nel computer di test non deve essere registrato l'assembly side-by-side.
9.  Distribuire l'applicazione o eseguire l'aggiornamento come pacchetto Windows Installer.

## <a name="example-application-manifest"></a>Manifesto dell'applicazione di esempio

Di seguito è riportato un esempio di manifesto dell'applicazione:

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
  <assemblyIdentity type="win32" name="Microsoft.Windows.mysampleapp" version="1.0.0.0" processorArchitecture="x86"/>
  <dependency>
    <dependentAssembly>
      <assemblyIdentity type="win32" name="Microsoft.Windows.SampleAssembly" version="6.0.0.0" processorArchitecture="x86" publicKeyToken="a5aaf5ba15723d5"/>
    </dependentAssembly>
  </dependency>
  <dependency>
    <dependentAssembly>
      <assemblyIdentity type="win32" name="Microsoft.Tools.MyPrivateDll" version="2.5.0.0" processorArchitecture="x86"/>
    </dependentAssembly>
  </dependency>
</assembly>
```

 

 
