---
title: Provider di servizi di esempio
description: Provider di servizi di esempio
ms.assetid: bbdeddb5-4ddf-4a61-828c-a9ba7af307ea
keywords:
- Windows Media Gestione dispositivi, esempi
- Gestione dispositivi, esempi
- Windows Media Gestione dispositivi, esempio di provider di servizi
- Gestione dispositivi, esempio di provider di servizi
- provider di servizi, esempi
- esempi, provider di servizi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e8b7e781785944ac1ca390a62303f1149d710d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298272"
---
# <a name="sample-service-provider"></a>Provider di servizi di esempio

Windows Media Gestione dispositivi SDK include un provider di servizi di esempio che è possibile utilizzare. Questo provider di servizi include una classe che segnala ogni disco rigido del computer come se fosse un dispositivo collegato. L'unica applicazione che utilizzerà questo provider di servizi è l'applicazione di esempio; In Esplora risorse non vengono visualizzati i "dispositivi" segnalati da questo provider di servizi. Il provider di servizi di esempio è un oggetto COM basato su ATL. Nei passaggi seguenti viene illustrato come utilizzare il provider di servizi di esempio:

> [!Note]  
> Il provider di servizi di esempio implementa pochissime funzionalità e pertanto non deve essere utilizzato per il test di applicazioni Windows Media Gestione dispositivi. Per testare un'applicazione, usare un provider di servizi completamente implementato.

 

-   L'esempio è stato fornito con un errore di codifica che comporterebbe il malfunzionamento del provider di servizi. Per correggere l'errore, aprire il file MDSPEnumStorage. cpp installato nella cartella < *percorso di installazione di SDK*  > \\ WMFSDK95 \\ WMDM \\ MDSP \\ mshdsp, andare alla riga 185 e modificare la riga seguente:

`wcsncpy(pStg->m_wcsName, m_wcsPath, dwLen);`

A questo scopo:

`wcsncpy(pStg->m_wcsName, m_wcsPath, ARRAYSIZE(pStg->m_wcsName));`

1.  Compilare il file di MsHDSP.dll. Questa operazione può essere eseguita tramite NMAKE o Visual Studio. Per informazioni su come compilare l'applicazione, vedere [compilazione del provider di servizi di esempio mediante NMAKE](compiling-the-sample-service-provider-using-nmake.md) o [compilazione del provider di servizi di esempio mediante Visual Studio](compiling-the-sample-service-provider-using-visual-studio.md) .
2.  Registrare MsHDSP.dll usando Regsvr32. La riga seguente, digitata in una finestra del prompt dei comandi nella stessa cartella MsHDSP.dll, registrerà il provider di servizi di esempio:

    ```C++
    regsvr32 mshdsp.dll
    ```

    

    Per arrestare la rappresentazione di un dispositivo, immettere la riga seguente al prompt dei comandi:

    ```C++
    regsvr32 /u mshdsp.dll
    ```

    

3.  I dispositivi rimovibili rappresentati da questa DLL possono essere visualizzati solo dall'applicazione di esempio fornita con questo SDK. Compilare l'applicazione di esempio usando uno dei metodi descritti in [esempio di applicazione desktop](sample-desktop-application.md).
4.  Per eseguire il debug del provider di servizi con Visual Studio, aprire il provider di servizi in Visual Studio e scegliere **Avvia** dal menu **debug** . Nella finestra di dialogo popup passare all'applicazione di esempio compilata nel passaggio precedente, fare clic su **OK** e il provider di servizi inizierà l'esecuzione in modalità di debug.

    Per eseguire il provider di servizi senza eseguire il debug in Visual Studio, è sufficiente registrare il msdhsp.dll ed eseguire l'applicazione desktop di esempio fornita con l'SDK. L'applicazione desktop di esempio esegue il provider di servizi di esempio automaticamente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Esempi**](samples.md)
</dt> </dl>

 

 




