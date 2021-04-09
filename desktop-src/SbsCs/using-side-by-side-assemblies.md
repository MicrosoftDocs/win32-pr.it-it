---
description: Usare la procedura seguente per sviluppare una nuova applicazione o aggiornare un'applicazione esistente per usare gli assembly affiancati disponibili da Microsoft o da altri autori affiancati di assembly.
ms.assetid: da6b6767-8a30-4a76-a030-615067a2cb17
title: Uso di assembly affiancati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1992562a0868918de2901a7ca88033784af6ef1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878974"
---
# <a name="using-side-by-side-assemblies"></a>Uso di assembly affiancati

Usare la procedura seguente per sviluppare una nuova applicazione o aggiornare un'applicazione esistente per usare gli [assembly affiancati](about-side-by-side-assemblies-.md) disponibili da Microsoft o da altri autori affiancati di assembly. Per un elenco degli assembly affiancati attualmente forniti da Microsoft, vedere assembly affiancati di [Microsoft supportati](supported-microsoft-side-by-side-assemblies.md). Si noti che l'applicazione deve essere eseguita in almeno Windows XP per installare gli assembly come assembly side-by-side. Per ulteriori informazioni, vedere [linee guida per la creazione di assembly affiancati](guidelines-for-creating-side-by-side-assemblies.md).

**Per aggiungere un assembly affiancato a un'applicazione**

1.  Identificare gli assembly affiancati richiesti dall'applicazione. A partire da Windows XP, questi assembly affiancati e i relativi manifesti di assembly vengono installati con il sistema operativo, ma non sono registrati a livello globale.
2.  Utilizzare un editor XML per creare un [manifesto dell'applicazione](application-manifests.md). Vedere il manifesto dell'applicazione di esempio di seguito. Per ulteriori informazioni, vedere [manifesti dell'applicazione](application-manifests.md) nel [riferimento ai file manifesto](manifest-files-reference.md).
3.  Immettere i valori degli attributi nel sottoelemento [*assemblyIdentity del contesto def*](d-sbscs-gly.md) del manifesto dell'applicazione che definisce in modo univoco l'applicazione. Per ulteriori informazioni sul contesto di definizione di **assemblyIdentity**, vedere [manifesti dell'applicazione](application-manifests.md).
4.  Se l'assembly contiene assembly dipendenti, immettere i valori degli attributi nei sottoelementi [*assemblyIdentity del contesto Ref*](r-sbscs-gly.md) corrispondenti del manifesto dell'applicazione. Per ulteriori informazioni sul contesto di riferimento **assemblyIdentity**, vedere [manifesti dell'applicazione](application-manifests.md).

    ``` syntax
    <dependentAssembly>
      <assemblyIdentity type="win32"
                        name="Microsoft.Windows.SampleAssembly"
                        version="6.0.0.0" processorArchitecture="x86"
                        publicKeyToken="a5aaf5ba15723d5"/>
    ```

5.  È possibile includere il manifesto dell'applicazione nel file di intestazione eseguibile binario dell'applicazione.

    In questo caso, aggiungere anche la riga seguente al file di intestazione dell'applicazione:

    <dl> \_ \_ \_ \_ Manifesto "YourApp.exe. manifest" dell'ID risorsa manifesto di CreateProcess  
    </dl>

    In alternativa, è possibile inserire un file manifesto separato nella stessa directory del file eseguibile dell'applicazione. Il sistema operativo carica il manifesto dal file system prima, quindi controlla la sezione delle risorse del file eseguibile. La versione del file system ha la precedenza.

6.  Gli [assembly condivisi](/windows/desktop/Msi/shared-assemblies) devono essere installati usando la versione di [Windows Installer](../msi/windows-installer-portal.md) 2,0. Creare un pacchetto di Windows Installer come descritto in [come installare gli assembly Win32 per la condivisione side-by-side in Windows XP](../msi/installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md).
7.  Gli [assembly privati](/windows/desktop/Msi/private-assemblies) possono essere installati usando la versione di [Windows Installer](../msi/windows-installer-portal.md) 2,0. Creare un pacchetto di Windows Installer come descritto in [come installare gli assembly Win32 per l'utilizzo privato di un'applicazione in Windows XP](../msi/installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md). È anche possibile usare qualsiasi altro programma di installazione per copiare un assembly privato e il relativo manifesto nella stessa cartella del file eseguibile dell'applicazione.
8.  Testare l'applicazione per verificare i risultati. Si noti che il computer di test non deve avere l'assembly affiancato registrato.
9.  Distribuire l'applicazione o aggiornare come pacchetto di Windows Installer.

## <a name="example-application-manifest"></a>Manifesto dell'applicazione di esempio

Di seguito è riportato un esempio di un manifesto dell'applicazione:

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

 

 
