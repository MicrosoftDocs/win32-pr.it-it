---
title: Interfacce server pubblicitarie
description: Il lato server di un'applicazione che usa handle automatici deve chiamare la funzione RpcNsBindingExport per rendere disponibili le informazioni di binding sul server ai client.
ms.assetid: d15fd8da-3afd-4031-95d1-b76a0ad9a20d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45955ac7228018d8ddebbc7c156031648091b6f3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044761"
---
# <a name="advertising-server-interfaces"></a>Interfacce server pubblicitarie

Il lato server di un'applicazione che usa handle automatici deve chiamare la funzione [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) per rendere disponibili le informazioni di binding sul server ai client. Per gli handle di binding automatici è necessario un servizio dei nomi in esecuzione in un server accessibile al client. L'implementazione Microsoft del nome Service, Microsoft Locator, gestisce gli handle automatici. Le applicazioni server che utilizzano handle di binding impliciti ed espliciti possono inoltre annunciare la loro presenza nel database del servizio nome.

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

Le chiamate alle prime due funzioni di questo frammento di codice sono simili all' [esempio Hello, World](tutorial.md). Queste funzioni rendono disponibili informazioni sull'associazione disponibile al client. Le chiamate a [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) e [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) inseriscono le informazioni nel database del servizio del nome. La chiamata a [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) riempie il vettore di associazione con handle di binding validi prima che gli handle vengano esportati nel servizio del nome. Dopo che il programma server Esporta gli handle nel database, il client (o stub client) può chiamare [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) e [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext) per ottenere queste informazioni. Per informazioni dettagliate, vedere [ricerca di sistemi host server](finding-server-host-systems.md).

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

Si noti che il parametro [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) *pBindingVector* è un puntatore a un puntatore a un [**\_ \_ vettore di binding RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_binding_vector). Tenere inoltre presente che ogni chiamata a [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) deve essere seguita da una chiamata a [**RpcBindingVectorFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree).

Per rimuovere l'interfaccia esportata dal database del servizio dei nomi, il server chiama [**RpcNsBindingUnexport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexporta) come illustrato:

``` syntax
status = RpcNsBindingUnexport(
                fNameSyntaxType, 
                pszAutoEntryName,  
                auto_ServerIfHandle,
                NULL);              // unexport handles only
```

La funzione [**RpcNsBindingUnexport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexporta) deve essere utilizzata solo quando il servizio è in fase di rimozione permanente. Non deve essere utilizzato quando il servizio è temporaneamente disabilitato, ad esempio quando il server viene arrestato per la manutenzione. Un programma server può registrarsi con il nome del database del servizio, ma non è disponibile perché il server è temporaneamente offline. L'applicazione client deve contenere codice di gestione delle eccezioni per tale condizione.

Per ulteriori informazioni sul contenuto e il formato del database del servizio dei nomi, vedere [il database del servizio nome RPC](the-rpc-name-service-database.md).

Le applicazioni possono utilizzare il servizio Active Directory se i programmi client e server sono in esecuzione in Windows 2000. I computer che eseguono i programmi client e server devono essere entrambi membri di un dominio di Windows 2000.

Per annunciare la propria presenza tramite il servizio Active Directory, il programma server deve essere eseguito nel contesto di sicurezza di un amministratore di dominio. Se è in esecuzione nel contesto di utenti di dominio, un amministratore di dominio deve modificare l'elenco di controllo di accesso (ACL) nel contenitore dei servizi RPC. Per ulteriori informazioni, vedere la documentazione Active Directory.

 

 




