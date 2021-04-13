---
description: Le applicazioni COM+ sono costituite da uno o più componenti COM.
ms.assetid: e7ed2844-276e-4726-952d-e4d3be2eb6e8
title: Parti di un'applicazione COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f75aba454689e25e8706d4a7e3f059d498891f9e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483029"
---
# <a name="parts-of-a-com-application"></a><span data-ttu-id="06eef-103">Parti di un'applicazione COM+</span><span class="sxs-lookup"><span data-stu-id="06eef-103">Parts of a COM+ Application</span></span>

<span data-ttu-id="06eef-104">Le applicazioni COM+ sono costituite da uno o più componenti COM.</span><span class="sxs-lookup"><span data-stu-id="06eef-104">COM+ applications consist of one or more COM components.</span></span>

<span data-ttu-id="06eef-105">In tutta la documentazione COM+ vengono utilizzati i termini seguenti:</span><span class="sxs-lookup"><span data-stu-id="06eef-105">The following terms are used throughout the COM+ documentation:</span></span>

<dl> <dt>

<span data-ttu-id="06eef-106"><span id="COM_component"></span><span id="com_component"></span><span id="COM_COMPONENT"></span>*Componente COM*</span><span class="sxs-lookup"><span data-stu-id="06eef-106"><span id="COM_component"></span><span id="com_component"></span><span id="COM_COMPONENT"></span>*COM component*</span></span>
</dt> <dd>

<span data-ttu-id="06eef-107">Unità binaria di codice che crea oggetti COM (include il codice per la creazione di pacchetti e la registrazione).</span><span class="sxs-lookup"><span data-stu-id="06eef-107">A binary unit of code that creates COM objects (includes packaging and registration code).</span></span>

</dd> <dt>

<span data-ttu-id="06eef-108"><span id="COM_object"></span><span id="com_object"></span><span id="COM_OBJECT"></span>*Oggetto COM*</span><span class="sxs-lookup"><span data-stu-id="06eef-108"><span id="COM_object"></span><span id="com_object"></span><span id="COM_OBJECT"></span>*COM object*</span></span>
</dt> <dd>

<span data-ttu-id="06eef-109">Istanza di una classe COM.</span><span class="sxs-lookup"><span data-stu-id="06eef-109">An instance of a COM class.</span></span>

</dd> <dt>

<span data-ttu-id="06eef-110"><span id="COM_class"></span><span id="com_class"></span><span id="COM_CLASS"></span>*Classe COM*</span><span class="sxs-lookup"><span data-stu-id="06eef-110"><span id="COM_class"></span><span id="com_class"></span><span id="COM_CLASS"></span>*COM class*</span></span>
</dt> <dd>

<span data-ttu-id="06eef-111">Implementazione concreta denominata di una o più interfacce.</span><span class="sxs-lookup"><span data-stu-id="06eef-111">A named, concrete implementation of one or more interfaces.</span></span> <span data-ttu-id="06eef-112">Una classe COM è identificata da un CLSID (talvolta anche da un ProgID).</span><span class="sxs-lookup"><span data-stu-id="06eef-112">A COM class is identified by a CLSID (sometimes by a ProgID also).</span></span>

</dd> <dt>

<span data-ttu-id="06eef-113"><span id="COM_interface"></span><span id="com_interface"></span><span id="COM_INTERFACE"></span>*Interfaccia COM*</span><span class="sxs-lookup"><span data-stu-id="06eef-113"><span id="COM_interface"></span><span id="com_interface"></span><span id="COM_INTERFACE"></span>*COM interface*</span></span>
</dt> <dd>

<span data-ttu-id="06eef-114">Gruppo di funzioni di metodo correlate esposte da una classe COM che specifica un contratto.</span><span class="sxs-lookup"><span data-stu-id="06eef-114">A group of related method functions exposed by a COM class that specify a contract.</span></span> <span data-ttu-id="06eef-115">Sono inclusi il nome, la firma dell'interfaccia, la semantica dell'interfaccia e il formato del buffer di marshalling.</span><span class="sxs-lookup"><span data-stu-id="06eef-115">This includes the name, interface signature, interface semantics, and marshaling buffer format.</span></span> <span data-ttu-id="06eef-116">Un'interfaccia viene identificata da un IID.</span><span class="sxs-lookup"><span data-stu-id="06eef-116">An interface is identified by an IID.</span></span> <span data-ttu-id="06eef-117">La sintassi dell'interfaccia è definita nelle librerie di tipi e/o IDL.</span><span class="sxs-lookup"><span data-stu-id="06eef-117">The interface syntax is defined in IDL and/or type libraries.</span></span> <span data-ttu-id="06eef-118">Le interfacce di una classe COM devono essere divise in set di metodi gestibili e coesi.</span><span class="sxs-lookup"><span data-stu-id="06eef-118">The interfaces of a COM class should be divided into manageable, cohesive sets of methods.</span></span>

