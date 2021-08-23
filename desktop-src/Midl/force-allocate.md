---
title: force_allocate attributo
description: L'attributo ACF \ force allocate\ forza l'allocazione di un parametro puntatore usando midl user allocate invece di \_ \_ \_ ottimizzare l'allocazione.
ms.assetid: 40e3a7d9-7e4f-4e3d-8c82-fb6ef567f293
keywords:
- force_allocate attributo MIDL
topic_type:
- apiref
api_name:
- force_allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9c82e1665e4c49461c3c7bd1c315b31f4f72c7e3f0e5331d9f0326347d36105
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582161"
---
# <a name="force_allocate-attribute"></a>Attributo force \_ allocate

L'attributo ACF force allocate forza l'allocazione di un parametro puntatore usando midl user allocate invece di \[ **\_** \] ottimizzare [**\_ \_**](midl-user-allocate-1.md) l'allocazione.

``` syntax
[ [function-attribute-list <>] ] type-specifier <> [pointer- <>declarator <>] function-name <>( [ force_allocate [ , parameter-attribute-list <> ] ] type-specifier <> [declarator <>] , ...);
```

## <a name="parameters"></a>Parametri

Questo attributo non ha parametri.

## <a name="remarks"></a>Commenti

RPC tenta di ridurre al minimo le allocazioni di memoria nel server fornendo puntatori ai buffer di memoria interni. Questo approccio può causare problemi per le applicazioni che tentano di chiamare direttamente [**midl \_ user \_ free**](midl-user-free-1.md) sui puntatori forniti da RPC, perché non è possibile liberare un puntatore ottimizzato. Contrassegnare un parametro con **\[ force \_ allocate \]** impedirà questa ottimizzazione per tutti i puntatori che lo derivano.

Un altro uso comune di **\[ force \_ allocate \]** è garantire l'allineamento della memoria a cui punta se un'applicazione richiede un allineamento maggiore di quello della memoria a cui punta. Ad esempio, le applicazioni passano spesso i dati in una matrice generica di byte anziché usare il tipo effettivo, ma è garantito che un byte sia allineato solo a 1, il che può causare problemi per le applicazioni che presuppongono un allineamento maggiore. Contrassegnando il parametro con **\[ force \_ \] allocate,** l'applicazione può garantire che tutta la memoria a cui punta abbia un allineamento uguale a quello garantito da [**midl user \_ \_ allocate.**](midl-user-allocate-1.md)

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

[Evitare di nascondere le informazioni](/windows/desktop/WinProg64/avoiding-information-hiding)
</dt> <dt>

[Progettazione di interfacce compatibili a 64 bit](/windows/desktop/WinProg64/designing-64-bit-compatible-interfaces)
</dt> <dt>

[**midl \_ user \_ allocate**](midl-user-allocate-1.md)
</dt> <dt>

[**midl \_ user \_ free**](midl-user-free-1.md)
</dt> <dt>

[**Allocare**](allocate.md)
</dt> </dl>

 

 