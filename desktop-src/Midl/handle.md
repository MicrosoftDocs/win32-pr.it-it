---
title: Attributo handle
description: L'attributo \ handle\ specifica un valore definito dall'utente o \ 0034;customized \ 0034; tipo di handle.
ms.assetid: db5c6ea6-6081-4cea-9265-5e2f67fd8c14
keywords:
- gestire l'attributo MIDL
topic_type:
- apiref
api_name:
- handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aacdb3611a12873a6e828c33606bb9c970747555c285f8612be2b43bc3f51adf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895291"
---
# <a name="handle-attribute"></a>Attributo handle

\[ **L'attributo** handle specifica un tipo di handle \] definito dall'utente o "personalizzato".

``` syntax
typedef [handle] typename;  
handle_t __RPC_USER typename_bind (typename);
void __RPC_USER typename_unbind (typename, handle_t);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*Typename* 
</dt> <dd>

Specifica il nome del tipo di handle di associazione definito dall'utente.

</dd> </dl>

## <a name="remarks"></a>Commenti

Gli handle definiti dall'utente consentono agli sviluppatori di progettare handle significativi per l'applicazione. Un handle definito dall'utente può essere definito solo in una dichiarazione di tipo, non in un dichiaratore di funzione.

Un parametro di un tipo definito dall'attributo handle viene usato per determinare l'associazione per la chiamata e viene trasmesso \[  \] alla routine chiamata.

L'utente deve fornire routine di associazione e annullamento dell'associazione per eseguire la conversione tra tipi di handle primitivi e definiti dall'utente. Dato un handle definito dall'utente di tipo *typename*, l'utente deve fornire le routine *typename* bind e \_  *typename* \_ **unbind**. Ad esempio, se il tipo di handle definito dall'utente è denominato MYHANDLE, le routine sono denominate MYHANDLE bind e \_  MYHANDLE \_ **unbind**.

In caso di esito positivo, la routine *di associazione* \_ **typename** deve restituire un handle di associazione primitiva valido. In caso di esito negativo, la routine deve restituire **un valore NULL.** Se la routine restituisce **NULL,** la routine  \_ **unbind typename** non verrà chiamata. Se la routine di associazione restituisce un handle di associazione non valido diverso da **NULL,** il comportamento dello stub non è definito.

Quando la procedura remota ha un handle definito dall'utente come parametro o come handle implicito, gli stub client chiamano la routine di associazione prima di chiamare la routine remota. Gli stub client chiamano la routine di annullamento dell'associazione dopo la chiamata remota.

In DCE IDL un parametro con l'attributo handle deve essere visualizzato \[  \] come primo parametro nell'elenco di argomenti della procedura remota. I parametri successivi, inclusi altri \[ **attributi di handle,** \] vengono trattati come parametri ordinari. Microsoft supporta un'estensione a DCE IDL che consente al parametro handle definito dall'utente di comparire in posizioni diverse \[  \] dal primo parametro.

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

[**handle \_ implicito**](implicit-handle.md)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> </dl>

 

 