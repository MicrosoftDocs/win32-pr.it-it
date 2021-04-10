---
description: In Direct3D 9 Direct3D consentirà al driver di restituire i codici di errore, ad esempio E \_ OutOfMemory, D3DERR \_ OUTOFVIDEOMEMORY e D3DERR UNSUPPORTEDCOLORARG, in \_ modo che un'applicazione sia in grado di rispondere.
ms.assetid: 483fdb03-e453-4a1b-bd8e-294e9e9a20c2
title: Errori interni del driver (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c81b0ee8ba50edb3c14fbd9a22c9fa9dc93aab8f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124761"
---
# <a name="driver-internal-errors-direct3d-9"></a>Errori interni del driver (Direct3D 9)

In Direct3D 9 Direct3D consentirà al driver di restituire i codici di errore, ad esempio E \_ OutOfMemory, D3DERR \_ OUTOFVIDEOMEMORY e D3DERR UNSUPPORTEDCOLORARG, in \_ modo che un'applicazione sia in grado di rispondere. Tuttavia, talvolta le chiamate API che hanno generato questi tipi restituiti vengono caricate in un buffer dei comandi e vengono inserite in batch per essere inviate alla GPU (vedere [controllo delle ottimizzazioni di runtime e driver](accurately-profiling-direct3d-api-calls.md)). In questo caso, gli errori non possono essere inoltrati all'applicazione quando è necessario eseguire un'azione, quindi il codice di errore viene utilizzato dal runtime e viene effettuata una nota sull'oggetto dispositivo. Successivamente, quando l'applicazione richiama [**IDirect3DDevice9::P**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)reinviate, **IDirect3DDevice9::P** reinviate restituirà D3DERR \_ DRIVERINTERNALERROR. Questo è il motivo per cui l'approccio migliore per un'applicazione da eseguire quando si riceve un DRIVERINTERNALERROR di D3DERR \_ da **IDirect3DDevice9::P inviato** il rimandamento è quello di eliminare e ricreare il dispositivo.

Se si vuole provare a eseguire il debug ulteriormente, di seguito sono riportati alcuni suggerimenti per provare a determinare quale chiamata API genera l'errore:

-   Poiché l'elenco dei possibili valori restituiti non è completo, è possibile provare a individuare la chiamata che ha avuto esito negativo circondando ogni chiamata all'API come la seguente:

    ```
    TRACE ( "Calling DrawPrimitive" );
    d3ddev->DrawPrim(...);
    TRACE ( "done\n" );
    ```

    

    Il flusso di debug dell'output dovrebbe quindi mostrare la chiamata che causa il problema.

-   Inoltre, a scopo di debug, provare a chiamare [**IDirect3DDevice9:: ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice) immediatamente prima di ogni [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) per verificare se esiste un ulteriore problema con il driver di dispositivo (operazione non supportata, combinazione inutilizzabile di formati di trama e così via).

    > [!Note]  
    > [**IDirect3DDevice9:: ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice) deve essere usato con cautela e con moderazione a causa della quantità di lavoro di convalida che il driver deve eseguire per restituire una risposta.

     

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Suggerimenti per la programmazione](programming-tips.md)
</dt> </dl>

 

 
