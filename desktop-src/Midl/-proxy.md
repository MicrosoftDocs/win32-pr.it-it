---
title: Opzione /proxy
description: L'opzione /proxy specifica il nome del file proxy di interfaccia per un'interfaccia COM.
ms.assetid: 3428f723-81e1-441a-93d5-24034251830c
keywords:
- Opzione /proxy MIDL
topic_type:
- apiref
api_name:
- /proxy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dc3483706369837d96d14cf30b2f0c6ee307e376f8c422e11d56e06451a22e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811211"
---
# <a name="proxy-switch"></a>Opzione /proxy

**L'opzione /proxy** specifica il nome del file proxy di interfaccia per un'interfaccia COM.

``` syntax
midl /proxy proxy_file_name
```

## <a name="switch-options"></a>Opzioni switch

<dl> <dt>

*nome \_ del file \_ proxy* 
</dt> <dd>

Specifica un nome file che esegue l'override del nome del file proxy di interfaccia predefinito. I nomi di file possono essere racchiusi tra virgolette doppie (") per impedire alla shell di interpretare i caratteri speciali.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il nome file specificato sostituisce il nome file predefinito ottenuto aggiungendo \_ P.C al nome del file IDL. [**L'opzione /proxy**](proxy.md) non influisce sulle interfacce RPC.

Se *il nome \_ \_ del file* proxy non include un percorso esplicito, il file viene scritto nella directory corrente o nella directory specificata dall'opzione [**/out.**](-out.md) Un percorso esplicito nel *nome file proxy \_ \_ esegue* l'override della **specifica dell'opzione /out.**

Per una descrizione più dettagliata del file proxy di interfaccia e di altri file generati dal compilatore MIDL, vedere Sintassi della riga di comando [MIDL generale.](general-midl-command-line-syntax.md)

## <a name="examples"></a>Esempio

**midl /proxy my \_ proxy.c filename.idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi generale della riga di comando MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/header**](-header.md)
</dt> <dt>

[**/iid**](-iid.md)
</dt> <dt>

[**/out**](-out.md)
</dt> </dl>

 

 




