---
title: attributo Hyper
description: La parola chiave Hyper indica un intero a 64 bit che può essere dichiarato come con segno o senza segno.
ms.assetid: cadcacc7-8eea-4ce2-b69f-98a1d8bafeaa
keywords:
- attributo MIDL Hyper
topic_type:
- apiref
api_name:
- hyper
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57da7c0d54e5b9ffcd47f76b22825d13b0a8cff9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718070"
---
# <a name="hyper-attribute"></a>attributo Hyper

La parola chiave **Hyper** indica un intero a 64 bit che può essere dichiarato come con segno o senza segno.

``` syntax
[ signed | unsigned ] hyper [ int ] declarator-list;
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*elenco di dichiaratori* 
</dt> <dd>

Specifica uno o più dichiaratori C standard, ad esempio identificatori, dichiaratori di puntatore e dichiaratori di matrici. I dichiaratori di funzione e le dichiarazioni di campi di bit non sono consentiti nelle strutture trasmesse in chiamate a procedure remote. Questi dichiaratori sono consentiti in strutture non trasmesse. Separare più dichiaratori con virgole.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il tipo **Hyper** è uno dei tipi di base del linguaggio di definizione dell'interfaccia (IDL). Il tipo **Hyper** può essere visualizzato come identificatore di tipo nelle dichiarazioni [**const**](const.md) , nelle dichiarazioni [**typedef**](typedef.md) , nelle dichiarazioni generali e nei dichiaratori di funzione (come identificatore del tipo restituito dalla funzione e come identificatore del tipo di parametro). Per il contesto in cui vengono visualizzati gli identificatori di tipo, vedere [file di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md).

> [!Note]  
> Per le piattaforme a 16 bit, il compilatore MIDL sostituisce interi senza segno con **MIDL \_ uhyper**. Ciò consente di definire interfacce con interi senza segno su piattaforme che non supportano direttamente interi a 64 bit. **MIDL \_ uhyper** è definito nei file di intestazione RPC.

 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tipi di base MIDL](midl-base-types.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> </dl>

 

 




