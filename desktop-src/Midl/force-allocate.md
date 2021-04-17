---
title: attributo force_allocate
description: L'attributo ACF \ Force \_ allocate \ forza l'allocazione di un parametro del puntatore usando l' \_ utente MIDL \_ allocate anziché ottimizzare l'allocazione.
ms.assetid: 40e3a7d9-7e4f-4e3d-8c82-fb6ef567f293
keywords:
- attributo force_allocate MIDL
topic_type:
- apiref
api_name:
- force_allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f73d0386d786e4d3004c78b1acccda7e9be8fc16
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472843"
---
# <a name="force_allocate-attribute"></a>Force \_ alloca attributo

L'attributo di allocazione forzata degli attributi di ACF impone l'allocazione di \[ **\_** \] un parametro del puntatore usando l' [**\_ utente MIDL \_ allocato**](midl-user-allocate-1.md) anziché ottimizzare l'allocazione.

``` syntax
[ [function-attribute-list <>] ] type-specifier <> [pointer- <>declarator <>] function-name <>( [ force_allocate [ , parameter-attribute-list <> ] ] type-specifier <> [declarator <>] , ...);
```

## <a name="parameters"></a>Parametri

Questo attributo non ha parametri.

## <a name="remarks"></a>Commenti

RPC tenta di ridurre al minimo le allocazioni di memoria nel server fornendo puntatori ai buffer di memoria interni. Questo approccio può causare problemi per le applicazioni che tentano di chiamare direttamente l' [**\_ utente MIDL \_ senza**](midl-user-free-1.md) i puntatori forniti da RPC, perché un puntatore ottimizzato non può essere liberato. Contrassegnando un parametro con **\[ Force \_ allocate \]** si eviterà questa ottimizzazione per tutti i puntatori che lo derivano.

Un altro uso comune di **\[ Force \_ allocate \]** consiste nel garantire l'allineamento della memoria a cui si fa riferimento se un'applicazione richiede un allineamento maggiore di quello della memoria a cui punta. Ad esempio, le applicazioni passano spesso dati in una matrice generica di byte anziché utilizzare il tipo effettivo, ma un byte è garantito solo per essere allineato a 1, che può causare problemi per le applicazioni che presuppongono un allineamento più grande. Contrassegnando il parametro con **\[ Force \_ allocate \]**, l'applicazione può garantire che tutte le memoria a cui puntano avranno un allineamento uguale a quello garantito dall' [**\_ utente MIDL \_ allocate**](midl-user-allocate-1.md).

## <a name="examples"></a>Esempi

``` syntax
/* IDL file */
void Func1([in, out, string] char **ppstr);
void Func2([in] long s, [in, size_is(s)] byte *pData);

/* ACF file */

/* e.g. The application wishes to call midl_user_free on *ppstr and supply a new pointer */
Func1([force_allocate] pstr);

/* e.g. pData really points to a structure that needs an alignment greater than 1 */
Func2([force_allocate] pData);
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Evitare le informazioni nascoste](/windows/desktop/WinProg64/avoiding-information-hiding)
</dt> <dt>

[Progettazione di interfacce compatibili con 64 bit](/windows/desktop/WinProg64/designing-64-bit-compatible-interfaces)
</dt> <dt>

[**\_alloca utente \_ MIDL**](midl-user-allocate-1.md)
</dt> <dt>

[**\_utente MIDL \_ gratuito**](midl-user-free-1.md)
</dt> <dt>

[**allocare**](allocate.md)
</dt> </dl>

 

 