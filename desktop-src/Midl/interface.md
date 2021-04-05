---
title: interface (attributo)
description: La parola chiave Interface specifica il nome dell'interfaccia. Il nome dell'interfaccia deve essere specificato sia nel file IDL che nell'ACF.
ms.assetid: 239b782e-57de-493c-b2f4-310d1859a9ae
keywords:
- attributo di interfaccia MIDL
topic_type:
- apiref
api_name:
- interface
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 852c29b2ba7b43e9d8b15863e60db8ad2fbde33f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872385"
---
# <a name="interface-attribute"></a>interface (attributo)

La parola chiave **Interface** specifica il nome dell'interfaccia. Il nome dell'interfaccia deve essere specificato sia nel file IDL che nell'ACF.

``` syntax
[ 
    interface-attribute-list 
] 
interface interface-name [ : base-interface ]
{
}

typedef interface interface-name declarator-list
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*Interface-Attribute-List* 
</dt> <dd>

Specifica gli attributi che si applicano all'interfaccia nel suo complesso. Gli attributi di interfaccia validi per un file IDL includono **\[** [**endpoint**](endpoint.md) **\]** , **\[** [**local**](local.md) **\]** , **\[** [**Object**](object.md) **\]** , **\[** [**pointer \_ default**](pointer-default.md) **\]** , **\[** [**UUID**](uuid.md) **\]** e **\[** [**Version**](version.md) **\]** . Gli attributi di interfaccia validi per un ACF includono **\[** [**Encode**](encode.md), **\]** **\[** [**Decode**](decode.md) **\]** , **\[** [**\_ handle automatico**](auto-handle.md) **\]** o **\[** [**\_ handle implicito**](implicit-handle.md) **\]** e **\[** [**codice**](code.md) **\]** o **\[** [**NoCode**](nocode.md) **\]** .

</dd> <dt>

*Nome interfaccia* 
</dt> <dd>

Specifica il nome dell'interfaccia. Il nome dell'interfaccia deve essere un nome univoco e deve iniziare con un carattere alfabetico o di sottolineatura.

</dd> <dt>

*interfaccia di base* 
</dt> <dd>

Specifica il nome di un'interfaccia da cui questa interfaccia derivata eredita le funzioni membro, i codici di stato e gli attributi di interfaccia. L'interfaccia derivata non eredita le definizioni dei tipi. A tale scopo, usare la parola chiave [**Import**](import.md) per importare il file IDL dell'interfaccia di base.

</dd> <dt>

*elenco di dichiaratori* 
</dt> <dd>

Specifica i dichiaratori C standard, ad esempio identificatori, dichiaratori di puntatore e dichiaratori di matrici. Per altre informazioni, vedere [attributi array e Sized-Pointer](array-and-sized-pointer-attributes.md), [**matrici**](arrays-1.md)e [matrici e puntatori](/windows/desktop/Rpc/arrays-and-pointers). Il *declarator-list* è costituito da uno o più dichiaratori, separati da virgole.

</dd> </dl>

## <a name="remarks"></a>Commenti

I nomi di interfaccia nel file IDL e ACF devono essere uguali, tranne quando si usa l'opzione del compilatore MIDL [**/ACF**](-acf.md).

Il nome dell'interfaccia costituisce la prima parte del nome delle strutture di dati di gestione dell'interfaccia che sono parametri per le funzioni di runtime RPC. Per ulteriori informazioni, vedere [**RPC \_ if \_ handle**](/windows/desktop/Rpc/rpc-if-handle).

Se l'intestazione dell'interfaccia include l'attributo dell' **\[** [**oggetto**](object.md) **\]** per indicare un'interfaccia com, deve includere anche l' **\[** [](uuid.md) **\]** attributo uuid ed è necessario specificare l'interfaccia com di base da cui è derivata. Per ulteriori informazioni sulle interfacce COM, vedere **\[** [**oggetto**](object.md) **\]** .

È anche possibile usare la parola chiave **Interface** con la parola chiave [**typedef**](typedef.md) per definire un tipo di dati dell'interfaccia.

## <a name="examples"></a>Esempi

``` syntax
/* use of interface keyword in IDL file for an RPC interface */ 
[ 
    uuid (00000000-0000-0000-0000-000000000000), 
    version (1.0) 
] 
interface remote_if_2 
{  
    // Interface definition statements.
} 
 
/* use of interface keyword in ACF for an RPC interface */ 
[
    implicit_handle( handle_t xa_bhandle ) 
] 
interface remote_if_2 
{ 
    // Attribute configuration statements.
} 
 
/* use of interface keyword in IDL file for a COM interface */ 
[ 
    object, uuid (00000000-0000-0000-0000-000000000000) 
] 
interface IDerivedInterface : IBaseInterface 
{  
    import "base.idl" 
    Save(); 
} 
 
/* use of interface keyword to define an interface pointer type */ 
typedef interface IStorage *LPSTORAGE;
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[File di configurazione dell'applicazione (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**endpoint**](endpoint.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**locale**](local.md)
</dt> <dt>

[**oggetto**](object.md)
</dt> <dt>

[**puntatore \_ predefinito**](pointer-default.md)
</dt> <dt>

[**\_gestore RPC if \_**](/windows/desktop/Rpc/rpc-if-handle)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**uuid**](uuid.md)
</dt> <dt>

[**Versione**](version.md)
</dt> </dl>

 

 