---
title: attributo firmato
description: La parola chiave signed indica il bit più significativo di una variabile integer che rappresenta un bit di segno anziché un bit di dati.
ms.assetid: 6116089a-647e-485b-8f79-9c9267aa4810
keywords:
- attributo MIDL firmato
topic_type:
- apiref
api_name:
- signed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 500b87c849f31082a036d605db0947650e914bed
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857085"
---
# <a name="signed-attribute"></a>attributo firmato

La parola chiave **signed** indica il bit più significativo di una variabile integer che rappresenta un bit di segno anziché un bit di dati.

``` syntax
[[ signed ]] type-qualifier [[ int ]]identifier-name;
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*type-qualifier* 
</dt> <dd>

Può essere qualsiasi di [**char**](char-idl.md), [**WCHAR \_ t**](wchar-t.md), [**Long**](long.md), [**short**](short.md)e [**small**](small.md).

</dd> <dt>

*nome identificatore* 
</dt> <dd>

Specifica un identificatore MIDL valido. Gli identificatori MIDL validi sono costituiti da un massimo di 31 caratteri alfanumerici e/o di sottolineatura e devono iniziare con un carattere alfabetico o di sottolineatura.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa parola chiave è facoltativa e può essere utilizzata con qualsiasi tipo di carattere e integer [**char**](char-idl.md), [**WCHAR \_ t**](wchar-t.md), [**Long**](long.md), [**short**](short.md)e [**small**](small.md). Facoltativamente, è possibile includere la parola chiave [**int**](int.md) dopo i qualificatori di tipo **Long**, **short** e **small**.

Quando si usa l'opzione del compilatore MIDL [**char**](char-idl.md), i tipi di carattere e Integer visualizzati nel file IDL senza parole chiave esplicite del segno possono apparire con le parole chiave **signed** o [**unsigned**](unsigned.md) nel file di intestazione generato. Per evitare confusione, specificare il segno dei tipi integer e character.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tipi di base MIDL](midl-base-types.md)
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

[**piccolo**](small.md)
</dt> <dt>

[**unsigned**](unsigned.md)
</dt> <dt>

[**WCHAR \_ t**](wchar-t.md)
</dt> </dl>

 

 




