---
title: Provider di servizi di esempio
description: Provider di servizi di esempio
ms.assetid: bbdeddb5-4ddf-4a61-828c-a9ba7af307ea
keywords:
- Windows Gestione dispositivi multimediali, esempi
- Gestione dispositivi, esempi
- Windows Media Device Manager, esempio di provider di servizi
- Gestione dispositivi, esempio di provider di servizi
- provider di servizi,esempi
- esempi, provider di servizi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8eead5296a1ba3213f291027c0b1e4d50275497ad2ebe5a3feaea994e4a5c8e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004911"
---
# <a name="sample-service-provider"></a>Provider di servizi di esempio

L Windows SDK di Gestione dispositivi multimediali include un provider di servizi di esempio da usare. Questo provider di servizi include una classe che segnala ogni disco rigido nel computer come se fosse un dispositivo collegato. L'unica applicazione che userà questo provider di servizi è l'applicazione di esempio. Windows Explorer non visualizza i "dispositivi" segnalati da questo provider di servizi. L'esempio di provider di servizi è un oggetto COM basato su ATL. La procedura seguente illustra come usare il provider di servizi di esempio:

> [!Note]  
> Il provider di servizi di esempio implementa pochissime funzionalità e quindi non deve essere usato per testare Windows applicazioni di Gestione dispositivi multimediali. Per testare un'applicazione, usare un provider di servizi completamente implementato.

 

-   L'esempio è stato fornito con un errore di codifica che causa un malfunzionamento del provider di servizi. Per correggere l'errore, aprire il file MDSPEnumStorage.cpp installato nella cartella < *SDK percorso* di installazione  > \\ WMFSDK95 \\ WMDM \\ mdsp mshdsp, passare alla riga \\ 185 e modificare la riga seguente:

`wcsncpy(pStg->m_wcsName, m_wcsPath, dwLen);`

A questo scopo:

`wcsncpy(pStg->m_wcsName, m_wcsPath, ARRAYSIZE(pStg->m_wcsName));`

1.  Compilare il file MsHDSP.dll file. È possibile eseguire questa operazione usando NMAKE o Visual Studio. Per informazioni su come compilare l'applicazione, vedere Compilazione del provider di servizi di esempio con [NMAKE](compiling-the-sample-service-provider-using-nmake.md) o Compilazione del provider di servizi di esempio [usando](compiling-the-sample-service-provider-using-visual-studio.md) Visual Studio.
2.  Registrare MsHDSP.dll usando regsvr32. La riga seguente, digitata in una finestra del prompt dei comandi nella stessa cartella MsHDSP.dll, registrerà il provider di servizi di esempio:

    ```C++
    regsvr32 mshdsp.dll
    ```

    

    Per arrestare la rappresentazione di un dispositivo, immettere la riga seguente al prompt dei comandi:

    ```C++
    regsvr32 /u mshdsp.dll
    ```

    

3.  I dispositivi rimovibili rappresentati da questa DLL possono essere visti solo dall'applicazione di esempio fornita con questo SDK. Compilare l'applicazione di esempio usando uno dei metodi descritti in [Applicazione desktop di esempio](sample-desktop-application.md).
4.  Per eseguire il debug del provider di Visual Studio, aprire il provider di servizi in Visual Studio e scegliere **Avvia** dal menu **Debug.** Nella finestra di dialogo popup passare all'applicazione di esempio compilata nel passaggio precedente e fare clic su **OK** e il provider di servizi inizierà l'esecuzione in modalità di debug.

    Per eseguire il provider di servizi senza eseguire il debug in Visual Studio, è sufficiente registrare il msdhsp.dll ed eseguire l'applicazione desktop di esempio fornita con l'SDK. L'applicazione desktop di esempio esegue automaticamente il provider di servizi di esempio.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Esempi**](samples.md)
</dt> </dl>

 

 




