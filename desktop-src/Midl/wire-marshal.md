---
title: wire_marshal (attributo)
description: L'attributo \ Wire \_ Marshal \ specifica un tipo di dati che verrà usato per la trasmissione (il tipo Wire) invece di un tipo di dati specifico dell'applicazione (User-Type).
ms.assetid: 51969f2c-7390-42c4-8aa6-ba12fdb22d23
keywords:
- attributo wire_marshal MIDL
topic_type:
- apiref
api_name:
- wire_marshal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17466648078162bc8244219f77e3ecc0dc4cb4d7
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "104399851"
---
# <a name="wire_marshal-attribute"></a>\_attributo Wire Marshal

L'attributo **\[ Wire \_ Marshal \]** specifica un tipo di dati che verrà usato per la trasmissione (il *tipo Wire*) invece di un tipo di dati specifico dell'applicazione ( *User-Type*).

``` syntax
typedef [wire_marshal(wire_type)] type-specifier userm-type; 
unsigned long __RPC_USER  < userm-type >_UserSize(
    unsigned long __RPC_FAR *pFlags,
    unsigned long StartingSize,
    < userm-type > __RPC_FAR * pUser_typeObject );
unsigned char __RPC_FAR * __RPC_USER  < userm-type >_UserMarshal(
    unsigned long  __RPC_FAR * pFlags,
    unsigned char __RPC_FAR * Buffer,
    < userm-type >  __RPC_FAR * pUser_typeObject);
unsigned char __RPC_FAR * __RPC_USER  < userm-type >_UserUnmarshal(
    unsigned long  __RPC_FAR *  pFlags,
    unsigned char __RPC_FAR *  Buffer,
    < userm-type > __RPC_FAR * pUser_typeObject);
void __RPC_USER  < userm-type >_UserFree(
    unsigned long  __RPC_FAR * pFlags,
    < userm-type >  __RPC_FAR * pUser_typeObject);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*tipo Wire* 
</dt> <dd>

Specifica il tipo di dati di trasferimento denominato effettivamente trasferito tra il client e il server. Il *tipo di collegamento* deve essere un tipo di base MIDL, un tipo predefinito o un identificatore di tipo di un tipo che può essere trasmesso attraverso la rete.

</dd> <dt>

*identificatore di tipo* 
</dt> <dd>

Tipo per il quale *UserY-Type* diventerà un alias.

</dd> <dt>

*utente-tipo* 
</dt> <dd>

Specifica l'identificatore del tipo di dati utente di cui effettuare il marshalling. Può trattarsi di qualsiasi tipo, come specificato da *Type-specifier*, purché disponga di una dimensione ben definita. Il *tipo di utente* non deve essere transmittable, ma deve essere un tipo noto al compilatore MIDL.

</dd> <dt>

*pFlags* 
</dt> <dd>

Specifica un puntatore a un campo del flag ( [**Long**](long.md) [**senza segno**](unsigned.md) ). La parola più significativa specifica i flag di rappresentazione dei dati NDR come definito da DCE per la rappresentazione a virgola mobile, Big o little-endian e character. La parola di ordine inferiore specifica un flag di contesto di marshalling. Il layout esatto dei flag viene descritto nella [funzione di tipo \_ UserSize](/windows/desktop/Rpc/the-type-usersize-function).

</dd> <dt>

*StartingSize* 
</dt> <dd>

Specifica la dimensione del buffer corrente (offset) prima di ridimensionare l'oggetto.

</dd> <dt>

*\_TypeObject Puser* 
</dt> <dd>

Specifica un puntatore a un oggetto di *tipo User \_ .*

</dd> <dt>

*Buffer* 
</dt> <dd>

Specifica il puntatore al buffer corrente.

</dd> </dl>

## <a name="remarks"></a>Commenti

Ogni tipo di dati specifico dell'applicazione, *User-Type,* presenta una corrispondenza uno-a-uno con un *tipo Wire* che definisce la rappresentazione in transito del tipo. È necessario specificare routine per dimensionare i dati per il marshalling, per effettuare il marshalling e l'unmarshalling dei dati e per liberare memoria. Si noti che se nei dati sono presenti tipi incorporati anch ' essi definiti con **\[ \_ marshalling \] di rete** o **\[** [**\_ marshalling dell'utente**](user-marshal.md) **\]** , è necessario gestire anche la manutenzione di tali tipi incorporati. Per ulteriori informazioni su queste routine, vedere [l'attributo Wire \_ Marshal](/windows/desktop/Rpc/the-wire-marshal-attribute).

L'implementazione deve seguire le regole di marshalling in base alla specifica OSF-DCE. Per informazioni dettagliate sulla sintassi di trasferimento del rapporto di recapito [https://www.opengroup.org/onlinepubs/9629399/chap14.htm](https://pubs.opengroup.org/onlinepubs/9629399/chap14.htm) , vedere. Se non si ha familiarità con il protocollo wire, non è consigliabile usare il **\[ \_ marshalling \] di rete** .

Il *tipo di collegamento* non può essere un puntatore di interfaccia o un puntatore completo. Il *tipo di Wire* deve avere una dimensione di memoria ben definita. Per informazioni dettagliate su come effettuare il marshalling di un determinato *tipo di Wire*, vedere [regole di marshalling per \_ marshalling degli utenti e \_ marshalling di rete](/windows/desktop/Rpc/marshaling-rules-for-user-marshal-and-wire-marshal) .

Il *tipo di utente* non deve essere un puntatore di interfaccia perché è possibile effettuare il marshalling direttamente. Se il tipo di utente è un puntatore completo, è necessario gestire manualmente l'alias.

Non è possibile usare l'attributo **\[ Wire \_ Marshal \]** con l' **\[** attributo [**allocate**](allocate.md) **\]** , direttamente o indirettamente, perché il motore NDR non controlla l'allocazione di memoria per il tipo trasmesso.

## <a name="examples"></a>Esempi

``` syntax
typedef unsigned long _FOUR_BYTE_DATA;

