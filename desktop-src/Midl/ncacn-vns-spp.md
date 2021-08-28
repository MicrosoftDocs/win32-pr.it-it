---
title: ncacn_vns_spp attributo
description: La parola chiave ncacn \_ vns \_ spp identifica Banyan Vines SPP come famiglia di protocolli per l'endpoint. Questa famiglia di protocolli è obsoleta e non deve essere usata nelle nuove applicazioni.
ms.assetid: a2aff0a6-2e7e-43e4-a180-f1ddd0456843
keywords:
- ncacn_vns_spp attributo MIDL
topic_type:
- apiref
api_name:
- ncacn_vns_spp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8409e7e9e0bfc01545ac73673f0653c5a4940c65422223233ec5005f5c9fc02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119560281"
---
# <a name="ncacn_vns_spp-attribute"></a>Attributo spp ncacn \_ vns \_

La **parola chiave ncacn \_ vns \_ spp** identifica Banyan Vines SPP come famiglia di protocolli per l'endpoint. Questa famiglia di protocolli è obsoleta e non deve essere usata nelle nuove applicazioni.

``` syntax
endpoint("ncacn_vns_spp:server-name[port-address]")
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*server-name* 
</dt> <dd>

Specifica il nome StreetTalk del server. Il nome è nel formato item@group @organization . L'elemento può contenere fino a 31 caratteri e il gruppo e l'organizzazione possono contenere fino a 15 caratteri.

</dd> <dt>

*port-name* 
</dt> <dd>

Specifica una porta SPP Banyan Vines. L'intervallo valido per gli endpoint statici è compreso tra 250 e 511.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per usare il protocollo di trasporto **ncacn \_ vns \_ spp** nelle applicazioni distribuite in esecuzione in Windows 2000, è necessario installare il software banyan Enterprise Client appropriato. Dopo **l'installazione, aprire Pannello di controllo**, scegliere **Configurazione e Aggiungi**, quindi selezionare Servizi RPC **\| Banyan per \| Banyan**. Il supporto per i client a 16 bit richiede software Vines appropriato. Per altre informazioni sul prodotto banyan Enterprise Client e sul software Vines a 16 bit, contattare Banyan.

La sintassi della stringa della porta di trasporto SPP Banyan Vines, come tutte le stringhe di porta, è definita indipendentemente dalla specifica IDL. Il compilatore esegue un controllo della sintassi, ma non garantisce che la specifica dell'endpoint sia corretta. Alcuni errori possono essere segnalati in fase di esecuzione anziché in fase di compilazione.

> [!Note]  
> Questa famiglia di protocolli non è supportata in Windows XP.

 

## <a name="examples"></a>Esempi

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version(1.1), 
    endpoint("ncacn_vns_spp:printer@sdkgrp@company[260]")
]
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**Endpoint**](endpoint.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**ncacn \_ in \_ dsp**](ncacn-at-dsp.md)
</dt> <dt>

[**ncacn \_ dnet \_ nsp**](ncacn-dnet-nsp.md)
</dt> <dt>

[**ncacn \_ ip \_ tcp**](ncacn-ip-tcp.md)
</dt> <dt>

[**ncacn \_ nb \_ ipx**](ncacn-nb-ipx.md)
</dt> <dt>

[**ncacn \_ spx**](ncacn-spx.md)
</dt> <dt>

[**ncacn \_ nb \_ nb**](ncacn-nb-nb.md)
</dt> <dt>

[**ncacn \_ nb \_ tcp**](ncacn-nb-tcp.md)
</dt> <dt>

[**ncacn \_ np**](ncacn-np.md)
</dt> <dt>

[**ncalrpc**](ncalrpc.md)
</dt> <dt>

[**ncadg \_ ipx**](ncadg-ipx.md)
</dt> <dt>

[**ncadg \_ ip \_ udp**](ncadg-ip-udp.md)
</dt> <dt>

[associazione di stringhe](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 