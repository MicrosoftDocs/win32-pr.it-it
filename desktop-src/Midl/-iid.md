---
title: opzione/IID
description: L'opzione/IID specifica il nome del file dell'identificatore di interfaccia per un'interfaccia COM, eseguendo l'override del nome predefinito ottenuto aggiungendo \_ i. c al nome del file IDL.
ms.assetid: 051593f5-e612-4b19-94e5-d7885dbede21
keywords:
- /IID switch MIDL
topic_type:
- apiref
api_name:
- /iid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 631a28f1bc5a1a24253c9416104df9941cd8da33
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104397874"
---
# <a name="iid-switch"></a>opzione/IID

L'opzione **/IID** specifica il nome del file dell'identificatore di interfaccia per un'interfaccia com, eseguendo l'override del nome predefinito ottenuto aggiungendo \_ i. c al nome del file IDL.

``` syntax
midl /iid filename
```

## <a name="switch-options"></a>Opzioni switch

<dl> <dt>

*filename* 
</dt> <dd>

Specifica un nome di file dell'identificatore di interfaccia che sostituisce il nome del file dell'identificatore di interfaccia predefinito per un'interfaccia COM. I nomi di file possono essere racchiusi tra virgolette doppie (") per impedire alla shell di interpretare i caratteri speciali.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'opzione **/IID** non influisce sulle interfacce RPC.

Se *filename* non include un percorso esplicito, il file viene scritto nella directory corrente o nella directory specificata dall'opzione [**/out**](-out.md) . Un percorso esplicito in *filename* esegue l'override della specifica del Commuter **/out** .

## <a name="examples"></a>Esempio

**MIDL/IID "My \_ IID. c" nomefile. idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> <dt>

[**/header**](-header.md)
</dt> <dt>

[**/out**](-out.md)
</dt> <dt>

[**/proxy**](-proxy.md)
</dt> </dl>

 

 




