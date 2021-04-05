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
# <a name="advertising-server-interfaces"></a><span data-ttu-id="db8ef-103">Interfacce server pubblicitarie</span><span class="sxs-lookup"><span data-stu-id="db8ef-103">Advertising Server Interfaces</span></span>

<span data-ttu-id="db8ef-104">Il lato server di un'applicazione che usa handle automatici deve chiamare la funzione [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) per rendere disponibili le informazioni di binding sul server ai client.</span><span class="sxs-lookup"><span data-stu-id="db8ef-104">The server side of an application that uses automatic handles must call the function [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) to make binding information about the server available to clients.</span></span> <span data-ttu-id="db8ef-105">Per gli handle di binding automatici è necessario un servizio dei nomi in esecuzione in un server accessibile al client.</span><span class="sxs-lookup"><span data-stu-id="db8ef-105">Automatic binding handles require a name service running on a server that is accessible to the client.</span></span> <span data-ttu-id="db8ef-106">L'implementazione Microsoft del nome Service, Microsoft Locator, gestisce gli handle automatici.</span><span class="sxs-lookup"><span data-stu-id="db8ef-106">The Microsoft implementation of the name service, Microsoft Locator, manages automatic handles.</span></span> <span data-ttu-id="db8ef-107">Le applicazioni server che utilizzano handle di binding impliciti ed espliciti possono inoltre annunciare la loro presenza nel database del servizio nome.</span><span class="sxs-lookup"><span data-stu-id="db8ef-107">Server applications that use implicit and explicit binding handles can also advertise their presence in the name service database.</span></span>

<span data-ttu-id="db8ef-108">In genere, il server chiama le funzioni di run-time seguenti:</span><span class="sxs-lookup"><span data-stu-id="db8ef-108">Typically, the server calls the following run-time functions:</span></span>

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

<span data-ttu-id="db8ef-109">Le chiamate alle prime due funzioni di questo frammento di codice sono simili all' [esempio Hello, World](tutorial.md).</span><span class="sxs-lookup"><span data-stu-id="db8ef-109">The calls to the first two functions in this code fragment are similar to the [Hello, World example](tutorial.md).</span></span> <span data-ttu-id="db8ef-110">Queste funzioni rendono disponibili informazioni sull'associazione disponibile al client.</span><span class="sxs-lookup"><span data-stu-id="db8ef-110">These functions make information about the binding available to the client.</span></span> <span data-ttu-id="db8ef-111">Le chiamate a [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) e [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) inseriscono le informazioni nel database del servizio del nome.</span><span class="sxs-lookup"><span data-stu-id="db8ef-111">The calls to [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) and [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) put the information in the name service database.</span></span> <span data-ttu-id="db8ef-112">La chiamata a [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) riempie il vettore di associazione con handle di binding validi prima che gli handle vengano esportati nel servizio del nome.</span><span class="sxs-lookup"><span data-stu-id="db8ef-112">The call to [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) fills the binding vector with valid binding handles before the handles are exported to the name service.</span></span> <span data-ttu-id="db8ef-113">Dopo che il programma server Esporta gli handle nel database, il client (o stub client) può chiamare [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) e [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext) per ottenere queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="db8ef-113">After the server program exports the handles to the database, the client (or client stubs) can call [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) and [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext) to obtain this information.</span></span> <span data-ttu-id="db8ef-114">Per informazioni dettagliate, vedere [ricerca di sistemi host server](finding-server-host-systems.md).</span><span class="sxs-lookup"><span data-stu-id="db8ef-114">For details, see [Finding Server Host Systems](finding-server-host-systems.md).</span></span>

<span data-ttu-id="db8ef-115">Le chiamate a [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) e [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) e alle strutture di dati associate sono simili alle seguenti:</span><span class="sxs-lookup"><span data-stu-id="db8ef-115">The calls to [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) and [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) and their associated data structures look similar to the following:</span></span>

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