typedef struct _TWO_X_TWO_BYTE_DATA 
{
        unsigned short low;
        unsigned short high;
} TWO_X_TWO_BYTE_DATA;

typedef [wire_marshal(TWO_X_TWO_BYTE_DATA)] 
    _FOUR_BYTE_DATA FOUR_BYTE_DATA; 

//Marshaling functions:

// Calculate size that converted data will 
// require in the buffer
unsigned long __RPC_USER FOUR_BYTE_DATA_UserSize( 
    ULONG __RPC_FAR * pulFlags, 
    ULONG __RPC_FAR ulStartingSize,
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Copy FOUR_BYTE_DATA into buffer as 
// TWO_X_TWO_BYTE_DATA
unsigned long __RPC_USER FOUR_BYTE_DATA_UserMarshal( 
    ULONG __RPC_FAR *pulFlags, 
    char __RPC_FAR * pBufferStart, 
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Recreate FOUR_BYTE_DATA from TWO_X_TWO_BYTE_DATA in buffer
unsigned long __RPC_USER FOUR_BYTE_DATA_UserUnmarshal( 
    ULONG __RPC_FAR * pulFlags, 
    char __RPC_FAR * pBufferStart, 
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Nothing to do here as the engine frees the top 
// node and FOUR_BYTE_DATA is a flat data type.
void __RPC_USER FOUR_BYTE_DATA_UserFree( 
    ULONG __RPC_FAR * pulFlags, 
    FOUR_BYTE_DATA __RPC_FAR * pul 
    );
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**allocare**](allocate.md)
</dt> <dt>

[Rappresentazione dei dati](/windows/desktop/Rpc/data-representation)
</dt> <dt>

[Tipi di base MIDL](midl-base-types.md)
</dt> <dt>

[**long**](long.md)
</dt> <dt>

[**NdrGetUserMarshalInfo**](/windows/desktop/api/rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> <dt>

[Attributo Wire \_ Marshal](/windows/desktop/Rpc/the-wire-marshal-attribute)
</dt> <dt>

[**Trasmetti \_ come**](transmit-as.md)
</dt> <dt>

[**unsigned**](unsigned.md)
</dt> <dt>

[**\_marshalling utente**](user-marshal.md)
</dt> </dl>

 

 