---
title: Opzione /use_epv
description: L'opzione /use epv indica al compilatore MIDL di generare codice stub del server che chiama la routine dell'applicazione server tramite un vettore del punto di ingresso (epv), anziché tramite una \_ chiamata statica. L'uso di questo attributo non è consigliato.
ms.assetid: 2853d836-ded3-412a-916b-1143968123a2
keywords:
- /use_epv l'opzione MIDL
topic_type:
- apiref
api_name:
- /use_epv
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 614abaf4c124aa0a6e1ca5f7da347ab4a9a2264e174c91734e6a75b188500a3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014059"
---
# <a name="use_epv-switch"></a>/use \_ epv - opzione

**L'opzione /use \_ epv** indica al compilatore MIDL di generare codice stub del server che chiama la routine dell'applicazione server tramite un vettore del punto di ingresso (epv), anziché tramite una chiamata statica. L'uso di questo attributo non è consigliato.

``` syntax
midl /use_epv
```

## <a name="switch-options"></a>Opzioni di cambio

Questa opzione non ha parametri.

## <a name="remarks"></a>Commenti

In genere, le applicazioni richiedono il collegamento statico alla routine dell'applicazione server. Il compilatore MIDL genera tale chiamata per impostazione predefinita. Tuttavia, se un'applicazione richiede che lo stub del server chiami la routine dell'applicazione server usando epv, è necessario specificare l'opzione **/use \_ epv.** Quando viene **specificata l'opzione /use \_ epv,** il compilatore MIDL genera un valore epv predefinito. Questo epv predefinito viene quindi usato se l'applicazione non registra un altro epv tramite la [**chiamata RpcServerRegisterIf.**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif)

## <a name="examples"></a>Esempio

**midl /use \_ epv** *filename***.idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**/no \_ \_ epv predefinito**](-no-default-epv.md)
</dt> <dt>

[**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif)
</dt> </dl>

 

 