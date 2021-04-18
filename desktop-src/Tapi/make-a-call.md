---
description: Nell'esempio di codice riportato di seguito viene illustrato come creare un oggetto chiamata, individuare i flussi associati alla chiamata, selezionare e creare terminali appropriati, selezionare i terminali sui flussi e completare la connessione.
ms.assetid: 49815b18-a8ea-46e0-b2a4-3d7a82e727b0
title: Effettuare una chiamata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbc22ebde34e65c9acc8e6c7dd81944b06804935
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309952"
---
# <a name="make-a-call"></a>Effettuare una chiamata

Nell'esempio di codice riportato di seguito viene illustrato come creare un oggetto chiamata, individuare i flussi associati alla chiamata, selezionare e creare terminali appropriati, selezionare i terminali sui flussi e completare la connessione.

Prima di usare questo esempio di codice, è necessario eseguire le operazioni in [Initialize TAPI](initialize-tapi.md) e [selezionare un indirizzo](select-an-address.md).

Inoltre, è necessario eseguire le operazioni illustrate in [selezionare un terminale](select-a-terminal.md) dopo la chiamata a [**ITAddress:: CreateCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall).

> [!Note]  
> Questo esempio non include il controllo degli errori e le versioni appropriate per il codice di produzione.

 

``` syntax
// Specify the destination address.
//
// szAddressToCall and 
// dwAddressType have been
// retrieved from a user interface.
ITBasicCallControl * pBasicCall
bstrAddressToCall = SysAllocString( szAddressToCall );
// If ( bstrAddressToCall == NULL ) process the error here. 

HRESULT hr = pAddress->CreateCall(
    bstrAddressToCall,
    dwAddressType,
    &pBasicCall
 );
// If ( hr != S_OK ) process the error here. 

SysFreeString(bstrAddressToCall);

// Create the required terminals for this call.
{
    // See the Select a Terminal code example.
}

// Make the connection.
pBasicCall->Connect( TRUE );
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ITAddress::CreateCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall)
</dt> <dt>

[**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol)
</dt> <dt>

[**ITBasicCallControl:: Connect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-connect)
</dt> </dl>

 

 



