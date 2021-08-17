---
title: Attributo byte
description: La parola chiave byte specifica un elemento di dati a 8 bit.
ms.assetid: d6401e05-5498-4d66-8f70-2c794ed26527
keywords:
- attributo byte MIDL
topic_type:
- apiref
api_name:
- byte
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a271cc81fe97fb25850bfe4dcb7d2edb55ba3c69805dab17d013bc646768e87f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118384726"
---
# <a name="byte-attribute"></a>Attributo byte

La parola chiave **byte** specifica un elemento di dati a 8 bit.

``` syntax
byte identifier-name;
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*identifier-name* 
</dt> <dd>

Specifica un identificatore MIDL valido. Gli identificatori MIDL validi sono costituiti da un massimo di 31 caratteri alfanumerici e/o caratteri di sottolineatura e devono iniziare con un carattere alfabetico o di sottolineatura.

</dd> </dl>

## <a name="remarks"></a>Commenti

Un elemento dati **byte** non viene sottoposto ad alcuna conversione per la trasmissione in rete come potrebbe essere un [**tipo char.**](char-idl.md)

Il **tipo di byte** è uno dei tipi di base del linguaggio IDL (Interface Definition Language). Il **tipo di byte** può essere visualizzato come identificatore di tipo in dichiarazioni [**const,**](const.md) [**dichiarazioni typedef,**](typedef.md) dichiarazioni generali e dichiaratori di funzione (come identificatore function-return-type e come identificatore di tipo parametro). Per il contesto in cui vengono visualizzati gli identificatori di tipo, vedere [File di definizione dell'interfaccia (IDL).](interface-definition-idl-file.md)

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tipi di base MIDL](midl-base-types.md)
</dt> <dt>

[**Char**](char-idl.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> </dl>

 

 




