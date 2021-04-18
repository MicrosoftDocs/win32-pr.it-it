---
title: local (attributo)
description: L'attributo \ Local \ specifica al compilatore MIDL che un'interfaccia o una funzione non è remota.
ms.assetid: 17ad3d87-4ca4-4e9b-91bc-280c03830f54
keywords:
- attributo locale MIDL
topic_type:
- apiref
api_name:
- local
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a40b1842bf637d3b7fcaab7a0c13319def1d1663
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299079"
---
# <a name="local-attribute"></a>local (attributo)

L'attributo **\[ Local \]** specifica al compilatore MIDL che un'interfaccia o una funzione non è remota.

``` syntax
[ 
    local 
    [, interface-attribute-list] 
] 
interface interface-name
{
}

[ 
    object, 
    uuid(string-uuid), 
    local [, interface-attribute-list] 
]
interface interface-name
{
}

[ local [, function-attribute-list] ] function-declarator ;
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*Interface-Attribute-List* 
</dt> <dd>

Specifica altri attributi che si applicano all'interfaccia nel suo complesso. Gli attributi **\[** [**endpoint**](endpoint.md) **\]** , **\[** [**Version**](version.md) **\]** e **\[** [**pointer \_ default**](pointer-default.md) **\]** sono facoltativi. Quando si esegue la compilazione con l'opzione di [**\_ configurazione/app**](-app-config.md) , è possibile che sia presente anche un handle **\[** [**implicito \_**](implicit-handle.md) **\]** o un **\[** [**\_ handle automatico**](auto-handle.md) **\]** . Separare più attributi con virgole.

</dd> <dt>

*Nome interfaccia* 
</dt> <dd>

Specifica il nome in base al quale i componenti software possono delineare l'interfaccia.

</dd> <dt>

*stringa-UUID* 
</dt> <dd>

Specifica una stringa UUID generata dall'utilità uuidgen. Se non si usa l'opzione del compilatore MIDL [**/OSF**](-osf.md), è possibile racchiudere la stringa UUID tra virgolette.

</dd> <dt>

*Function-Attribute-List* 
</dt> <dd>

Specifica zero o più attributi che si applicano alla funzione. Gli attributi di funzione validi sono **\[** [**callback**](callback.md), **\]** l'attributo Pointer **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** e gli attributi Usage **\[** [**String**](string.md) **\]** , **\[** [**Ignore**](ignore.md) **\]** e **\[** [**Context \_ handle**](context-handle.md) **\]** . Separare più attributi con virgole.

</dd> <dt>

*Function-dichiaratore* 
</dt> <dd>

Specifica l'identificatore di tipo, il nome della funzione e l'elenco di parametri per la funzione.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'attributo **\[ Local \]** può essere applicato a singole funzioni o all'interfaccia nel suo complesso.

Quando viene usato nell'intestazione dell'interfaccia, l'attributo **\[ Local \]** consente di usare il compilatore MIDL come generatore di intestazioni. Il compilatore non genera stub per le funzioni e non garantisce che l'intestazione possa essere trasmessa.

Per un'interfaccia RPC, l'attributo **\[ Local \]** non può essere utilizzato contemporaneamente all' **\[** attributo [**UUID**](uuid.md) **\]** . È necessario che **\[ UUID \]** o **\[ Local \]** sia presente nell'intestazione di interfaccia e che quello scelto venga eseguito esattamente una volta.

Per un'interfaccia COM (identificata dall' **\[** [](object.md) **\]** attributo dell'interfaccia oggetto), l'elenco di attributi di interfaccia può includere l'attributo **\[ locale \]** anche se **\[** [](uuid.md) **\]** è presente l'attributo uuid.

Quando viene usata in una singola funzione, l'attributo **\[ locale \]** definisce una procedura locale per la quale non vengono generati stub. L'uso di **\[ Local \]** come attributo di funzione è un'estensione Microsoft per DCE IDL. Pertanto, questo attributo non è disponibile quando si esegue la compilazione utilizzando l'opzione MIDL [**/OSF**](-osf.md) .

Si noti che un'interfaccia senza attributi può essere importata in un file IDL di base. Tuttavia, l'interfaccia deve contenere solo tipi di oggetto senza procedure. Se nell'interfaccia è inclusa anche una routine, è necessario specificare un attributo local o UUID.

## <a name="examples"></a>Esempi

``` syntax
/* IDL file #1 */ 
[
    local
] 
interface local_procs 
{ 
    void MyLocalProc(void);
} 
 
/* IDL file #2 */ 
[
    object, 
    uuid(12345678-1234-1234-123456789ABC), 
    local
] 
interface local_object_procs : IUnknown
{ 
    void MyLocalObjectProc(void);
} 
 
/* IDL file #3 */ 
[
    uuid(87654321-1234-1234-123456789ABC)
] 
interface mixed_procs 
{ 
    [local] void MyLocalProc(void); 
    HRESULT MyRemoteProc([in] short sParam); 
}
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**configurazione di/app \_**](-app-config.md)
</dt> <dt>

[**\_handle automatico**](auto-handle.md)
</dt> <dt>

[**callback**](callback.md)
</dt> <dt>

[**handle di contesto \_**](context-handle.md)
</dt> <dt>

[**endpoint**](endpoint.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**ignorare**](ignore.md)
</dt> <dt>

[**handle implicito \_**](implicit-handle.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**oggetto**](object.md)
</dt> <dt>

[**puntatore \_ predefinito**](pointer-default.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**string**](string.md)
</dt> <dt>

[**unico**](unique.md)
</dt> <dt>

[**uuid**](uuid.md)
</dt> <dt>

[**Versione**](version.md)
</dt> </dl>

 

 




