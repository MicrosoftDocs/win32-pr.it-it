---
title: attributo enable_allocate
description: L'attributo \ enable \_ allocate \ ACF specifica che il codice stub del server deve abilitare l'ambiente di gestione della memoria stub.
ms.assetid: 3a232a82-f114-4d8c-8b71-cf8860c77db3
keywords:
- attributo enable_allocate MIDL
topic_type:
- apiref
api_name:
- enable_allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f43e8c10592fcf99ea294327c400c579ce45bf6b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104117615"
---
# <a name="enable_allocate-attribute"></a>Abilita \_ attributo allocate

L'attributo **\[ enable \_ allocate \]** ACF specifica che il codice stub del server deve abilitare l'ambiente di gestione della memoria stub.

> [!Note]  
> L'attributo **\[ enable \_ allocate \]** è obsoleto e non è più supportato.

 

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

*facoltativo-Attribute-List* 
</dt> <dd>

Specifica un elenco di zero o più attributi MIDL aggiuntivi.

</dd> <dt>

*Nome interfaccia* 
</dt> <dd>

Nome dell'interfaccia a cui verrà applicato l'attributo **\[ enable \_ allcoate \]** .

</dd> </dl>

## <a name="remarks"></a>Commenti

In modalità predefinita, lo stub del server Abilita l'ambiente di memoria solo quando viene usato l'attributo **\[ enable \_ allocate \]** . Per poter allocare memoria tramite [**RpcSmAllocate**](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmallocate), è necessario abilitare l'ambiente di gestione della memoria. In modalità **OSF** (quando si esegue la compilazione con l'opzione [**/OSF**](-osf.md) ), lo stub Abilita automaticamente questo ambiente o su richiesta quando viene usato l'attributo **\[ enable \_ allocate \]** .

Lo stub lato client può essere sensibile all'ambiente di gestione della memoria **RPCSS** . Se viene eseguito uno stub client sensibile quando il pacchetto **RPCSS** è disabilitato, vengono chiamati gli allocatori/deallocatori utente predefiniti, ad esempio [MIDL \_ User \_ Alloch](/windows/desktop/Rpc/the-midl-user-allocate-function) /  [MIDL \_ User \_ Free](/windows/desktop/Rpc/the-midl-user-free-function). Se abilitata, il pacchetto **RPCSS** utilizza la coppia allocatore/deallocatore del pacchetto. Nella modalità predefinita, il client è sensibile solo quando viene utilizzato l'attributo **\[ enable \_ allocate \]** . In genere, lo stub lato client opera nell'ambiente disabilitato. In modalità **OSF** (quando si esegue la compilazione con l'opzione [**/OSF**](-osf.md) ), il client è sempre sensibile all'ambiente di gestione della memoria **RPCSS** e, di conseguenza, l'attributo **\[ enable \_ allocate \]** non influirà sugli stub client.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[File di configurazione dell'applicazione (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[\_alloca utente \_ MIDL](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[\_utente MIDL \_ gratuito](/windows/desktop/Rpc/the-midl-user-free-function)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[RpcSmDisableAllocate](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmdisableallocate)
</dt> <dt>

[RpcSmEnableAllocate](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmenableallocate)
</dt> <dt>

[RpcSmFree](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmfree)
</dt> </dl>

 

 