---
title: Attributo hyper
description: La parola chiave hyper indica un intero a 64 bit che può essere dichiarato con o senza segno.
ms.assetid: cadcacc7-8eea-4ce2-b69f-98a1d8bafeaa
keywords:
- attributo HYPER MIDL
topic_type:
- apiref
api_name:
- hyper
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44f202890d2d81dcd7916f29c0330bf8e7093a7cf189e7b76a8af64dd2f0d0a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895261"
---
# <a name="hyper-attribute"></a>Attributo hyper

La parola **chiave hyper** indica un intero a 64 bit che può essere dichiarato con o senza segno.

``` syntax
[ signed | unsigned ] hyper [ int ] declarator-list;
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*declarator-list* 
</dt> <dd>

Specifica uno o più dichiaratori C standard, ad esempio identificatori, dichiaratori di puntatori e dichiaratori di matrici. I dichiaratori di funzione e le dichiarazioni di campo di bit non sono consentiti nelle strutture trasmesse nelle chiamate di procedura remota. Questi dichiaratori sono consentiti nelle strutture che non vengono trasmesse. Separare più dichiaratori con virgole.

</dd> </dl>

## <a name="remarks"></a>Commenti

**L'hyper-type** è uno dei tipi di base del linguaggio IDL (Interface Definition Language). **L'hyper-type** può essere visualizzato come identificatore di tipo in dichiarazioni [**const,**](const.md) [**dichiarazioni typedef,**](typedef.md) dichiarazioni generali e dichiaratori di funzione (come identificatore function-return-type e come identificatore di tipo di parametro). Per il contesto in cui vengono visualizzati gli identificatori di tipo, vedere [File di definizione dell'interfaccia (IDL).](interface-definition-idl-file.md)

> [!Note]  
> Per le piattaforme a 16 bit, il compilatore MIDL sostituisce gli iper integer senza segno con **MIDL \_ uhyper.** In questo modo è possibile definire interfacce con hyper integer senza segno nelle piattaforme che non supportano direttamente interi a 64 bit. **MIDL \_ uhyper** è definito nei file di intestazione RPC.

 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tipi di base MIDL](midl-base-types.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> </dl>

 

 




