---
title: opzione/sstub
description: L'opzione/sstub specifica il nome del file stub del server per un'interfaccia RPC.
ms.assetid: 8e695e81-7c1b-40c0-aeaa-5390512fa099
keywords:
- /sstub switch MIDL
topic_type:
- apiref
api_name:
- /sstub
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 131be3dd1890967f7107bea64c3dc2634833653d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299173"
---
# <a name="sstub-switch"></a>opzione/sstub

L'opzione **/sstub** specifica il nome del file stub del server per un'interfaccia RPC.

``` syntax
midl /sstub stub_file_name
```

## <a name="switch-options"></a>Opzioni switch

<dl> <dt>

*\_nome file \_ Stub* 
</dt> <dd>

Specifica un nome file che esegue l'override del nome del file stub del server predefinito. I nomi di file possono essere racchiusi tra virgolette doppie (") per impedire alla shell di interpretare i caratteri speciali.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il nome file specificato sostituisce il nome file predefinito. Per impostazione predefinita, il nome del file viene ottenuto aggiungendo \_ S. C al nome del file IDL. Questa opzione non influisce sulle interfacce OLE.

Quando si importano file, il nome file specificato si applica a un solo file stub, ovvero il file stub che corrisponde al file IDL specificato nella riga di comando.

Se *il \_ \_ nome del file stub* non include un percorso esplicito, il file viene scritto nella directory corrente o nella directory specificata dall'opzione [**/out**](-out.md) . Un percorso esplicito *nel \_ \_ nome del file stub* esegue l'override della specifica del comcambio **/out** .

L'opzione **/Server** None ha la precedenza sull'opzione **/sstub**

## <a name="examples"></a>Esempio

**MIDL/sstub My \_ sstub. c filename. idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> <dt>

[**/cstub**](-cstub.md)
</dt> <dt>

[**/header**](-header.md)
</dt> <dt>

[**/out**](-out.md)
</dt> </dl>

 

 




