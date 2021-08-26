---
title: Interfacce del server pubblicitario
description: Il lato server di un'applicazione che usa handle automatici deve chiamare la funzione RpcNsBindingExport per rendere disponibili ai client le informazioni di associazione sul server.
ms.assetid: d15fd8da-3afd-4031-95d1-b76a0ad9a20d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1f81ec4b494c9ce2abd18031e3bf0ed3dd25d55908238ebc7bba96bce57e88f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073601"
---
# <a name="advertising-server-interfaces"></a>Interfacce del server pubblicitario

Il lato server di un'applicazione che usa handle automatici deve chiamare la funzione [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) per rendere disponibili ai client le informazioni di associazione sul server. Gli handle di associazione automatici richiedono un servizio dei nomi in esecuzione in un server accessibile al client. L'implementazione Microsoft del servizio dei nomi, Microsoft Locator, gestisce gli handle automatici. Anche le applicazioni server che usano handle di associazione impliciti ed espliciti possono annunciare la propria presenza nel database del servizio dei nomi.

In genere, il server chiama le funzioni di run-time seguenti:

``` syntax
/* auto handle server application (fragment) */
 
//interface header file that the MIDL compiler generates
#include "auto.h" 
 
void main(void)
{
    RpcUseProtseqEp(...);
    RpcServerRegisterIf(...);
    RpcServerInqBindings(...);
    RpcNsBindingExport(...);
    ...
}
```

Le chiamate alle prime due funzioni in questo frammento di codice sono simili [all'esempio Hello, World](tutorial.md). Queste funzioni rendono disponibili al client informazioni sull'associazione. Le chiamate a [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) e [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) hanno inserito le informazioni nel database del servizio dei nomi. La chiamata a [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) riempie il vettore di associazione con handle di associazione validi prima che gli handle siano esportati nel servizio dei nomi. Dopo che il programma server ha esportato gli handle nel database, il client (o stub client) può chiamare [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) e [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext) per ottenere queste informazioni. Per informazioni dettagliate, vedere [Ricerca di sistemi host server](finding-server-host-systems.md).

Le chiamate a [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) e [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) e alle strutture di dati associate sono simili alle seguenti:

``` syntax
RPC_BINDING_VECTOR * pBindingVector;
RPCSTATUS status;
 
status = RpcServerInqBindings(&pBindingVector);
 
status = RpcNsBindingExport(
                fNameSyntaxType,      // name syntax type 
                pszAutoEntryName,     // nsi entry name 
                autoh_ServerIfHandle, // if server handle
                pBindingVector,       // set in previous call 
                NULL);                // UUID vector
```

Si noti che [**il parametro RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) *pBindingVector* è un puntatore a un puntatore a [**RPC BINDING \_ \_ VECTOR**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_binding_vector). Tenere inoltre presente che ogni chiamata a [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) deve essere seguita da una chiamata a [**RpcBindingVectorFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree).

Per rimuovere l'interfaccia esportata dal database del servizio dei nomi, il server chiama [**RpcNsBindingUnexport,**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexporta) come illustrato di seguito:

``` syntax
status = RpcNsBindingUnexport(
                fNameSyntaxType, 
                pszAutoEntryName,  
                auto_ServerIfHandle,
                NULL);              // unexport handles only
```

La [**funzione RpcNsBindingUnexport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexporta) deve essere usata solo quando il servizio viene rimosso definitivamente. Non deve essere usato quando il servizio è temporaneamente disabilitato, ad esempio quando il server viene arrestato per la manutenzione. Un programma server può registrarsi con il database del servizio dei nomi, ma non essere disponibile perché il server è temporaneamente offline. L'applicazione client deve contenere codice di gestione delle eccezioni per una condizione di questo tipo.

Per altre informazioni sul contenuto e sul formato del database del servizio nomi, vedere Database del servizio nomi [RPC](the-rpc-name-service-database.md).

Le applicazioni possono utilizzare il servizio Active Directory se i programmi client e server vengono eseguiti in Windows 2000. I computer che eseguono i programmi client e server devono essere entrambi membri di un Windows 2000.

Per annunciarne la presenza tramite il servizio Active Directory, il programma server deve essere eseguito nel contesto di sicurezza di un amministratore di dominio. Se è in esecuzione nel contesto degli utenti di dominio, un amministratore di dominio deve modificare l'elenco di controllo di accesso (ACL) nel contenitore servizi RPC. Per altre informazioni, vedere la documentazione di Active Directory.

 

 