<span data-ttu-id="db8ef-116">Si noti che il parametro [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) *pBindingVector* è un puntatore a un puntatore a un [**\_ \_ vettore di binding RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_binding_vector).</span><span class="sxs-lookup"><span data-stu-id="db8ef-116">Note that the [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) parameter *pBindingVector* is a pointer to a pointer to [**RPC\_BINDING\_VECTOR**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_binding_vector).</span></span> <span data-ttu-id="db8ef-117">Tenere inoltre presente che ogni chiamata a [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) deve essere seguita da una chiamata a [**RpcBindingVectorFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree).</span><span class="sxs-lookup"><span data-stu-id="db8ef-117">Also remember that each call to [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) must be followed by a call to [**RpcBindingVectorFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree).</span></span>

<span data-ttu-id="db8ef-118">Per rimuovere l'interfaccia esportata dal database del servizio dei nomi, il server chiama [**RpcNsBindingUnexport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexporta) come illustrato:</span><span class="sxs-lookup"><span data-stu-id="db8ef-118">To remove the exported interface from the name service database, the server calls [**RpcNsBindingUnexport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexporta) as shown:</span></span>

``` syntax
status = RpcNsBindingUnexport(
                fNameSyntaxType, 
                pszAutoEntryName,  
                auto_ServerIfHandle,
                NULL);              // unexport handles only
```

<span data-ttu-id="db8ef-119">La funzione [**RpcNsBindingUnexport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexporta) deve essere utilizzata solo quando il servizio è in fase di rimozione permanente.</span><span class="sxs-lookup"><span data-stu-id="db8ef-119">The [**RpcNsBindingUnexport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexporta) function should be used only when the service is being permanently removed.</span></span> <span data-ttu-id="db8ef-120">Non deve essere utilizzato quando il servizio è temporaneamente disabilitato, ad esempio quando il server viene arrestato per la manutenzione.</span><span class="sxs-lookup"><span data-stu-id="db8ef-120">It should not be used when the service is temporarily disabled, such as when the server is shut down for maintenance.</span></span> <span data-ttu-id="db8ef-121">Un programma server può registrarsi con il nome del database del servizio, ma non è disponibile perché il server è temporaneamente offline.</span><span class="sxs-lookup"><span data-stu-id="db8ef-121">A server program can register itself with the name service database, yet be unavailable because the server is temporarily offline.</span></span> <span data-ttu-id="db8ef-122">L'applicazione client deve contenere codice di gestione delle eccezioni per tale condizione.</span><span class="sxs-lookup"><span data-stu-id="db8ef-122">The client application should contain exception-handling code for such a condition.</span></span>

<span data-ttu-id="db8ef-123">Per ulteriori informazioni sul contenuto e il formato del database del servizio dei nomi, vedere [il database del servizio nome RPC](the-rpc-name-service-database.md).</span><span class="sxs-lookup"><span data-stu-id="db8ef-123">For more information on the content and format of the name service database, see [The RPC Name Service Database](the-rpc-name-service-database.md).</span></span>

<span data-ttu-id="db8ef-124">Le applicazioni possono utilizzare il servizio Active Directory se i programmi client e server sono in esecuzione in Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="db8ef-124">Applications can utilize the Active Directory service if both the client and server programs are running under Windows 2000.</span></span> <span data-ttu-id="db8ef-125">I computer che eseguono i programmi client e server devono essere entrambi membri di un dominio di Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="db8ef-125">The computers running the client and server programs must both be members of a Windows 2000 domain.</span></span>

<span data-ttu-id="db8ef-126">Per annunciare la propria presenza tramite il servizio Active Directory, il programma server deve essere eseguito nel contesto di sicurezza di un amministratore di dominio.</span><span class="sxs-lookup"><span data-stu-id="db8ef-126">To advertise its presence using the Active Directory service, the server program should run in the security context of a domain administrator.</span></span> <span data-ttu-id="db8ef-127">Se è in esecuzione nel contesto di utenti di dominio, un amministratore di dominio deve modificare l'elenco di controllo di accesso (ACL) nel contenitore dei servizi RPC.</span><span class="sxs-lookup"><span data-stu-id="db8ef-127">If it is running in the context of domain users, a domain administrator must modify the access control list (ACL) on the RPC Services container.</span></span> <span data-ttu-id="db8ef-128">Per ulteriori informazioni, vedere la documentazione Active Directory.</span><span class="sxs-lookup"><span data-stu-id="db8ef-128">For more information, see the Active Directory documentation.</span></span>

 

 




