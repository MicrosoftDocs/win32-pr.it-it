---
description: L'esempio di codice seguente illustra la creazione di una semplice conferenza telefonica. Per informazioni sulle videoconferenze multimediali multicast IP, vedere Informazioni su Rendezvous IP Telephony Conferencing.
ms.assetid: fb55853d-b882-41c8-99e6-bfa897b2dabf
title: Creare una conferenza semplice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61ca284e0629fa4318765b3ae12a63a9319beb585baf41a8dd636b1023c16329
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118867513"
---
# <a name="create-a-simple-conference"></a>Creare una conferenza semplice

L'esempio di codice seguente illustra la creazione di una semplice conferenza telefonica. Per informazioni sulle videoconferenze multimediali multicast IP, vedere [Informazioni su Rendezvous IP Telephony Conferencing](about-rendezvous-ip-telephony-conferencing.md).

Prima di usare questo esempio di codice, è necessario che sia [in](make-a-call.md) corso una chiamata ed è necessario eseguire le operazioni in Effettuare una chiamata o Ricevere una chiamata. [](receive-a-call.md)

> [!Note]  
> In questo esempio non sono disponibili il controllo degli errori e le versioni appropriate per il codice di produzione.

 

``` syntax
// From elsewhere in your code, you have obtained pBasicCall and pCallInfo, 
// which are pointers to the ITBasicCallControl and ITCallInfo interfaces
// of a call currently in progress. pAddress is an ITAddress pointer.

// Create a consultation call for the conference.
ITBasicCallControl *pConsultCall;
HRESULT hr = pAddress->CreateCall(
        bstrAddressToCall,
        dwAddressType,
        &pConsultCall
        );
// If ( hr != S_OK ) process the error here. 

// Move the consultation call into your conference.
// Note: If a CallHub object does not already exist, TAPI will create it.
hr = pBasicCall->Conference(
               pConsultCall,
               VARIANT_TRUE
               );
// If ( hr != S_OK ) process the error here. 

// Finish the creation of the conference.
hr = pConsultCall->Finish(FM_ASCONFERENCE);
// If ( hr != S_OK ) process the error here. 

// Assuming the Finish method succeeds, the consultation call (pConsultCall)
// may transition to the CS_DISCONNECTED state or may remain connected, 
// depending on the service provider.
//
// Get the ITCallHub interface pointer.
ITCallHub *pCallHub;
hr = pCallInfo->get_CallHub( pCallHub );
// If ( hr != S_OK ) process the error here. 

// You can use the ITCallHub interface to obtain additional information on
// the conference. Specific capabilities depend on the TSP/MSP being used.
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)
</dt> <dt>

[**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol)
</dt> <dt>

[**ITCallHub**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallhub)
</dt> </dl>

 

 



