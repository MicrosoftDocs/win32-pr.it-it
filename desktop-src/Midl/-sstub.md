---
title: Opzione /sstub
description: L'opzione /sstub specifica il nome del file stub del server per un'interfaccia RPC.
ms.assetid: 8e695e81-7c1b-40c0-aeaa-5390512fa099
keywords:
- Opzione /sstub MIDL
topic_type:
- apiref
api_name:
- /sstub
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdd83776939e9746103b2f12598a53832d767cebb93767142649a09b804339a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014069"
---
# <a name="sstub-switch"></a>Opzione /sstub

**L'opzione /sstub** specifica il nome del file stub del server per un'interfaccia RPC.

``` syntax
midl /sstub stub_file_name
```

## <a name="switch-options"></a>Opzioni switch

<dl> <dt>

*nome \_ file \_ stub* 
</dt> <dd>

Specifica un nome file che esegue l'override del nome del file stub del server predefinito. I nomi di file possono essere racchiusi tra virgolette doppie (") per impedire alla shell di interpretare i caratteri speciali.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il nome file specificato sostituisce il nome file predefinito. Per impostazione predefinita, il nome del file viene ottenuto aggiungendo \_ S.C al nome del file IDL. Questa opzione non influisce sulle interfacce OLE.

Quando si importano file, il nome file specificato si applica a un solo file stub, ovvero il file stub che corrisponde al file IDL specificato nella riga di comando.

Se *il nome del \_ file \_ stub* non include un percorso esplicito, il file viene scritto nella directory corrente o nella directory specificata [**dall'opzione /out.**](-out.md) Un percorso esplicito nel *nome file stub \_ \_* esegue l'override della **specifica dell'opzione /out.**

**L'opzione /server** none ha la precedenza **sull'opzione /sstub.**

## <a name="examples"></a>Esempio

**midl /sstub my \_ sstub.c filename.idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi generale della riga di comando MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/cstub**](-cstub.md)
</dt> <dt>

[**/header**](-header.md)
</dt> <dt>

[**/out**](-out.md)
</dt> </dl>

 

 




