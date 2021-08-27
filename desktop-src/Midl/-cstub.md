---
title: Opzione /cstub
description: L'opzione /cstub specifica il nome del file stub client per un'interfaccia RPC.
ms.assetid: f2c9e083-3511-4e72-b1d1-14a3a662ffaf
keywords:
- Opzione /cstub MIDL
topic_type:
- apiref
api_name:
- /cstub
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47b4f635b6d09c85b345eea6dcb7320294e226ad6f2540f01af1e9b3e8098671
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105660"
---
# <a name="cstub-switch"></a>Opzione /cstub

**L'opzione /cstub** specifica il nome del file stub client per un'interfaccia RPC.

``` syntax
midl /cstub stub_file_name
```

## <a name="switch-options"></a>Opzioni di cambio

<dl> <dt>

*Nome \_ file \_ stub* 
</dt> <dd>

Specifica un nome di file che esegue l'override del nome del file stub del client predefinito. I nomi di file possono essere racchiusi in modo esplicito tra virgolette doppie (") per impedire alla shell di interpretare i caratteri speciali.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il nome file specificato sostituisce il nome file predefinito. Per impostazione predefinita, il nome del file viene ottenuto aggiungendo l'estensione \_ c.c al nome del file IDL. Questa opzione non influisce sulle interfacce OLE.

Quando si importano file, il nome file specificato si applica a un solo file stub, ovvero al file stub che corrisponde al file IDL specificato nella riga di comando.

Se *il nome del \_ file \_ stub* non include un percorso esplicito, il file viene scritto nella directory corrente o nella directory specificata [**dall'opzione /out.**](-out.md) Un percorso esplicito nel *nome file stub \_ \_* esegue l'override della **specifica dell'opzione /out.**

**L'opzione /client** none ha la precedenza **sull'opzione /cstub.**

## <a name="examples"></a>Esempio

**midl /cstub my \_ cstub.c filename.idl**

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

 

 




