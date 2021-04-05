---
title: handle (attributo)
description: L'attributo \ handle \ specifica un oggetto definito dall'utente o \ 0034; personalizzato \ 0034; tipo di handle.
ms.assetid: db5c6ea6-6081-4cea-9265-5e2f67fd8c14
keywords:
- Gestisci attributo MIDL
topic_type:
- apiref
api_name:
- handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d4560de53bf3f24238e9ff96e01c74716729749
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872517"
---
# <a name="handle-attribute"></a>handle (attributo)

L' \[ attributo **handle** \] specifica un tipo di handle definito dall'utente o personalizzato.

``` syntax
typedef [handle] typename;  
handle_t __RPC_USER typename_bind (typename);
void __RPC_USER typename_unbind (typename, handle_t);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*typeName* 
</dt> <dd>

Specifica il nome del tipo di handle di binding definito dall'utente.

</dd> </dl>

## <a name="remarks"></a>Commenti

Gli handle definiti dall'utente consentono agli sviluppatori di progettare handle significativi per l'applicazione. Un handle definito dall'utente può essere definito solo in una dichiarazione di tipo, non in un dichiaratore di funzione.

Un parametro di un tipo definito dall'attributo \[ **handle** \] viene utilizzato per determinare l'associazione per la chiamata e viene trasmesso alla routine chiamata.

L'utente deve fornire routine di binding e di annullamento dell'associazione per eseguire la conversione tra tipi primitivi e di handle definiti dall'utente. Dato un handle definito dall'utente di tipo *typeName*, l'utente deve fornire le routine *typeName* \_ **Bind** e *typeName* \_ **UNBIND**. Se, ad esempio, il tipo di handle definito dall'utente è denominato HANDLE, le routine sono denominate HANDLE \_ **Bind** e handler \_ **UNBIND**.

In caso di esito positivo, la  \_ routine **Bind** typeName deve restituire un handle di associazione primitivo valido. Se ha esito negativo, la routine deve restituire un **valore null**. Se la routine restituisce **null**, la routine *typeName* \_ **UNBIND** non verrà chiamata. Se la routine di associazione restituisce un handle di binding non valido diverso da **null**, il comportamento dello stub non è definito.

Quando la procedura remota dispone di un handle definito dall'utente come parametro o come handle implicito, gli stub client chiamano la routine di associazione prima di chiamare la procedura remota. Gli stub client chiamano la routine unbinding dopo la chiamata remota.

In DCE IDL, un parametro con l' \[ attributo **handle** \] deve apparire come primo parametro nell'elenco di argomenti della procedura remota. I parametri successivi, inclusi altri attributi dell' \[ **handle** \] , vengono trattati come parametri normali. Microsoft supporta un'estensione di DCE IDL che consente la visualizzazione del parametro dell'handle definito dall'utente \[  \] in posizioni diverse dal primo parametro.

## <a name="examples"></a>Esempi

``` syntax
typedef [handle] struct 
{ 
    char machine[8]; 
    char nmpipe[256]; 
} h_service; 
 
handle_t __RPC_USER h_service_bind(h_service); 
void __RPC_USER h_service_unbind(h_service, handle_t);
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Binding e handle](/windows/desktop/Rpc/binding-and-handles)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**handle implicito \_**](implicit-handle.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> </dl>

 

 