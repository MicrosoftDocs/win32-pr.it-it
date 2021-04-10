---
title: Async (attributo)
description: L'attributo \ Async \ ACF definisce una chiamata di procedura remota come operazione asincrona.
ms.assetid: 8002980a-94be-4d45-99d7-dfa4eae7f102
keywords:
- MIDL dell'attributo asincrono
topic_type:
- apiref
api_name:
- async
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 562b157f26078c6f4d5b3cffe47417fa18fe608d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103956415"
---
# <a name="async-attribute"></a>Async (attributo)

L' \[ attributo **asincrono** \] ACF definisce una chiamata di procedura remota come operazione asincrona.

``` syntax
[async, opt-acf-attributes] function-name (param-list)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*opz-ACF-attributi* 
</dt> <dd>

Specifica gli attributi facoltativi di configurazione dell'applicazione.

</dd> <dt>

*Nome funzione* 
</dt> <dd>

Specifica il nome della funzione nel file IDL.

</dd> <dt>

*param-list* 
</dt> <dd>

Specifica un elenco di parametri facoltativo.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo attributo non è applicabile nelle interfacce COM.

Per dichiarare una funzione RPC come asincrona, dichiarare prima la funzione come parte della definizione di un'interfaccia in un file IDL. Modificare quindi la dichiarazione di funzione, all'interno del file di configurazione dell'applicazione (ACF), applicando l' \[  \] attributo Async. Si noti che la dichiarazione di funzione non fa menzione dell'handle asincrono e che l'handle di associazione è il primo parametro. L'applicazione dell' \[ attributo **Async** \] nel file ACF genera il codice appropriato in modo che quando viene chiamata questa funzione, il server asincrono prevede di ricevere un handle asincrono prima degli altri parametri.

> [!Note]  
> L'attributo Async non può essere usato con l'opzione della riga di comando [**/OSF**](-osf.md) .

 

## <a name="examples"></a>Esempi

``` syntax
//file:Xasync.idl
interface AsyncIface 
{
    HRESULT MyAsyncFunc (
        handle_t hBinding,
        [in] int a,
        [in] int b,
        [out] int *c) ;
//other interface definitions
}
//end XAsync.idl

// file: Xasync.acf
interface AsyncIface
{
    [async] MyAsyncFunc () ;
    //any other ACF definitions
}
//end Xasync.acf
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[File di configurazione dell'applicazione (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[RPC asincrona](/windows/desktop/Rpc/asynchronous-rpc)
</dt> </dl>

 

 