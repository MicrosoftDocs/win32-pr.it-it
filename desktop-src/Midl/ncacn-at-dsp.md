---
title: ncacn_at_dsp attributo
description: La parola chiave ncacn \_ at \_ dsp identifica AppleTalk DSP come famiglia di protocolli per l'endpoint. Questa famiglia di protocolli è obsoleta e non deve essere usata nelle nuove applicazioni.
ms.assetid: 3165e4f6-8869-4eff-af65-53e85f78a949
keywords:
- ncacn_at_dsp attributo MIDL
topic_type:
- apiref
api_name:
- ncacn_at_dsp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb021f9212f1034f0b3c235ad77d9ad270325af914887252494316f9ae1c41b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118642772"
---
# <a name="ncacn_at_dsp-attribute"></a>Attributo ncacn \_ at \_ dsp

La **parola chiave ncacn \_ at \_ dsp** identifica AppleTalk DSP come famiglia di protocolli per l'endpoint. Questa famiglia di protocolli è obsoleta e non deve essere usata nelle nuove applicazioni.

``` syntax
endpoint("ncacn_at_dsp:[port-name]")
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*port-name* 
</dt> <dd>

Specifica una stringa di caratteri lunga fino a 22 byte.

</dd> </dl>

## <a name="remarks"></a>Commenti

La sintassi della stringa di porta DSP AppleTalk, come tutte le stringhe di porta, è definita dall'implementazione del trasporto ed è indipendente dalla specifica IDL. Il compilatore MIDL esegue un controllo della sintassi limitato, ma non garantisce che la specifica dell'endpoint sia corretta. Alcune classi di errori possono essere segnalate in fase di esecuzione anziché in fase di compilazione.

## <a name="examples"></a>Esempi

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_at_dsp:[my_services_endpoint]") 
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

[**associazione di stringhe**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 