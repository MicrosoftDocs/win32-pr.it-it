---
title: enable_allocate attributo
description: L'attributo \ enable \_ allocate\ ACF specifica che il codice stub del server deve abilitare l'ambiente di gestione della memoria stub.
ms.assetid: 3a232a82-f114-4d8c-8b71-cf8860c77db3
keywords:
- enable_allocate attributo MIDL
topic_type:
- apiref
api_name:
- enable_allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58f44b3a2f11094c37edf24f5fc00bbd8229d65dc2a54292acd2ca3221472e85
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979621"
---
# <a name="enable_allocate-attribute"></a>abilitare \_ l'attributo di allocazione

**\[ L'attributo enable \_ allocate \]** ACF specifica che il codice stub del server deve abilitare l'ambiente di gestione della memoria stub.

> [!Note]  
> **\[ L'attributo enable \_ allocate \]** è obsoleto e non è più supportato.

 

``` syntax
[
    enable_allocate
  [ , optional-attribute-list]
]
interface interface-name
{
    . . .
};
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*optional-attribute-list* 
</dt> <dd>

Specifica un elenco di zero o più attributi MIDL aggiuntivi.

</dd> <dt>

*interface-name* 
</dt> <dd>

Nome dell'interfaccia a cui verrà applicato **\[ l'attributo enable \_ \] allcoate.**

</dd> </dl>

## <a name="remarks"></a>Commenti

In modalità predefinita, lo stub del server abilita l'ambiente di memoria solo quando viene usato **\[ l'attributo \_ enable allocate. \]** L'ambiente di gestione della memoria deve essere abilitato prima di poter allocare memoria [**tramite RpcSmAllocate**](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmallocate). In **modalità osf** (quando si esegue la compilazione con l'opzione [**/osf),**](-osf.md) lo stub abilita automaticamente questo ambiente o su richiesta quando viene usato l'attributo **\[ enable \_ allocate. \]**

Lo stub sul lato client può essere sensibile all'ambiente di gestione della memoria **Rpcss.** Se viene eseguito uno stub client sensibile quando il pacchetto **Rpcss** è disabilitato, vengono chiamati gli allocatori/deallocatori utente predefiniti (ad esempio, [midl \_ user \_ allocate](/windows/desktop/Rpc/the-midl-user-allocate-function) /  [midl user \_ \_ free).](/windows/desktop/Rpc/the-midl-user-free-function) Se abilitato, il **pacchetto Rpcss** usa la coppia allocatore/deallocatore dal pacchetto. Nella modalità predefinita, il client è sensibile solo quando viene usato **\[ l'attributo enable \_ allocate. \]** In genere, lo stub lato client opera nell'ambiente disabilitato. In **modalità osf** (quando si esegue la compilazione con l'opzione [**/osf),**](-osf.md) il client è sempre sensibile all'ambiente di gestione della memoria **Rpcss** e pertanto l'attributo **\[ enable \_ allocate \]** non influisce sugli stub client.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[File di configurazione dell'applicazione (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[midl \_ user \_ allocate](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[midl \_ user \_ free](/windows/desktop/Rpc/the-midl-user-free-function)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[RpcSmDisableAllocate](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmdisableallocate)
</dt> <dt>

[RpcSmEnableAllocate](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmenableallocate)
</dt> <dt>

[RpcSmFree](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmfree)
</dt> </dl>

 

 