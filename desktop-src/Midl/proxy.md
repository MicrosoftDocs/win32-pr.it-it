---
title: attributo proxy
description: L'attributo \ proxy \ impedisce che l'automazione si registri come gestore di proxy/stub per un'interfaccia duale.
ms.assetid: 88e59938-83c9-436a-931c-f4396fdcf653
keywords:
- attributo MIDL proxy
topic_type:
- apiref
api_name:
- proxy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5aa8c9d305b7f51a012ae26d7b1a76d2e3011fd7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472758"
---
# <a name="proxy-attribute"></a>attributo proxy

L'attributo **\[ proxy \]** impedisce che l'automazione si registri come gestore di proxy/stub per un'interfaccia duale.

``` syntax
[ 
    proxy, 
    uuid(string-uuid <>)
    [ , interface-attribute-list <>] 
] 
interface interface-name <> : base-interface <>
{
    ...
}
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*stringa-UUID* 
</dt> <dd>

Specifica una stringa costituita da 8 cifre esadecimali seguite da un trattino, quindi da tre gruppi di 4 cifre esadecimali seguite da un trattino e quindi da 12 cifre esadecimali. È possibile racchiudere la stringa UUID tra virgolette, tranne quando si usa l'opzione del compilatore MIDL [**/OSF**](-osf.md).

</dd> <dt>

*Interface-Attribute-List* 
</dt> <dd>

Specifica un elenco di zero o più attributi IDL che si applicano all'interfaccia nel suo complesso. Quando sono presenti due o più attributi di interfaccia, devono essere separati da virgole.

</dd> <dt>

*Nome interfaccia* 
</dt> <dd>

Nome dell'interfaccia.

</dd> <dt>

*interfaccia di base* 
</dt> <dd>

Specifica il nome di un'interfaccia da cui questa interfaccia derivata eredita le funzioni membro, i codici di stato e gli attributi di interfaccia. L'interfaccia derivata non eredita le definizioni dei tipi. A tale scopo, usare la parola chiave [**Import**](import.md) per importare il file IDL dell'interfaccia di base.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'uso dell' \[ attributo **proxy** \] per un'interfaccia duale impedisce al TLB di assumere gli stub generati. Se questo attributo viene specificato, non è necessario annullare la registrazione del proxy TypeLib quando viene annullata la registrazione della libreria dei tipi.

### <a name="flags"></a>Flags

<dl> <dt>

<span id="TYPEFLAG_PROXY"></span><span id="typeflag_proxy"></span>\_proxy TYPEFLAG
</dt> <dd>

Le interfacce possono essere contrassegnate con il \_ flag proxy TypeFlag per indicare che utilizzeranno una libreria a collegamento dinamico proxy/stub. Questo flag specifica che non deve essere annullata la registrazione del proxy TypeLib quando viene annullata la registrazione della libreria dei tipi.

</dd> </dl>

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Generazione di una libreria dei tipi con MIDL**](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**Dual**](dual.md)
</dt> <dt>

[**TYPEFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 