---
title: user_marshal attributo
description: L'attributo ACF di marshalling utente associa un tipo locale denominato nella lingua di destinazione (userm-type) a un tipo di trasferimento (wire-type) trasferito tra client e \_ server.
ms.assetid: a2407aa3-574d-4690-8cdf-cb1c01ca8c49
keywords:
- user_marshal attributo MIDL
topic_type:
- apiref
api_name:
- user_marshal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f17b4ef9d4376309307403ee12e2c5aae507556beaf091f9d742998d18671a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105571"
---
# <a name="user_marshal-attribute"></a>attributo \_ di marshalling utente

**L'attributo \_** ACF di marshalling utente associa un tipo locale denominato nella lingua di destinazione (*userm-type*) a un tipo di trasferimento (*wire-type*) trasferito tra client e server.

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

*userm-type* 
</dt> <dd>

Specifica l'identificatore del tipo di dati utente di cui eseguire il marshalling. Il *tipo userm* non deve essere trasmissibile e non deve essere un tipo noto al compilatore MIDL.

</dd> <dt>

*wire-type* 
</dt> <dd>

Specifica il tipo di dati di trasferimento denominato effettivamente trasferito tra client e server. Il tipo wire deve essere un tipo di base MIDL, un tipo predefinito o un identificatore di tipo di un tipo che può essere trasmesso in rete.

</dd> <dt>

*pFlags* 
</dt> <dd>

Specifica un puntatore a un campo flag ( [**unsigned**](unsigned.md) [**long**](long.md)). La parola di ordine elevato specifica i flag di rappresentazione dei dati NDR come definito da DCE per la rappresentazione a virgola mobile, big-endian o little-endian e carattere. La parola di ordine basso specifica un flag di contesto di marshalling. Il layout esatto dei flag è descritto in [Funzione \_ UserSize di tipo](/windows/desktop/Rpc/the-type-usersize-function).

</dd> <dt>

*StartingSize* 
</dt> <dd>

Specifica le dimensioni correnti del buffer (offset) prima del ridimensionamento dell'oggetto.

</dd> <dt>

*pUser \_ typeObject* 
</dt> <dd>

Specifica un puntatore a un oggetto di *tipo userm \_*.

</dd> <dt>

*Buffer* 
</dt> <dd>

Specifica il puntatore al buffer corrente.

</dd> </dl>

## <a name="remarks"></a>Commenti

Ogni tipo locale denominato, *userm-type*, ha una corrispondenza *uno-a-uno* con un tipo wire che definisce la rappresentazione di cablare del tipo. È necessario fornire routine per ridimensionare i dati per il marshalling, effettuare il marshalling e l'unmarshal dei dati e liberare memoria. Per altre informazioni su queste routine, vedere [Attributo \_ di marshalling dell'utente](/windows/desktop/Rpc/the-user-marshal-attribute). Si noti che se nei dati sono presenti **tipi \_** incorporati definiti anche con il marshalling utente o il wire \[ [**\[ \_ marshal, \]**](wire-marshal.md)è necessario gestire anche la manutenzione di tali tipi incorporati.

*Wire-type non può* essere un puntatore a interfaccia o un puntatore completo. Il *wire-type* deve avere una dimensione di memoria ben definita. Per informazioni dettagliate su come effettuare il marshalling di un determinato tipo di rete, vedere Marshaling Rules for user marshal and wire marshal (Regole di marshalling per il marshalling utente e [ \_ wire \_ marshal).](/windows/desktop/Rpc/marshaling-rules-for-user-marshal-and-wire-marshal) 

*Userm-type* non deve essere un puntatore a interfaccia perché è possibile effettuare direttamente il marshalling di questi tipi. Se il tipo di utente è un puntatore completo, è necessario gestire l'aliasing manualmente.

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

[**rappresentano \_ come**](represent-as.md)
</dt> <dt>

[**Unsigned**](unsigned.md)
</dt> <dt>

[Attributo di \_ marshalling dell'utente](/windows/desktop/Rpc/the-user-marshal-attribute)
</dt> <dt>

[**wire \_ marshal**](wire-marshal.md)
</dt> <dt>

[**NdrGetUserMarshalInfo**](/windows/desktop/api/rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> </dl>

 

 