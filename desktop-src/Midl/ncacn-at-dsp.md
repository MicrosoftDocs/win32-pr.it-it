---
title: attributo ncacn_at_dsp
description: La \_ \_ parola chiave ncacn at DSP identifica AppleTalk DSP come famiglia di protocolli per l'endpoint. Questa famiglia di protocolli è obsoleta e non deve essere utilizzata nelle nuove applicazioni.
ms.assetid: 3165e4f6-8869-4eff-af65-53e85f78a949
keywords:
- attributo ncacn_at_dsp MIDL
topic_type:
- apiref
api_name:
- ncacn_at_dsp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9149cd7270c2e82e760c24b4af1fed54c2c08622
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103963045"
---
# <a name="ncacn_at_dsp-attribute"></a>ncacn \_ nell' \_ attributo DSP

La parola chiave **ncacn \_ at \_ DSP** identifica AppleTalk DSP come famiglia di protocolli per l'endpoint. Questa famiglia di protocolli è obsoleta e non deve essere utilizzata nelle nuove applicazioni.

``` syntax
endpoint("ncacn_at_dsp:[port-name]")
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*nome porta* 
</dt> <dd>

Specifica una stringa di caratteri con lunghezza fino a 22 byte.

</dd> </dl>

## <a name="remarks"></a>Commenti

La sintassi della stringa di porta AppleTalk DSP, come tutte le stringhe di porta, è definita dall'implementazione del trasporto ed è indipendente dalla specifica IDL. Il compilatore MIDL esegue un controllo della sintassi limitato, ma non garantisce che la specifica dell'endpoint sia corretta. Alcune classi di errori possono essere segnalate in fase di esecuzione anziché in fase di compilazione.

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

[**endpoint**](endpoint.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Associazione stringa**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 