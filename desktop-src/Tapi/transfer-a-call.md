---
description: Nell'esempio di codice seguente viene illustrato un trasferimento di chiamata.
ms.assetid: 05862605-2600-4cdf-8390-e24e4e8586f3
title: Trasferire una chiamata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e71d6e6fd9dc275a6d4c00e84806132cabf756effcb41e7a704b20929bc46d1a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072831"
---
# <a name="transfer-a-call"></a>Trasferire una chiamata

Nell'esempio di codice seguente viene illustrato un trasferimento di chiamata.

Prima di usare questo esempio di codice, è necessario che sia in corso una chiamata ed è necessario eseguire le operazioni in Effettuare [una chiamata](make-a-call.md) o Ricevere [una chiamata](receive-a-call.md).

> [!Note]  
> In questo esempio non sono disponibili il controllo degli errori e le versioni appropriate per il codice di produzione.

 

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

 

 