<span data-ttu-id="06eef-119">Le interfacce COM non sono modificabili. il contratto COM indica che non è possibile modificarli.</span><span class="sxs-lookup"><span data-stu-id="06eef-119">COM interfaces are immutable; the COM contract states that they cannot be modified.</span></span> <span data-ttu-id="06eef-120">Qualsiasi modifica, ad esempio l'aggiunta di metodi, richiede la definizione di una nuova interfaccia.</span><span class="sxs-lookup"><span data-stu-id="06eef-120">Any modification (such as adding methods) requires defining a new interface.</span></span>

</dd> <dt>

<span data-ttu-id="06eef-121"><span id="COM_method"></span><span id="com_method"></span><span id="COM_METHOD"></span>*Metodo COM*</span><span class="sxs-lookup"><span data-stu-id="06eef-121"><span id="COM_method"></span><span id="com_method"></span><span id="COM_METHOD"></span>*COM method*</span></span>
</dt> <dd>

<span data-ttu-id="06eef-122">Uno di un set di funzioni correlate fornite da un'interfaccia COM.</span><span class="sxs-lookup"><span data-stu-id="06eef-122">One of a set of related functions provided by a COM interface.</span></span>

</dd> </dl>

## <a name="configured-and-unconfigured-components"></a><span data-ttu-id="06eef-123">Componenti configurati e non configurati</span><span class="sxs-lookup"><span data-stu-id="06eef-123">Configured and Unconfigured Components</span></span>

<span data-ttu-id="06eef-124">Per sfruttare i servizi supportati dalle applicazioni COM+, l'ambiente COM+ impone requisiti specifici sui componenti COM compilati per le applicazioni COM+.</span><span class="sxs-lookup"><span data-stu-id="06eef-124">To take advantage of the services that COM+ applications support, the COM+ environment imposes specific requirements on COM components built for COM+ applications.</span></span> <span data-ttu-id="06eef-125">Quando viene aggiunto a un'applicazione COM+, un componente COM è noto come *componente configurato*.</span><span class="sxs-lookup"><span data-stu-id="06eef-125">When added to a COM+ application, a COM component is known as a *configured component*.</span></span>

<span data-ttu-id="06eef-126">I componenti COM compilati per le applicazioni COM+ sono componenti server in-process.</span><span class="sxs-lookup"><span data-stu-id="06eef-126">COM components built for COM+ applications are in-process server components.</span></span> <span data-ttu-id="06eef-127">Il componente deve contenere una libreria dei tipi (file tlb) per descrivere tutte le classi implementate nel componente e dichiarare le interfacce per tutte le classi nel componente.</span><span class="sxs-lookup"><span data-stu-id="06eef-127">The component must contain a type library (.tlb file) to describe all classes implemented in the component and declare the interfaces on all classes in the component.</span></span> <span data-ttu-id="06eef-128">È possibile creare e implementare questi componenti con Microsoft Visual Basic, Microsoft Visual C++ o qualsiasi strumento di sviluppo compatibile con COM.</span><span class="sxs-lookup"><span data-stu-id="06eef-128">You can create and implement these components with Microsoft Visual Basic, Microsoft Visual C++, or any COM-compatible development tool.</span></span>

<span data-ttu-id="06eef-129">Un *componente non configurato* è un componente che non viene installato in un'applicazione com+.</span><span class="sxs-lookup"><span data-stu-id="06eef-129">An *unconfigured component* is a component that isn't installed in a COM+ application.</span></span> <span data-ttu-id="06eef-130">È possibile trasformare la maggior parte dei componenti non configurati in componenti configurati semplicemente mediante l'integrazione in un'applicazione COM+.</span><span class="sxs-lookup"><span data-stu-id="06eef-130">You can transform most unconfigured components into configured components simply by integrating them into a COM+ application.</span></span>

> [!Note]  
> <span data-ttu-id="06eef-131">Non utilizzare lo stesso AppID per un'applicazione COM+ e nel registro di sistema per un componente non configurato.</span><span class="sxs-lookup"><span data-stu-id="06eef-131">Do not use the same AppID for both a COM+ application and in the registry for an unconfigured component.</span></span> <span data-ttu-id="06eef-132">Quando il componente non configurato viene attivato, l'attivazione può recuperare le informazioni dell'applicazione COM+ dal registro di sistema che non contiene le informazioni necessarie per l'attivazione COM.</span><span class="sxs-lookup"><span data-stu-id="06eef-132">When the unconfigured component is activated , as activation may retrieve the COM+ application information from the registry that does not contain the information required for COM activation.</span></span> <span data-ttu-id="06eef-133">Potrebbero verificarsi problemi simili se viene effettuata una chiamata a [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) da Dllhost che ospita l'applicazione server com+.</span><span class="sxs-lookup"><span data-stu-id="06eef-133">Similar problems could arise if a call is made to [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) from DllHost that hosts COM+ Server application.</span></span>

 

 

 
