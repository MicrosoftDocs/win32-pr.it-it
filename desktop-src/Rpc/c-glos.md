---
title: C (RPC)
description: Parole che iniziano con C nel Glossario RPC (Remote Procedure Call).
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: da1ee843-c33e-42a1-bcaf-6cdb4834e70b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f15eb37af87fd36dd31f3e9e106904b4ce734c15
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "103963696"
---
# <a name="c-rpc"></a><span data-ttu-id="403cc-103">C (RPC)</span><span class="sxs-lookup"><span data-stu-id="403cc-103">C (RPC)</span></span>

<span data-ttu-id="403cc-104">[A](a-glos.md) [B](b-glos.md) C [d](d-glos.md) [E](e-glos.md) [F](f-glos.md) G H [i](i-glos.md) J K [L](l-glos.md) [M](m-glos.md) [N](n-glos.md) [O](o-glos.md) [P](p-glos.md) [Q](q.md) [R](r-glos.md) [S](s-glos.md) [T](t-glos.md) [U](u-glos.md) [V](v-glos.md) [W](w-glos.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="403cc-104">[A](a-glos.md) [B](b-glos.md) C [D](d-glos.md) [E](e-glos.md) [F](f-glos.md) G H [I](i-glos.md) J K [L](l-glos.md) [M](m-glos.md) [N](n-glos.md) [O](o-glos.md) [P](p-glos.md) [Q](q.md) [R](r-glos.md) [S](s-glos.md) [T](t-glos.md) [U](u-glos.md) [V](v-glos.md) [W](w-glos.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="403cc-105"><span id="_rpc_cds_glos"></span><span id="_RPC_CDS_GLOS"></span>**Servizio directory celle (CDS)**</span><span class="sxs-lookup"><span data-stu-id="403cc-105"><span id="_rpc_cds_glos"></span><span id="_RPC_CDS_GLOS"></span>**Cell Directory Service (CDS)**</span></span>
</dt> <dd>

<span data-ttu-id="403cc-106">Nome-provider di servizi per l'ambiente di elaborazione distribuita di Open Software Foundation.</span><span class="sxs-lookup"><span data-stu-id="403cc-106">Name-service provider for the Open Software Foundation's Distributed Computing Environment.</span></span>

</dd> <dt>

<span data-ttu-id="403cc-107"><span id="_rpc_client_stub_glos"></span><span id="_RPC_CLIENT_STUB_GLOS"></span>**Stub client**</span><span class="sxs-lookup"><span data-stu-id="403cc-107"><span id="_rpc_client_stub_glos"></span><span id="_RPC_CLIENT_STUB_GLOS"></span>**client stub**</span></span>
</dt> <dd>

<span data-ttu-id="403cc-108">Codice sorgente del linguaggio C generato da MIDL.</span><span class="sxs-lookup"><span data-stu-id="403cc-108">MIDL-generated C-language source code.</span></span> <span data-ttu-id="403cc-109">Contiene tutte le funzioni necessarie affinché l'applicazione client effettui chiamate a procedure remote utilizzando il modello di una chiamata di funzione tradizionale in un'applicazione autonoma.</span><span class="sxs-lookup"><span data-stu-id="403cc-109">It contains all the functions necessary for the client application to make remote procedure calls using the model of a traditional function call in a standalone application.</span></span> <span data-ttu-id="403cc-110">Lo stub del client è responsabile del marshalling dei parametri di input e dell'unmarshalling dei parametri di output.</span><span class="sxs-lookup"><span data-stu-id="403cc-110">The client stub is responsible for marshaling input parameters and unmarshaling output parameters.</span></span> <span data-ttu-id="403cc-111">Vedere anche [*stub server*](s-glos.md), [*stub proxy*](p-glos.md).</span><span class="sxs-lookup"><span data-stu-id="403cc-111">See also [*server stub*](s-glos.md), [*proxy stub*](p-glos.md).</span></span>

</dd> <dt>

<span data-ttu-id="403cc-112"><span id="_rpc_conformant_array_glos"></span><span id="_RPC_CONFORMANT_ARRAY_GLOS"></span>**matrice conforme**</span><span class="sxs-lookup"><span data-stu-id="403cc-112"><span id="_rpc_conformant_array_glos"></span><span id="_RPC_CONFORMANT_ARRAY_GLOS"></span>**conformant array**</span></span>
</dt> <dd>

<span data-ttu-id="403cc-113">Matrice la cui dimensione viene determinata in fase di esecuzione da un altro parametro, da un campo della struttura o da un'espressione.</span><span class="sxs-lookup"><span data-stu-id="403cc-113">Array whose size is determined at run time by another parameter, structure field, or expression.</span></span>

</dd> <dt>

<span data-ttu-id="403cc-114"><span id="_rpc_connection_oriented_glos"></span><span id="_RPC_CONNECTION_ORIENTED_GLOS"></span>**orientato alla connessione**</span><span class="sxs-lookup"><span data-stu-id="403cc-114"><span id="_rpc_connection_oriented_glos"></span><span id="_RPC_CONNECTION_ORIENTED_GLOS"></span>**connection-oriented**</span></span>
</dt> <dd>

<span data-ttu-id="403cc-115">Protocollo di comunicazione o trasporto che fornisce un circuito virtuale attraverso il quale i pacchetti di dati vengono ricevuti nello stesso ordine in cui sono stati trasmessi.</span><span class="sxs-lookup"><span data-stu-id="403cc-115">Communications protocol or transport that provides a virtual circuit through which data packets are received in the same order as they were transmitted.</span></span> <span data-ttu-id="403cc-116">Se la connessione tra computer ha esito negativo, l'applicazione riceve una notifica.</span><span class="sxs-lookup"><span data-stu-id="403cc-116">If the connection between computers fails, the application is notified.</span></span> <span data-ttu-id="403cc-117">[*TCP*](t-glos.md) e [*SPX*](s-glos.md) sono esempi di protocolli orientati alla connessione.</span><span class="sxs-lookup"><span data-stu-id="403cc-117">[*TCP*](t-glos.md) and [*SPX*](s-glos.md) are examples of connection-oriented protocols.</span></span> <span data-ttu-id="403cc-118">Vedere anche [*datagramma*](d-glos.md).</span><span class="sxs-lookup"><span data-stu-id="403cc-118">See also [*datagram*](d-glos.md).</span></span>

</dd> <dt>

<span data-ttu-id="403cc-119"><span id="_rpc_connectionless_glos"></span><span id="_RPC_CONNECTIONLESS_GLOS"></span>**connessione**</span><span class="sxs-lookup"><span data-stu-id="403cc-119"><span id="_rpc_connectionless_glos"></span><span id="_RPC_CONNECTIONLESS_GLOS"></span>**connectionless**</span></span>
</dt> <dd>

<span data-ttu-id="403cc-120">Vedere [*datagramma*](d-glos.md).</span><span class="sxs-lookup"><span data-stu-id="403cc-120">See [*datagram*](d-glos.md).</span></span>

</dd> <dt>

<span data-ttu-id="403cc-121"><span id="_rpc_context_rundown_glos"></span><span id="_RPC_CONTEXT_RUNDOWN_GLOS"></span>**Rundown del contesto**</span><span class="sxs-lookup"><span data-stu-id="403cc-121"><span id="_rpc_context_rundown_glos"></span><span id="_RPC_CONTEXT_RUNDOWN_GLOS"></span>**context rundown**</span></span>
</dt> <dd>

<span data-ttu-id="403cc-122">Notifica del server risultante da una chiusura imprevista dell'associazione tra applicazioni client e server.</span><span class="sxs-lookup"><span data-stu-id="403cc-122">Server notification that results from an unexpected termination of the binding between client and server applications.</span></span>

</dd> </dl>

 

 




