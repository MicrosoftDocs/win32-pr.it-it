---
title: attributo handle_t
description: La \_ parola chiave handle t dichiara che un oggetto deve essere del tipo di handle primitivo handle \_ t. Un handle di associazione primitivo è un oggetto dati che può essere utilizzato dall'applicazione per rappresentare l'associazione.
ms.assetid: 94962ed6-5c17-43e7-853f-1e9c4b3118a7
keywords:
- attributo handle_t MIDL
topic_type:
- apiref
api_name:
- handle_t
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 435dcfcf620bd33043d8c8c7d948bccd74eb4e77
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337055"
---
# <a name="handle_t-attribute"></a>handle \_ t (attributo)

La parola chiave **handle \_ t** dichiara che un oggetto deve essere del tipo di handle primitivo **handle \_ t**. Un handle di associazione primitivo è un oggetto dati che può essere utilizzato dall'applicazione per rappresentare l'associazione.

``` syntax
typedef RPC_BINDING_HANDLE handle_t;
```

## <a name="parameters"></a>Parametri

Questo attributo non ha parametri.

## <a name="remarks"></a>Commenti

Il tipo di **handle \_ t** è uno dei tipi predefiniti del linguaggio di definizione dell'interfaccia (IDL). Può essere visualizzato come identificatore di tipo nelle dichiarazioni [**typedef**](typedef.md) , nelle dichiarazioni generali e nei dichiaratori di funzione (come identificatore del tipo restituito dalla funzione e come identificatore del tipo di parametro). Per il contesto in cui vengono visualizzati gli identificatori di tipo, vedere [file di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md).

In Microsoft RPC, i parametri di tipo **handle \_ t** possono verificarsi solo come **\[** parametri [**in**](in.md) **\]** . Gli handle primitivi non possono avere l' **\[** attributo [**Unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** .

I parametri di tipo **handle \_ t** (parametri di handle primitivi) non vengono trasmessi in rete.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tipi di base MIDL](midl-base-types.md)
</dt> <dt>

[Binding e handle](/windows/desktop/Rpc/binding-and-handles)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**in**](in.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**unico**](unique.md)
</dt> </dl>

 

 