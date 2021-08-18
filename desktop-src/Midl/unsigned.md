---
title: attributo unsigned
description: La parola chiave unsigned indica che il bit più significativo di una variabile integer rappresenta un bit di dati anziché un bit con segno.
ms.assetid: bfcc6bec-895e-45e1-b162-b79651662aa6
keywords:
- attributo unsigned MIDL
topic_type:
- apiref
api_name:
- unsigned
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 383a8fc0379ca81abb9ad0a88edab8750661bdfa429e32e7e91d193aa0fd2938
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146174"
---
# <a name="unsigned-attribute"></a>attributo unsigned

La **parola chiave unsigned** indica che il bit più significativo di una variabile integer rappresenta un bit di dati anziché un bit con segno.

``` syntax
[[ unsigned ]] type-qualifier [[ int ]]identifier-name;
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*type-qualifier* 
</dt> <dd>

Può essere qualsiasi di [**char**](char-idl.md), [**wchar \_ t**](wchar-t.md), [**long**](long.md), [**int**](int.md), [**short**](short.md)e [**small**](small.md).

</dd> <dt>

*identifier-name* 
</dt> <dd>

Specifica un identificatore MIDL valido. Gli identificatori MIDL validi sono costituiti da un massimo di 31 caratteri alfanumerici e/o di sottolineatura e devono iniziare con un carattere alfabetico o di sottolineatura.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa parola chiave è facoltativa e può essere usata con qualsiasi tipo di carattere e integer [**char**](char-idl.md), [**wchar \_ t**](wchar-t.md), [**long**](long.md), [**short**](short.md)e [**small**](small.md). Facoltativamente, è possibile includere la parola chiave [**int**](int.md) dopo i qualificatori di tipo **long**, **short** e **small**.

Quando si usa l'opzione del compilatore MIDL [**/char**](-char.md), i tipi carattere e integer visualizzati nel file IDL senza parole chiave di segno esplicite possono essere visualizzati con la parola chiave [**signed**](signed.md) o **unsigned** nel file di intestazione generato. Per evitare confusione, specificare il segno dei tipi integer e carattere.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tipi di base MIDL](midl-base-types.md)
</dt> <dt>

[**Char**](char-idl.md)
</dt> <dt>

[**/char**](-char.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**int**](int.md)
</dt> <dt>

[**long**](long.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**Firmato**](signed.md)
</dt> <dt>

[**Piccolo**](small.md)
</dt> <dt>

[**wchar \_ t**](wchar-t.md)
</dt> </dl>

 

 




