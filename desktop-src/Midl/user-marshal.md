---
title: attributo user_marshal
description: L' \_ attributo ACF del marshalling dell'utente associa un tipo locale denominato al linguaggio di destinazione (User-Type) con un tipo di trasferimento (tipo Wire) che viene trasferito tra il client e il server.
ms.assetid: a2407aa3-574d-4690-8cdf-cb1c01ca8c49
keywords:
- attributo user_marshal MIDL
topic_type:
- apiref
api_name:
- user_marshal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5326c9390362193a1be9dc06ee3a57f174474cc2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337023"
---
# <a name="user_marshal-attribute"></a>\_attributo Marshal utente

L'attributo ACF del **\_ marshalling dell'utente** associa un tipo locale denominato al linguaggio di destinazione (*User-Type*) con un tipo di trasferimento (*tipo Wire*) che viene trasferito tra il client e il server.

``` syntax
typedef [user_marshal(userm_type)] wire-type; 
unsigned long __RPC_USER  < userm_type >_UserSize(
    unsigned long __RPC_FAR *pFlags,
    unsigned long StartingSize,
    < userm_type >  __RPC_FAR * pUser_typeObject );
unsigned char __RPC_FAR * __RPC_USER  < userm-type >_UserMarshal(
    unsigned long __RPC_FAR *pFlags,
    unsigned char __RPC_FAR * Buffer,
    < userm_type >  __RPC_FAR * pUser_typeObject);
unsigned char __RPC_FAR * __RPC_USER  < userm_type >_UserUnmarshal(
    unsigned long  __RPC_FAR *  pFlags,
    unsigned char __RPC_FAR *  Buffer,
    < userm_type >  __RPC_FAR * pUser_typeObject);
void __RPC_USER  < userm_type >_UserFree(
    unsigned long  __RPC_FAR * pFlags,
    < userm_type >  __RPC_FAR * pUser_typeObject);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*utente-tipo* 
</dt> <dd>

Specifica l'identificatore del tipo di dati utente di cui effettuare il marshalling. Il *tipo di utente* non deve essere trasmissibile e non deve essere un tipo noto al compilatore MIDL.

</dd> <dt>

*tipo Wire* 
</dt> <dd>

Specifica il tipo di dati di trasferimento denominato effettivamente trasferito tra il client e il server. Il tipo Wire deve essere un tipo di base MIDL, un tipo predefinito o un identificatore di tipo di un tipo che può essere trasmesso attraverso la rete.

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

Specifica un puntatore a un oggetto di *\_ tipo User*.

</dd> <dt>

*Buffer* 
</dt> <dd>

Specifica il puntatore al buffer corrente.

</dd> </dl>

## <a name="remarks"></a>Commenti

Ogni tipo locale denominato, *User-Type*, presenta una corrispondenza uno-a-uno con un *tipo Wire* che definisce la rappresentazione in transito del tipo. È necessario specificare routine per dimensionare i dati per il marshalling, per effettuare il marshalling e l'unmarshalling dei dati e per liberare memoria. Per ulteriori informazioni su queste routine, vedere [l' \_ attributo Marshal utente](/windows/desktop/Rpc/the-user-marshal-attribute). Si noti che se nei dati sono presenti tipi incorporati che sono definiti anche **con \_ marshalling utente** o \[ [**\[ \_ marshalling \] di rete**](wire-marshal.md), è necessario gestire anche la manutenzione di tali tipi incorporati.

Il *tipo di collegamento* non può essere un puntatore di interfaccia o un puntatore completo. Il *tipo di Wire* deve avere una dimensione di memoria ben definita. Per informazioni dettagliate su come effettuare il marshalling di un determinato *tipo di Wire*, vedere [regole di marshalling per \_ marshalling degli utenti e \_ marshalling di rete](/windows/desktop/Rpc/marshaling-rules-for-user-marshal-and-wire-marshal) .

Il *tipo di utente* non deve essere un puntatore di interfaccia perché è possibile effettuare il marshalling direttamente. Se il tipo di utente è un puntatore completo, è necessario gestire manualmente l'alias.

## <a name="examples"></a>Esempi

``` syntax
// Marshal a long as a structure containing two shorts.

typedef unsigned long FOUR_BYTE_DATA;
typedef struct _TWO_X_TWO_BYTE_DATA 
{ 
    unsigned short low; 
    unsigned short high; 
} TWO_X_TWO_BYTE_DATA;
```

``` syntax
// ACFL file

typedef [user_marshal(FOUR_BYTE_DATA)] TWO_X_TWO_BYTE_DATA;

// Marshaling functions:

// Calculate size that converted data will require in the buffer
unsigned long __RPC_USER FOUR_BYTE_DATA_UserSize( 
    ULONG __RPC_FAR * pulFlags, 
    ULONG __RPC_FAR ulStartingSize,
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Copy FOUR_BYTE_DATA into buffer as TWO_X_TWO_BYTE_DATA
unsigned long __RPC_USER FOUR_BYTE_DATA_UserMarshal( 
    ULONG __RPC_FAR *pulFlags, 
    char __RPC_FAR * pBufferStart, 
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Recreate FOUR_BYTE_DATA from TWO_X_TWO_BYTE_DATA in buffer
unsigned long __RPC_USER FOUR_BYTE_DATA_UserUnmarshal( 
    ULONG __RPC_FAR * pulFlags, 
    char __RPC_FAR * pBufferStart, 
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Nothing to do here as the engine frees the top node and FOUR_BYTE_DATA is a flat data type.
void __RPC_USER FOUR_BYTE_DATA_UserFree( 
    ULONG __RPC_FAR * pulFlags, 
    FOUR_BYTE_DATA __RPC_FAR * pul);
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[File di configurazione dell'applicazione (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[Tipi di base MIDL](midl-base-types.md)
</dt> <dt>

[**long**](long.md)
</dt> <dt>

[**rappresenta \_ come**](represent-as.md)
</dt> <dt>

[**unsigned**](unsigned.md)
</dt> <dt>

[\_Attributo Marshal utente](/windows/desktop/Rpc/the-user-marshal-attribute)
</dt> <dt>

[**\_marshalling di rete**](wire-marshal.md)
</dt> <dt>

[**NdrGetUserMarshalInfo**](/windows/desktop/api/rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> </dl>

 

 