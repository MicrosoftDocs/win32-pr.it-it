---
title: opzione/proxy
description: L'opzione/proxy specifica il nome del file proxy di interfaccia per un'interfaccia COM.
ms.assetid: 3428f723-81e1-441a-93d5-24034251830c
keywords:
- /proxy switch MIDL
topic_type:
- apiref
api_name:
- /proxy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27bff2103e22952e456976c6e0a88e7d232e42c3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857589"
---
# <a name="proxy-switch"></a>opzione/proxy

L'opzione **/proxy** specifica il nome del file proxy di interfaccia per un'interfaccia com.

``` syntax
midl /proxy proxy_file_name
```

## <a name="switch-options"></a>Opzioni switch

<dl> <dt>

*\_nome file \_ proxy* 
</dt> <dd>

Specifica un nome file che esegue l'override del nome del file proxy di interfaccia predefinito. I nomi di file possono essere racchiusi tra virgolette doppie (") per impedire alla shell di interpretare i caratteri speciali.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il nome file specificato sostituisce il nome file predefinito ottenuto aggiungendo \_ P. C al nome del file IDL. L'opzione del [**proxy**](proxy.md) /non influisce sulle interfacce RPC.

Se *il \_ \_ nome del file proxy* non include un percorso esplicito, il file viene scritto nella directory corrente o nella directory specificata dall'opzione [**/out**](-out.md) . Un percorso esplicito *nel \_ \_ nome del file proxy* esegue l'override della specifica del comcambio **/out** .

Per una descrizione più dettagliata del file proxy di interfaccia e di altri file generati dal compilatore MIDL, vedere [sintassi della riga di comando di MIDL generale](general-midl-command-line-syntax.md).

## <a name="examples"></a>Esempio

**MIDL/proxy My \_ proxy. c nomefile. idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> <dt>

[**/header**](-header.md)
</dt> <dt>

[**/IID**](-iid.md)
</dt> <dt>

[**/out**](-out.md)
</dt> </dl>

 

 




