---
title: attributo Small
description: La parola chiave Small designa un numero intero a 8 bit.
ms.assetid: 368e8836-1baa-4547-a62b-f34ac38bbdb2
keywords:
- MIDL attributo Small
topic_type:
- apiref
api_name:
- small
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5a0f106f1be1ba6d0acabf877b5dbefab3eaff6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104397367"
---
# <a name="small-attribute"></a>attributo Small

La parola chiave **small** designa un numero intero a 8 bit.

``` syntax
small identifier-name;
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*nome identificatore* 
</dt> <dd>

Specifica un identificatore MIDL valido. Gli identificatori MIDL validi sono costituiti da un massimo di 31 caratteri alfanumerici e/o di sottolineatura e devono iniziare con un carattere alfabetico o di sottolineatura.

</dd> </dl>

## <a name="remarks"></a>Commenti

La parola chiave **small** può essere preceduta dalla parola chiave [**signed**](signed.md) o dalla parola chiave [**unsigned**](unsigned.md). La parola chiave [**int**](int.md) è facoltativa e può essere omessa. Per il compilatore MIDL, un numero intero piccolo è **firmato** per impostazione predefinita ed è sinonimo di **signed Small int**.

Il tipo di valore integer **piccolo** è uno dei tipi di base del linguaggio IDL. Il tipo di valore integer **piccolo** può essere visualizzato come identificatore di tipo nelle dichiarazioni [**const**](const.md) , nelle dichiarazioni [**typedef**](typedef.md) , nelle dichiarazioni generali e nei dichiaratori di funzione (come identificatore del tipo restituito dalla funzione e come identificatore del tipo di parametro). Per il contesto in cui vengono visualizzati gli identificatori di tipo, vedere [file di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md).

Il segno del tipo **piccolo** può essere modificato dall'opzione del compilatore MIDL [**/char**](-char.md). Per evitare confusione, specificare il segno del tipo integer con le parole chiave [**signed**](signed.md) e [**unsigned**](unsigned.md).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**/char**](-char.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**INT**](int.md)
</dt> <dt>

[**long**](long.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**con segno**](signed.md)
</dt> <dt>

[**unsigned**](unsigned.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> </dl>

 

 




