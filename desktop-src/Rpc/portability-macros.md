---
title: Macro di portabilità (RPC. h)
description: Gli strumenti RPC ottengono il modello, la chiamata e l'indipendenza della convenzione di denominazione associando i tipi di dati e i tipi restituiti dalla funzione nei file stub e nei file di intestazione generati con definizioni specifiche per ogni piattaforma.
ms.assetid: 94de1138-5a84-41d8-bf88-97f0ac630f5f
keywords:
- RPC macro di portabilità
topic_type:
- apiref
api_name:
- Portability Macros
api_location:
- Rpc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c184365496db7757524a12f1b0807c3c53e24b27
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/12/2021
ms.locfileid: "103968835"
---
# <a name="portability-macros"></a>Macro di portabilità

Gli strumenti RPC ottengono il modello, la chiamata e l'indipendenza della convenzione di denominazione associando i tipi di dati e i tipi restituiti dalla funzione nei file stub e nei file di intestazione generati con definizioni specifiche per ogni piattaforma. Queste definizioni di macro assicurano che tutti i tipi di dati e le funzioni che richiedono la designazione di **\_ \_ lontano** siano specificati come oggetti lontani.

Nella figura seguente sono illustrate le definizioni di macro che il compilatore MIDL applica alle chiamate di funzione tra i componenti RPC:

![Diagramma che mostra le definizioni delle macro MIDL si applica alle chiamate di funzione.](images/prog-a29.png)

Le macro RPC sono definite come segue.



| Definizione    | Descrizione                                                                                                                                         |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| \_\_\_API RPC  | Applicato alle chiamate effettuate dallo stub all'applicazione utente. Entrambe le funzioni si trovano nello stesso programma eseguibile.                                       |
| \_\_RPC \_ lontano  | Applicato alla definizione macro standard per i puntatori. Questa definizione di macro dovrebbe essere inclusa nella firma di tutte le funzioni fornite dall'utente. |
| \_\_\_Stub RPC | Applicato alle chiamate effettuate dalla libreria di Runtime allo stub. Queste chiamate possono essere considerate private.                                                 |
| \_\_\_utente RPC | Applicato alle chiamate effettuate dalla libreria di runtime all'applicazione utente. Che superano il limite tra una DLL e un'applicazione.                   |
| \_voce RPC    | Applicato alle chiamate effettuate dall'applicazione o dallo stub alla libreria di Runtime. Questa definizione di macro viene applicata a tutte le funzioni di runtime RPC.           |



 

Per eseguire correttamente il collegamento con le librerie di runtime, gli stub e le routine di supporto di Microsoft RPC, alcune funzioni fornite dall'utente devono includere anche queste macro nella definizione della funzione. Utilizzare l' **\_ \_ \_ API RPC** macro quando si definiscono le funzioni associate alla gestione della memoria, gli handle di associazione definiti dall'utente e l'attributo **trasmissione \_ come** e si utilizza l' **\_ \_ \_ utente** della macro RPC quando si definisce la routine di esecuzione del contesto associata all'handle di contesto. Specificare le funzioni come:

<dl> <dt>

<span id="__RPC_USER_midl_user_allocate_..._"></span><span id="__rpc_user_midl_user_allocate_..._"></span><span id="__RPC_USER_MIDL_USER_ALLOCATE_..._"></span>\_\_\_Allocare *utenti \_ MIDL* utente RPC \_ (...)
</dt> <dd></dd> <dt>

<span id="__RPC_USER_midl_user_free_..._"></span><span id="__rpc_user_midl_user_free_..._"></span><span id="__RPC_USER_MIDL_USER_FREE_..._"></span>\_\_Utente RPC utente \_ *MIDL \_* \_ gratuito (...)
</dt> <dd></dd> <dt>

<span id="__RPC_USER__handletype_bind_..._"></span><span id="__rpc_user__handletype_bind_..._"></span><span id="__RPC_USER__HANDLETYPE_BIND_..._"></span>\_\_\_Binding *HANDLETYPE* utente RPC \_ (...)
</dt> <dd></dd> <dt>

<span id="__RPC_USER_handletype_unbind_..._"></span><span id="__rpc_user_handletype_unbind_..._"></span><span id="__RPC_USER_HANDLETYPE_UNBIND_..._"></span>\_\_\_Disassociazione *HANDLETYPE* utente RPC \_ (...)
</dt> <dd></dd> <dt>

<span id="__RPC_USER_type_to_local"></span><span id="__rpc_user_type_to_local"></span><span id="__RPC_USER_TYPE_TO_LOCAL"></span>\_\_\_ *Tipo* di utente RPC \_ in \_ locale
</dt> <dd></dd> <dt>

<span id="__RPC_USER_type_from_local"></span><span id="__rpc_user_type_from_local"></span><span id="__RPC_USER_TYPE_FROM_LOCAL"></span>\_\_\_ *Tipo* di utente RPC \_ da \_ locale
</dt> <dd></dd> <dt>

<span id="__RPC_USER_type_to_xmit_..._"></span><span id="__rpc_user_type_to_xmit_..._"></span><span id="__RPC_USER_TYPE_TO_XMIT_..._"></span>\_\_\_Tipo di utente RPC \_ in \_ Xmit (...)
</dt> <dd></dd> <dt>

<span id="__RPC_USER_type_from_xmit_..._"></span><span id="__rpc_user_type_from_xmit_..._"></span><span id="__RPC_USER_TYPE_FROM_XMIT_..._"></span>\_\_\_ *Tipo* di utente RPC \_ da \_ Xmit (...)
</dt> <dd></dd> <dt>

<span id="__RPC_USER_type_free_local"></span><span id="__rpc_user_type_free_local"></span><span id="__RPC_USER_TYPE_FREE_LOCAL"></span>\_\_\_ *Tipo* di utente RPC \_ disponibile \_ locale
</dt> <dd></dd> <dt>

<span id="__RPC_USER_type_free_inst_..._"></span><span id="__rpc_user_type_free_inst_..._"></span><span id="__RPC_USER_TYPE_FREE_INST_..._"></span>\_\_\_ *Tipo* di utente RPC \_ \_ (...)
</dt> <dd></dd> <dt>

<span id="__RPC_USER_type_free_xmit_..._"></span><span id="__rpc_user_type_free_xmit_..._"></span><span id="__RPC_USER_TYPE_FREE_XMIT_..._"></span>\_\_\_ *Tipo* di utente RPC \_ \_ Xmit gratuito (...)
</dt> <dd></dd> <dt>

<span id="__RPC_USER_context_rundown_..._"></span><span id="__rpc_user_context_rundown_..._"></span><span id="__RPC_USER_CONTEXT_RUNDOWN_..._"></span>\_\_\_Rundown del contesto utente RPC \_ (...)
</dt> <dd></dd> </dl>

> [!Note]  
> Tutti i parametri del puntatore in queste funzioni devono essere specificati utilizzando la macro **\_ \_ RPC \_ per** intero.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>RPC. h</dt> </dl> |



 

 





