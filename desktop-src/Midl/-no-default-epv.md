---
title: /no_default_epv opzione
description: L' \_ \_ opzione EPV predefinita/No indica al compilatore MIDL di non generare un vettore del punto di ingresso predefinito (EPV). Non è consigliabile usare questo attributo.
ms.assetid: 160b5fd3-cd9c-4f51-8c35-6cddab120021
keywords:
- /no_default_epv switch MIDL
topic_type:
- apiref
api_name:
- /no_default_epv
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0a6e39319c5f03c1cd41959a009307b07bef66f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103956385"
---
# <a name="no_default_epv-switch"></a>\_ \_ opzione EPV predefinita/No

L' **opzione \_ \_ EPV predefinita/No** indica al compilatore MIDL di non generare un vettore del punto di ingresso predefinito (EPV). Non è consigliabile usare questo attributo.

``` syntax
midl /no_default_epv
```

## <a name="switch-options"></a>Opzioni switch

Questa opzione non ha parametri.

## <a name="remarks"></a>Commenti

In questo caso, l'applicazione deve registrare un EPV con la chiamata [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) . Confrontare questa opzione con l'opzione [**/utilizza \_ EPV**](-use-epv.md)

## <a name="examples"></a>Esempio

**MIDL/No \_ default \_ EPV filename. idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**\_EPV/utilizza**](-use-epv.md)
</dt> <dt>

[**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif)
</dt> </dl>

 

 