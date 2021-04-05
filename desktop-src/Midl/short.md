---
title: attributo Short
description: La parola chiave short definisce un intero a 16 bit.
ms.assetid: 622464a3-0d79-421a-8742-8a3746fe1533
keywords:
- MIDL attributo breve
topic_type:
- apiref
api_name:
- short
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b993c830c631b5b95246a7a191388ce897dbaafb
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104334284"
---
# <a name="short-attribute"></a>attributo Short

La parola chiave **short** definisce un intero a 16 bit.

``` syntax
[[ signed | unsigned ]] short [[ int ]] declarator-list;
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*elenco di dichiaratori* 
</dt> <dd>

Specifica uno o più dichiaratori C standard, ad esempio identificatori, dichiaratori di puntatore e dichiaratori di matrici. I dichiaratori di funzione e le dichiarazioni di campi di bit non sono consentiti nelle strutture trasmesse in chiamate a procedure remote. Questi dichiaratori sono consentiti in strutture non trasmesse. Separare più dichiaratori con virgole.

</dd> </dl>

## <a name="remarks"></a>Commenti

La parola chiave **short** può essere preceduta dalla parola chiave [**signed**](signed.md) o dalla parola chiave [**unsigned**](unsigned.md). La parola chiave [**int**](int.md) è facoltativa e può essere omessa. Per il compilatore MIDL, un valore short integer è firmato per impostazione predefinita ed è sinonimo di **signed short int**.

Il tipo **short** Integer è uno dei tipi di base del linguaggio IDL. Il tipo **short** Integer può essere visualizzato come identificatore di tipo nelle dichiarazioni [**const**](const.md) , nelle dichiarazioni [**typedef**](typedef.md) , nelle dichiarazioni generali e nei dichiaratori di funzione (come identificatore del tipo restituito dalla funzione e come identificatore del tipo di parametro). Per il contesto in cui vengono visualizzati gli identificatori di tipo, vedere [file di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tipi di base MIDL](midl-base-types.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**INT**](int.md)
</dt> <dt>

[**long**](long.md)
</dt> <dt>

[**con segno**](signed.md)
</dt> <dt>

[**piccolo**](small.md)
</dt> <dt>

[**unsigned**](unsigned.md)
</dt> </dl>

 

 




