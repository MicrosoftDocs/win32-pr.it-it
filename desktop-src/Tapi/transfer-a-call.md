---
description: Nell'esempio di codice riportato di seguito viene illustrato il trasferimento di una chiamata.
ms.assetid: 05862605-2600-4cdf-8390-e24e4e8586f3
title: Trasferimento di una chiamata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd1d537efd33ea2df4ddb9ad3e9b55b633cca18f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315793"
---
# <a name="transfer-a-call"></a>Trasferimento di una chiamata

Nell'esempio di codice riportato di seguito viene illustrato il trasferimento di una chiamata.

Prima di usare questo esempio di codice, è necessario che sia in corso una chiamata ed è necessario eseguire le operazioni in [effettuare una chiamata](make-a-call.md) o [ricevere una chiamata](receive-a-call.md).

> [!Note]  
> Questo esempio non include il controllo degli errori e le versioni appropriate per il codice di produzione.

 

``` syntax
// From elsewhere in your code, you have obtained pAddress and pBasicCall, 
// which are pointers to the ITAddress and ITBasicCallControl interfaces
// of the call in progress that will be transferred.

// Create the call object for transfer. bstrAddressToCall and dwAddressType
// have been retrieved from a UI.
ITBasicCallControl * pConsultCall
HRESULT hr = pAddress->CreateCall(
        bstrAddressToCall,
        dwAddressType,
        &pConsultCall
        );
// If ( hr != S_OK ) process the error here. 

// Start the transfer.
hr = pBasicCall->Transfer(
        pConsultCall,
        VARIANT_TRUE
        );
// If ( hr != S_OK ) process the error here. 

// Depending on the service provider, additional operations may be available
// or required.

// Finish the transfer.
hr = pConsultCall->Finish(FM_ASTRANSFER);
// If ( hr != S_OK ) process the error here. 

// The consultation call transitions to CS_DISCONNECTED.
// The objects associated with pConsultCall and pBasicCall can be released immediately or
// used for information purposes and released later.
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)
</dt> <dt>

[**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol)
</dt> <dt>

[**ITCallHub**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallhub)
</dt> </dl>

 

 



