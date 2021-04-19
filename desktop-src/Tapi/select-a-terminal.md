---
description: Nell'esempio di codice seguente viene illustrato come selezionare terminali sui flussi associati a una chiamata.
ms.assetid: ff43e81c-ff39-466d-870a-54b75c2938a4
title: Selezionare un terminale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac3d195e021f5937c733f3d7a0efce0cfee5eba9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319860"
---
# <a name="select-a-terminal"></a>Selezionare un terminale

Nell'esempio di codice seguente viene illustrato come selezionare terminali sui flussi associati a una chiamata.

Prima di usare questo esempio di codice, è necessario eseguire le operazioni in [Initialize TAPI](initialize-tapi.md) e [selezionare un indirizzo](select-an-address.md).

Questo esempio richiede inoltre che l'applicazione disponga già di un puntatore all'interfaccia [**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) di una chiamata in ingresso o in uscita. Per esempi di codice su come ottenere questo puntatore, vedere [effettuare una chiamata](make-a-call.md) o [ricevere una chiamata](receive-a-call.md) .

> [!Note]  
> Questo esempio non include il controllo degli errori e le versioni appropriate per il codice di produzione.

 

``` syntax
// pAddress is an ITAddress interface pointer.
// pBasicCall is an ITBasicCallControl interface pointer.

// Get the ITStreamControl interface.
ITStreamControl * pStreamControl;
HRESULT hr = pBasicCall->QueryInterface(
        IID_ITStreamControl,
        (void **) &pStreamControl
        );
// If ( hr != S_OK ) process the error here. 

// Enumerate the streams and select 
// terminals onto them.
IEnumStream * pEnumStreams;
ITStream    * pStream;
hr = pStreamControl->EnumerateStreams(&pEnumStreams);
// If ( hr != S_OK ) process the error here. 

while ( S_OK == pEnumStreams->Next(1, &pStream, NULL) )
{
    // Get the media type and direction of this stream.
    long                lMediaType;
    TERMINAL_DIRECTION  dir;
    hr = pStream->get_MediaType( &lMediaType );
    // If ( hr != S_OK ) process the error here. 
    hr = pStream->get_Direction( &dir );
    // If ( hr != S_OK ) process the error here. 

    // Create the default terminal for this media type and direction.
    //   If lMediaType == TAPIMEDIATYPE_VIDEO and
    //   dir == TD_RENDER, a dynamic video render terminal
    //   is required. Please see Incoming.cpp in 
    //   the samples section of the SDK. 
    // For all other terminals, get the default static terminal.
    ITTerminal * pTerminal;
    ITTerminalSupport * pTerminalSupport;
    hr = pAddress->QueryInterface( 
            IID_ITTerminalSupport, 
            (void **)&pTerminalSupport
         );
    // If ( hr != S_OK ) process the error here. 
    hr = pTerminalSupport->GetDefaultStaticTerminal(
            lMediaType,
            dir,
            pTerminal
         );
    // If ( hr != S_OK ) process the error here. 
    // Select the terminal on the stream.
    hr = pStream->SelectTerminal(pTerminal);
    // If ( hr != S_OK ) process the error here. 
}
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ITAddress**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress)
</dt> <dt>

[**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol)
</dt> <dt>

[**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)
</dt> <dt>

[**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> <dt>

[**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream)
</dt> <dt>

[**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)
</dt> <dt>

[**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)
</dt> </dl>

 

 
