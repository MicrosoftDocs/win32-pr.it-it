---
title: attributo Long
description: La parola chiave Long designa un intero a 32 bit.
ms.assetid: 5619e482-e3c3-4898-a70b-afd337d2749a
keywords:
- MIDL attributo Long
topic_type:
- apiref
api_name:
- long
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47ea9af3bfac85ff375f6d5433b4e9f3ed37d8f7
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103955919"
---
# <a name="long-attribute"></a>attributo Long

La parola chiave **Long** designa un intero a 32 bit.

``` syntax
[ signed | unsigned ] long [ int ] declarator-list;
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*elenco di dichiaratori* 
</dt> <dd>

Specifica uno o più dichiaratori C standard, ad esempio identificatori, dichiaratori di puntatore e dichiaratori di matrici. I dichiaratori di funzione e le dichiarazioni di campi di bit non sono consentiti nelle strutture trasmesse in chiamate a procedure remote. Questi dichiaratori sono consentiti in strutture non trasmesse. Separare più dichiaratori con virgole.

</dd> </dl>

## <a name="remarks"></a>Commenti

La parola chiave **Long** può essere preceduta dalla parola chiave [**signed**](signed.md) o dalla parola chiave [**unsigned**](unsigned.md). La parola chiave [**int**](int.md) è facoltativa e può essere omessa. Per il compilatore MIDL, un valore long integer è firmato per impostazione predefinita ed è sinonimo di **signed long int**. Sulle piattaforme a 32 bit, **Long** è sinonimo di **int**.

Il tipo **Long** Integer è uno dei tipi di base del linguaggio IDL. Il tipo **Long** Integer può essere visualizzato come identificatore di tipo nelle dichiarazioni [**const**](const.md) , nelle dichiarazioni [**typedef**](typedef.md) , nelle dichiarazioni generali e nei dichiaratori di funzione (come identificatore del tipo restituito dalla funzione e come identificatore del tipo di parametro). Per il contesto in cui vengono visualizzati gli identificatori di tipo, vedere [file di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**const**](const.md)
</dt> <dt>

[Tipi di base MIDL](midl-base-types.md)
</dt> <dt>

[**Hyper**](hyper.md)
</dt> <dt>

[**INT**](int.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**con segno**](signed.md)
</dt> <dt>

[**piccolo**](small.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**unsigned**](unsigned.md)
</dt> </dl>

 

 




