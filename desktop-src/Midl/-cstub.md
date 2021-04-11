---
title: opzione/cstub
description: L'opzione/cstub specifica il nome del file stub client per un'interfaccia RPC.
ms.assetid: f2c9e083-3511-4e72-b1d1-14a3a662ffaf
keywords:
- /cstub switch MIDL
topic_type:
- apiref
api_name:
- /cstub
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 878f6eee47deaac3887c3f9936c18b0185cc807a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104334572"
---
# <a name="cstub-switch"></a>opzione/cstub

L'opzione **/cstub** specifica il nome del file stub client per un'interfaccia RPC.

``` syntax
midl /cstub stub_file_name
```

## <a name="switch-options"></a>Opzioni switch

<dl> <dt>

*\_nome file \_ Stub* 
</dt> <dd>

Specifica un nome file che esegue l'override del nome del file stub client predefinito. I nomi di file possono essere racchiusi tra virgolette doppie (") per impedire alla shell di interpretare i caratteri speciali.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il nome file specificato sostituisce il nome file predefinito. Per impostazione predefinita, il nome del file viene ottenuto aggiungendo l'estensione \_ c. c al nome del file IDL. Questa opzione non influisce sulle interfacce OLE.

Quando si importano file, il nome file specificato si applica a un solo file stub, ovvero il file stub che corrisponde al file IDL specificato nella riga di comando.

Se *il \_ \_ nome del file stub* non include un percorso esplicito, il file viene scritto nella directory corrente o nella directory specificata dall'opzione [**/out**](-out.md) . Un percorso esplicito *nel \_ \_ nome del file stub* esegue l'override della specifica del comcambio **/out** .

L'opzione **/client** None ha la precedenza sull'opzione **/cstub** .

## <a name="examples"></a>Esempio

**MIDL/cstub My \_ cstub. c filename. idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**/header**](-header.md)
</dt> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> <dt>

[**/out**](-out.md)
</dt> <dt>

[**/sstub**](-sstub.md)
</dt> </dl>

 

 




