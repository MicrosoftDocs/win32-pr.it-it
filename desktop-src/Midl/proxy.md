---
title: attributo proxy
description: L'attributo \proxy\ impedisce ad Automazione di registrarsi come gestore proxy/stub per un'interfaccia duale.
ms.assetid: 88e59938-83c9-436a-931c-f4396fdcf653
keywords:
- attributo proxy MIDL
topic_type:
- apiref
api_name:
- proxy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37e81cb7f67f87153825db59d921b6ee9ec7df6cd334ed2228896c8dec5f9d5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641420"
---
# <a name="proxy-attribute"></a>attributo proxy

**\[ L'attributo proxy \]** impedisce ad Automazione di registrarsi come gestore proxy/stub per un'interfaccia duale.

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

*string-uuid* 
</dt> <dd>

Specifica una stringa costituita da 8 cifre esadecimali seguite da un trattino, quindi tre gruppi di 4 cifre esadecimali, ognuno seguito da un trattino e quindi da 12 cifre esadecimali. È possibile racchiudere la stringa UUID tra virgolette, tranne quando si usa l'opzione del compilatore MIDL [**/osf**](-osf.md).

</dd> <dt>

*interface-attribute-list* 
</dt> <dd>

Specifica un elenco di zero o più attributi IDL che si applicano all'intera interfaccia. Quando sono presenti due o più attributi di interfaccia, devono essere separati da virgole.

</dd> <dt>

*interface-name* 
</dt> <dd>

Nome dell'interfaccia.

</dd> <dt>

*interfaccia di base* 
</dt> <dd>

Specifica il nome di un'interfaccia da cui questa interfaccia derivata eredita funzioni membro, codici di stato e attributi di interfaccia. L'interfaccia derivata non eredita le definizioni dei tipi. A tale scopo, usare la [**parola chiave import**](import.md) per importare il file IDL dell'interfaccia di base.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'uso \[ **dell'attributo proxy** \] per un'interfaccia duale impedisce al TLB di assumere gli stub generati. Se questo attributo viene specificato, la registrazione del proxy della libreria dei tipi non deve essere annullata quando viene annullata la registrazione della libreria dei tipi.

### <a name="flags"></a>Flags

<dl> <dt>

<span id="TYPEFLAG_PROXY"></span><span id="typeflag_proxy"></span>TYPEFLAG \_ PROXY
</dt> <dd>

Le interfacce possono essere contrassegnate con il flag TYPEFLAG PROXY per indicare che verrà utilizzata una libreria di collegamento dinamico \_ proxy/stub. Questo flag specifica che la registrazione del proxy della libreria dei tipi non deve essere annullata quando viene annullata la registrazione della libreria dei tipi.

</dd> </dl>

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Generazione di una libreria dei tipi con MIDL**](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**Dual**](dual.md)
</dt> <dt>

[**TYPEFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 