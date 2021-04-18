---
title: attributo byte
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
ms.openlocfilehash: 347b1f22f06431c5490d4fdac15cdb22b25da69e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299212"
---
# <a name="byte-attribute"></a>attributo byte

La parola chiave **byte** specifica un elemento di dati a 8 bit.

``` syntax
byte identifier-name;
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*nome identificatore* 
</dt> <dd>

Specifica un identificatore MIDL valido. Gli identificatori MIDL validi sono costituiti da un massimo di 31 caratteri alfanumerici e/o di sottolineatura e devono iniziare con un carattere alfabetico o di sottolineatura.

</dd> </dl>

## <a name="remarks"></a>Commenti

Un elemento dati **byte** non subisce alcuna conversione per la trasmissione in rete come tipo [**char**](char-idl.md) .

Il tipo di **byte** è uno dei tipi di base del linguaggio di definizione dell'interfaccia (IDL). Il tipo di **byte** può essere visualizzato come identificatore di tipo nelle dichiarazioni [**const**](const.md) , nelle dichiarazioni [**typedef**](typedef.md) , nelle dichiarazioni generali e nei dichiaratori di funzione (come identificatore del tipo restituito dalla funzione e come identificatore del tipo di parametro). Per il contesto in cui vengono visualizzati gli identificatori di tipo, vedere [file di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tipi di base MIDL](midl-base-types.md)
</dt> <dt>

[**char**](char-idl.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> </dl>

 

 




