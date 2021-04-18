---
title: /use_epv opzione
description: L' \_ opzione/utilizza EPV indica al compilatore MIDL di generare codice stub del server che chiama la routine dell'applicazione server tramite un vettore del punto di ingresso (EPV), anziché da una chiamata statica. Non è consigliabile usare questo attributo.
ms.assetid: 2853d836-ded3-412a-916b-1143968123a2
keywords:
- /use_epv switch MIDL
topic_type:
- apiref
api_name:
- /use_epv
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec73b5cb9833c15a77c96a784e1ded88d266f9a6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299662"
---
# <a name="use_epv-switch"></a>\_opzione EPV/utilizza

L'opzione **/utilizza \_ EPV** indica al compilatore MIDL di generare codice stub del server che chiama la routine dell'applicazione server tramite un vettore del punto di ingresso (EPV), anziché da una chiamata statica. Non è consigliabile usare questo attributo.

``` syntax
midl /use_epv
```

## <a name="switch-options"></a>Opzioni switch

Questa opzione non ha parametri.

## <a name="remarks"></a>Commenti

In genere, le applicazioni richiedono il collegamento statico alla routine dell'applicazione server. Per impostazione predefinita, il compilatore MIDL genera una chiamata di questo tipo. Tuttavia, se un'applicazione richiede che lo stub del server chiami la routine dell'applicazione server usando EPV, è necessario specificare l'opzione **/utilizza \_ EPV** . Quando viene specificata l'opzione **/utilizza \_ EPV** , il compilatore MIDL genera un EPV predefinito. Questa EPV predefinita viene quindi utilizzata se l'applicazione non registra un altro EPV tramite la chiamata [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) .

## <a name="examples"></a>Esempio

**MIDL/utilizza \_ EPV** *nomefile * * *. idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**/No \_ default \_ EPV**](-no-default-epv.md)
</dt> <dt>

[**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif)
</dt> </dl>

 

 