---
title: opzione/SAL
description: L'opzione/Sal indica a MIDL di generare le annotazioni SAL nei file stub generati.
ms.assetid: 452A19CA-6F72-416F-8059-77937412DA88
keywords:
- /Sal switch MIDL
topic_type:
- apiref
api_name:
- /sal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ef52eb510c71bfdb153b95a5d05e992359e39b6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299091"
---
# <a name="sal-switch"></a>opzione/SAL

L'opzione **/Sal** indica a MIDL di generare le annotazioni SAL nei file stub generati.

``` syntax
midl /sal
```

## <a name="switch-options"></a>Opzioni switch

Questa opzione non ha parametri.

## <a name="remarks"></a>Commenti

MIDL contrassegna i parametri dei puntatori e delle matrici con le annotazioni che riflettono la descrizione del parametro nel file IDL come applicato da RPC e dal motore di marshalling del recapito. MIDL non crea annotazioni per i parametri nei metodi di interfaccia contrassegnati con l'attributo [**\[ locale \]**](local.md), a meno che nella riga di comando non sia presente anche [**/SAL \_ local**](-sal-local.md) . Per eseguire l'override dell'annotazione generata da MIDL, usare l'attributo [**\[ annotate \]**](annotate.md) .

Le annotazioni generate da MIDL sono sempre precedute dal prefisso \_ \_ RPC \_ e richiedono l'uso dell'intestazione **rpcsal. h** per convertire l'annotazione in annotazioni SAL standard.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> <dt>

[**/SAL \_ locale**](-sal-local.md)
</dt> <dt>

[**\[Annotare\]**](annotate.md)
</dt> </dl>

 

 




