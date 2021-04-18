---
title: attributo senza segno
description: La parola chiave unsigned indica che il bit più significativo di una variabile integer rappresenta un bit di dati anziché un bit con segno.
ms.assetid: bfcc6bec-895e-45e1-b162-b79651662aa6
keywords:
- attributo MIDL senza segno
topic_type:
- apiref
api_name:
- unsigned
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 329d638f1b5be97e5b441aa4e84825fe59a4a3f0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299167"
---
# <a name="unsigned-attribute"></a>attributo senza segno

La parola chiave **unsigned** indica che il bit più significativo di una variabile integer rappresenta un bit di dati anziché un bit con segno.

``` syntax
[[ unsigned ]] type-qualifier [[ int ]]identifier-name;
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*type-qualifier* 
</dt> <dd>

Può essere qualsiasi tipo di [**carattere**](char-idl.md), [**WCHAR \_ t**](wchar-t.md), [**Long**](long.md), [**int**](int.md), [**short**](short.md)e [**small**](small.md).

</dd> <dt>

*nome identificatore* 
</dt> <dd>

Specifica un identificatore MIDL valido. Gli identificatori MIDL validi sono costituiti da un massimo di 31 caratteri alfanumerici e/o di sottolineatura e devono iniziare con un carattere alfabetico o di sottolineatura.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa parola chiave è facoltativa e può essere utilizzata con qualsiasi tipo di carattere e integer [**char**](char-idl.md), [**WCHAR \_ t**](wchar-t.md), [**Long**](long.md), [**short**](short.md)e [**small**](small.md). Facoltativamente, è possibile includere la parola chiave [**int**](int.md) dopo i qualificatori di tipo **Long**, **short** e **small**.

Quando si usa l'opzione del compilatore MIDL [**/char**](-char.md), i tipi di carattere e Integer visualizzati nel file IDL senza parole chiave esplicite del segno possono apparire con la parola chiave [**signed**](signed.md) o **unsigned** nel file di intestazione generato. Per evitare confusione, specificare il segno dei tipi integer e character.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tipi di base MIDL](midl-base-types.md)
</dt> <dt>

[**char**](char-idl.md)
</dt> <dt>

[**/char**](-char.md)
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

[**piccolo**](small.md)
</dt> <dt>

[**WCHAR \_ t**](wchar-t.md)
</dt> </dl>

 

 




