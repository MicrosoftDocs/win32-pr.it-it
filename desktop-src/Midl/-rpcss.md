---
title: Opzione /rpcss
description: L'opzione /rpcss, se specificata, agisce come se l'attributo enable allocate fosse specificato \_ in tutte le operazioni dell'interfaccia. L'utilizzo di questo attributo non è consigliato.
ms.assetid: a4507779-7d07-4517-8592-39f0d9460bc3
keywords:
- Opzione /rpcss MIDL
topic_type:
- apiref
api_name:
- /rpcss
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e0c3087f47bd12c852ef168b2684d5b094239cdac45933c8e7d831fc6461c1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118643741"
---
# <a name="rpcss-switch"></a>Opzione /rpcss

**L'opzione /rpcss,** se specificata, agisce come se l'attributo [**enable \_ allocate**](enable-allocate.md) fosse specificato in tutte le operazioni dell'interfaccia. L'utilizzo di questo attributo non è consigliato.

``` syntax
midl /rpcss
```

## <a name="switch-options"></a>Opzioni di cambio

Questa opzione non ha parametri.

## <a name="remarks"></a>Commenti

In modalità predefinita, il pacchetto RpcSs è abilitato solo se la procedura o l'interfaccia ha l'attributo [**enable \_ allocate**](enable-allocate.md) o l'opzione **/rpcss** è specificata nella riga di comando. In **modalità /osf,** lo stub sul lato server abilita il pacchetto di allocazione RpcSs.

## <a name="examples"></a>Esempio

**midl /rpcss filename.idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**abilitare \_ l'allocazione**](enable-allocate.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> </dl>

 

 




