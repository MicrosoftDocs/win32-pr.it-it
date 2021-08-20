---
title: Opzione /iid
description: L'opzione /iid specifica il nome del file dell'identificatore di interfaccia per un'interfaccia COM, eseguendo l'override del nome predefinito ottenuto aggiungendo \_ i.c al nome file IDL.
ms.assetid: 051593f5-e612-4b19-94e5-d7885dbede21
keywords:
- Opzione /iid MIDL
topic_type:
- apiref
api_name:
- /iid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bfe2aa9ebb96aa4878ac198e320bda4816f0b81025df5b0497d99c59a612767
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117992230"
---
# <a name="iid-switch"></a>Opzione /iid

**L'opzione /iid** specifica il nome del file dell'identificatore di interfaccia per un'interfaccia COM, eseguendo l'override del nome predefinito ottenuto aggiungendo \_ i.c al nome file IDL.

``` syntax
midl /iid filename
```

## <a name="switch-options"></a>Opzioni di cambio

<dl> <dt>

*Filename* 
</dt> <dd>

Specifica un nome file dell'identificatore di interfaccia che esegue l'override del nome file dell'identificatore di interfaccia predefinito per un'interfaccia COM. I nomi di file possono essere racchiusi in modo esplicito tra virgolette doppie (") per impedire alla shell di interpretare i caratteri speciali.

</dd> </dl>

## <a name="remarks"></a>Commenti

**L'opzione /iid** non influisce sulle interfacce RPC.

Se *filename* non include un percorso esplicito, il file viene scritto nella directory corrente o nella directory specificata dall'opzione [**/out.**](-out.md) Un percorso esplicito in *filename* esegue l'override della **specifica dell'opzione /out.**

## <a name="examples"></a>Esempio

**midl /iid "my \_ iid.c" filename.idl**

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

 

 




