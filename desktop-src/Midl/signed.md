---
title: attributo signed
description: La parola chiave signed indica che il bit più significativo di una variabile integer rappresenta un bit di segno anziché un bit di dati.
ms.assetid: 6116089a-647e-485b-8f79-9c9267aa4810
keywords:
- attributo con segno MIDL
topic_type:
- apiref
api_name:
- signed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f3db15bc46d6d8ab3ec108c648d094ebf706d9286a8c4b0a823fa409e118e3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641335"
---
# <a name="signed-attribute"></a>attributo signed

La parola chiave **signed** indica che il bit più significativo di una variabile integer rappresenta un bit di segno anziché un bit di dati.

``` syntax
[[ signed ]] type-qualifier [[ int ]]identifier-name;
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*type-qualifier* 
</dt> <dd>

Può essere qualsiasi di [**char**](char-idl.md), [**wchar \_ t**](wchar-t.md), [**long**](long.md), [**short**](short.md)e [**small**](small.md).

</dd> <dt>

*identifier-name* 
</dt> <dd>

Specifica un identificatore MIDL valido. Gli identificatori MIDL validi sono costituiti da un massimo di 31 caratteri alfanumerici e/o di sottolineatura e devono iniziare con un carattere alfabetico o di sottolineatura.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa parola chiave è facoltativa e può essere usata con qualsiasi tipo di carattere e integer [**char**](char-idl.md), [**wchar \_ t**](wchar-t.md), [**long**](long.md), [**short**](short.md)e [**small**](small.md). Facoltativamente, è possibile includere la parola chiave [**int**](int.md) dopo i qualificatori di tipo **long**, **short** e **small**.

Quando si usa l'opzione del compilatore MIDL [**char**](char-idl.md), i tipi character e  integer visualizzati nel file IDL senza parole chiave di segno esplicite possono essere visualizzati con le parole chiave signed o [**unsigned**](unsigned.md) nel file di intestazione generato. Per evitare confusione, specificare il segno dei tipi integer e carattere.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tipi di base MIDL](midl-base-types.md)
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

[**Piccolo**](small.md)
</dt> <dt>

[**Unsigned**](unsigned.md)
</dt> <dt>

[**wchar \_ t**](wchar-t.md)
</dt> </dl>

 

 




