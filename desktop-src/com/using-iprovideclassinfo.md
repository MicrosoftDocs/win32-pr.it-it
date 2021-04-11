---
title: Uso di IProvideClassInfo
description: Uso di IProvideClassInfo
ms.assetid: 16541aab-474f-4ae5-a6b6-fb2fea6d38ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32a3abd61bb330a2a7d681b6d53648c5fbde8c53
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047433"
---
# <a name="using-iprovideclassinfo"></a><span data-ttu-id="06858-103">Uso di IProvideClassInfo</span><span class="sxs-lookup"><span data-stu-id="06858-103">Using IProvideClassInfo</span></span>

<span data-ttu-id="06858-104">Un oggetto collegabile può offrire le interfacce [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) e [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2) in modo che i client possano facilmente esaminare le informazioni sul tipo.</span><span class="sxs-lookup"><span data-stu-id="06858-104">A connectable object can offer the [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) and [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2) interfaces so that its clients can easily examine its type information.</span></span> <span data-ttu-id="06858-105">Questa funzionalità è importante quando si gestiscono le interfacce in uscita, che, per definizione, sono definite da un oggetto ma implementate da un client sul relativo oggetto sink.</span><span class="sxs-lookup"><span data-stu-id="06858-105">This capability is important when dealing with outgoing interfaces, which, by definition, are defined by an object but implemented by a client on its own sink object.</span></span> <span data-ttu-id="06858-106">In alcuni casi, un'interfaccia in uscita è nota in fase di compilazione sia per l'oggetto collegabile che per l'oggetto sink; Questo è il caso di [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink).</span><span class="sxs-lookup"><span data-stu-id="06858-106">In some cases, an outgoing interface is known at compile time to both the connectable object and the sink object; such is the case with [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink).</span></span>

<span data-ttu-id="06858-107">In altri casi, tuttavia, solo l'oggetto collegabile conosce le definizioni di interfaccia in uscita in fase di compilazione.</span><span class="sxs-lookup"><span data-stu-id="06858-107">In other cases, however, only the connectable object knows its outgoing interface definitions at compile time.</span></span> <span data-ttu-id="06858-108">In questi casi, il client deve ottenere le informazioni sul tipo per l'interfaccia in uscita, in modo che sia in grado di fornire dinamicamente un sink che supporta i punti di ingresso corretti, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="06858-108">In these cases, the client must obtain the type information for the outgoing interface so that it can dynamically provide a sink supporting the right entry points, as follows:</span></span>

1.  <span data-ttu-id="06858-109">Il client enumera i punti di connessione e quindi, per ottenere l'IID delle interfacce in uscita supportate dall'oggetto collegabile, chiama [**IConnectionPoint:: GetConnectionInterface**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-getconnectioninterface) per ogni punto di connessione.</span><span class="sxs-lookup"><span data-stu-id="06858-109">The client enumerates the connection points and then, to obtain the IIDs of outgoing interfaces supported by the connectable object, calls [**IConnectionPoint::GetConnectionInterface**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-getconnectioninterface) for each connection point.</span></span>
2.  <span data-ttu-id="06858-110">Il client esegue una query sull'oggetto collegabile per una delle interfacce [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) .</span><span class="sxs-lookup"><span data-stu-id="06858-110">The client queries the connectable object for one of the [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) interfaces.</span></span>
3.  <span data-ttu-id="06858-111">Il client chiama i metodi nelle interfacce [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) per ottenere le informazioni sul tipo per l'interfaccia in uscita.</span><span class="sxs-lookup"><span data-stu-id="06858-111">The client calls methods in the [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) interfaces to get the type information for the outgoing interface.</span></span>
4.  <span data-ttu-id="06858-112">Il client crea un oggetto sink che supporta l'interfaccia in uscita.</span><span class="sxs-lookup"><span data-stu-id="06858-112">The client creates a sink object supporting the outgoing interface.</span></span>
5.  <span data-ttu-id="06858-113">Il processo continua e il client chiama [**IConnectionPoint:: Advise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) per connettere il sink al punto di connessione.</span><span class="sxs-lookup"><span data-stu-id="06858-113">The process continues, and the client calls [**IConnectionPoint::Advise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) to connect its sink to the connection point.</span></span>

<span data-ttu-id="06858-114">Nelle informazioni sul tipo, l' [**origine**](/windows/desktop/Midl/source) dell'attributo contrassegna un' [**interfaccia**](/windows/desktop/Midl/interface) o un'interfaccia [**Dispatch**](/windows/desktop/Midl/dispinterface) elencata sotto una [**coclasse**](/windows/desktop/Midl/coclass) come interfaccia in uscita.</span><span class="sxs-lookup"><span data-stu-id="06858-114">In the type information, the attribute [**source**](/windows/desktop/Midl/source) marks an [**interface**](/windows/desktop/Midl/interface) or [**dispinterface**](/windows/desktop/Midl/dispinterface) listed under a [**coclass**](/windows/desktop/Midl/coclass) as an outgoing interface.</span></span> <span data-ttu-id="06858-115">Quelli elencati senza questo attributo sono considerati interfacce in ingresso.</span><span class="sxs-lookup"><span data-stu-id="06858-115">Those listed without this attribute are considered incoming interfaces.</span></span>

## <a name="related-topics"></a><span data-ttu-id="06858-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="06858-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06858-117">Interfacce di oggetti collegabili</span><span class="sxs-lookup"><span data-stu-id="06858-117">Connectable Object Interfaces</span></span>](connectable-object-interfaces.md)
</dt> <dt>

[<span data-ttu-id="06858-118">Fornire informazioni sulla classe</span><span class="sxs-lookup"><span data-stu-id="06858-118">Providing Class Information</span></span>](providing-class-information.md)
</dt> </dl>

 

 