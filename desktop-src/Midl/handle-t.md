---
title: handle_t attributo
description: La parola \_ chiave handle t dichiara un oggetto come del tipo di handle primitivo handle \_ t. Un handle di associazione primitivo è un oggetto dati che può essere usato dall'applicazione per rappresentare l'associazione.
ms.assetid: 94962ed6-5c17-43e7-853f-1e9c4b3118a7
keywords:
- handle_t attributo MIDL
topic_type:
- apiref
api_name:
- handle_t
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 251a2574908891d29baf9d4748943d0550f3f015eddccbdd123e31598b39b08c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117991329"
---
# <a name="handle_t-attribute"></a>Attributo handle \_ t

La **parola chiave handle \_ t** dichiara un oggetto come del tipo di handle primitivo **handle \_ t**. Un handle di associazione primitivo è un oggetto dati che può essere usato dall'applicazione per rappresentare l'associazione.

``` syntax
typedef RPC_BINDING_HANDLE handle_t;
```

## <a name="parameters"></a>Parametri

Questo attributo non ha parametri.

## <a name="remarks"></a>Commenti

Il **tipo \_ handle t** è uno dei tipi predefiniti del linguaggio IDL (Interface Definition Language). Può essere visualizzato come identificatore di tipo nelle dichiarazioni [**typedef,**](typedef.md) nelle dichiarazioni generali e nei dichiaratori di funzione (come identificatore function-return-type e identificatore di tipo di parametro). Per il contesto in cui vengono visualizzati gli identificatori di tipo, vedere [File di definizione dell'interfaccia (IDL).](interface-definition-idl-file.md)

In Microsoft RPC, i parametri di tipo **handle \_ t** possono verificarsi solo come **\[** [**nei**](in.md) **\]** parametri . Gli handle primitivi non possono avere **\[** [**l'attributo unique**](unique.md) **\]** o **\[** [**ptr.**](ptr.md) **\]**

I parametri di **tipo handle \_ t** (parametri di handle primitivi) non vengono trasmessi in rete.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tipi di base MIDL](midl-base-types.md)
</dt> <dt>

[Binding e handle](/windows/desktop/Rpc/binding-and-handles)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Pollici**](in.md)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**Unico**](unique.md)
</dt> </dl>

 

 