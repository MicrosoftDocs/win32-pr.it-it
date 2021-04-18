---
description: Uso di Windows Media con i servizi di modifica DirectShow
ms.assetid: 26a88197-ec80-4443-9d50-e11df40dd1eb
title: Uso di Windows Media con i servizi di modifica DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18fbfe715495834217b695f887305f1ecb21cb6f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320455"
---
# <a name="using-windows-media-with-directshow-editing-services"></a>Uso di Windows Media con i servizi di modifica DirectShow

\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]

In questa sezione viene descritto come utilizzare il contenuto basato su Windows Media in un'applicazione di [servizi di modifica DirectShow](directshow-editing-services.md) (des). Esistono due scenari principali:

-   Clip di origine. Un progetto DES può contenere clip audio e video da file di Windows Media.
-   Formato di destinazione. Windows Media è un formato ideale per l'output finale di un progetto di modifica video.

Per lavorare con i file di Windows Media, l'applicazione deve fornire un certificato software, detto anche chiave. Questa operazione viene eseguita implementando un oggetto provider di chiavi. Il provider di chiavi è un oggetto COM che espone l'interfaccia **IServiceProvider** . Per informazioni sull'implementazione del provider di chiavi, vedere [sblocco di Windows Media Format SDK](unlocking-the-windows-media-format-sdk.md).

Per usare DES con i file di Windows Media, gli oggetti DES seguenti richiedono la chiave software:

-   Motore di rendering, per l'anteprima o la scrittura di file.
-   Oggetto MediaDet, per ottenere i frame video o i tipi di supporto da file ASF.
-   \[! Importante\]  
    > Non usare il motore di rendering intelligente per leggere o scrivere file di Windows Media. Usare sempre il motore di rendering di base (CLSID \_ RenderEngine).

     

Per assegnare a un oggetto la chiave software, eseguire una query sull'oggetto per l'interfaccia **IObjectWithSite** e chiamare **IObjectWithSite:: SESITE** con un puntatore al provider di chiavi. Il codice seguente, ad esempio, fornisce la chiave software al motore di rendering:


```C++
// Create your key provider, using an application-defined function:
IServiceProvider *pKey;
hr = MyCreateKeyProviderFunction(&pKey);  

// Query the Render Engine for IObjectWithSite.
IObjectWithSite *pOWS;
hr = pRenderEngine->QueryInterface(__uuidof(IObjectWithSite), 
    reinterpret_cast<void**>(&pOWS));
if (SUCCEEDED(hr))
{
    // Give it your key provider.
    hr = pOWS->SetSite(pKey);
    pOWS->Release();
}
pKey->Release();
```



Per usare le clip di origine di Windows Media in un progetto DES, è sufficiente chiamare **IObjectWithSite:: SESITE** nel motore di rendering con un puntatore al provider di chiavi.

Per informazioni sulla scrittura di file Windows Media, vedere [scrittura di un file Windows Media in des](writing-a-windows-media-file-in-des.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dei servizi di modifica DirectShow](using-directshow-editing-services.md)
</dt> </dl>

 

 



