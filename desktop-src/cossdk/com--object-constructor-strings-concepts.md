---
description: Le stringhe del costruttore di oggetti COM+ sono stringhe di inizializzazione che vengono specificate in maniera amministrativa per un componente.
ms.assetid: b4915dae-c97c-4d36-95ee-bb10dcb40845
title: Concetti relativi alle stringhe del costruttore di oggetti COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c32bffd35ad230efe1f22b52da10e1b4910d71da
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966028"
---
# <a name="com-object-constructor-strings-concepts"></a><span data-ttu-id="29361-103">Concetti relativi alle stringhe del costruttore di oggetti COM+</span><span class="sxs-lookup"><span data-stu-id="29361-103">COM+ Object Constructor Strings Concepts</span></span>

<span data-ttu-id="29361-104">Le stringhe del costruttore di oggetti COM+ sono stringhe di inizializzazione che vengono specificate in maniera amministrativa per un componente.</span><span class="sxs-lookup"><span data-stu-id="29361-104">COM+ object constructor strings are initialization strings that are administratively specified for a component.</span></span> <span data-ttu-id="29361-105">È possibile usare le stringhe del costruttore di oggetti per scrivere un singolo componente con un grado di generalizzazione che ne consente la personalizzazione in un secondo momento per una determinata attività. ovvero, è possibile eseguire la costruzione di oggetti con parametri.</span><span class="sxs-lookup"><span data-stu-id="29361-105">You can use object constructor strings to write a single component with a degree of generality that allows it to be later customized for a particular task; that is, you can perform parameterized object construction.</span></span>

<span data-ttu-id="29361-106">È ad esempio possibile utilizzare questa funzionalità per scrivere un componente che include una connessione ODBC generica e successivamente specificare un DSN esatto per il componente in modo amministrativo.</span><span class="sxs-lookup"><span data-stu-id="29361-106">For example, you might use this feature to write a component that holds a generic ODBC connection and later specify an exact DSN for the component administratively.</span></span> <span data-ttu-id="29361-107">Se la configurazione del sistema viene modificata, è possibile modificare di conseguenza la stringa del costruttore.</span><span class="sxs-lookup"><span data-stu-id="29361-107">If the system configuration changes, you can change the constructor string accordingly.</span></span>

> [!Note]  
> <span data-ttu-id="29361-108">Le stringhe del costruttore di oggetti non devono essere usate per archiviare informazioni sensibili alla sicurezza.</span><span class="sxs-lookup"><span data-stu-id="29361-108">Object constructor strings should not be used to store security-sensitive information.</span></span>

 

<span data-ttu-id="29361-109">È possibile utilizzare le stringhe del costruttore di oggetti insieme al [pool di oggetti](com--object-pooling.md) per ottenere un livello maggiore di granularità nella modalità di raggruppamento e riutilizzo delle risorse.</span><span class="sxs-lookup"><span data-stu-id="29361-109">You can use object constructor strings in conjunction with [object pooling](com--object-pooling.md) to achieve a greater degree of granularity in how you pool and reuse resources.</span></span> <span data-ttu-id="29361-110">È possibile, ad esempio, creare diversi componenti distinti, ad eccezione delle stringhe del costruttore e dei CLSID, per mantenere pool distinti di oggetti che contengano connessioni utilizzabili da gruppi distinti di client.</span><span class="sxs-lookup"><span data-stu-id="29361-110">For example, you might create several distinct components, identical except for constructor strings and CLSIDs, to maintain distinct pools of objects holding connections usable by distinct groups of clients.</span></span> <span data-ttu-id="29361-111">Questa operazione è utile se le connessioni vengono aperte in modo da associarle a specifici ruoli di sicurezza, ad esempio quando le connessioni vengono aperte con un'autenticazione specifica nel database, rendendole non riutilizzabile nel caso generale.</span><span class="sxs-lookup"><span data-stu-id="29361-111">This would be useful if connections are opened in a manner that binds them to particular security roles—such as when the connections are opened with some specific authentication at the database—rendering them non-reusable in the general case.</span></span>

<span data-ttu-id="29361-112">A tale scopo, è possibile scrivere un singolo componente generico che si basa sulle stringhe del costruttore di oggetti, usando [**IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct), e ricompilarlo per produrre diversi componenti personalizzabili ciascuno con un CLSID distinto.</span><span class="sxs-lookup"><span data-stu-id="29361-112">To do this, you can write a single generic component that relies on object constructor strings, using [**IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct), and recompile it to produce several customizable components each with a distinct CLSID.</span></span> <span data-ttu-id="29361-113">È quindi possibile personalizzare in modo amministrativo ogni componente per aprire una connessione appropriata con una stringa del costruttore, configurarli per il pool e mantenerli in pool distinti per CLSID.</span><span class="sxs-lookup"><span data-stu-id="29361-113">You can then administratively tailor each component to open an appropriate connection with a constructor string, configure them to be pooled, and they will be maintained in distinct pools per CLSID.</span></span>

<span data-ttu-id="29361-114">È possibile specificare una stringa del costruttore quando un componente è stato scritto in modo specifico per riconoscere la stringa immessa.</span><span class="sxs-lookup"><span data-stu-id="29361-114">You can specify a constructor string when a component has been written specifically to recognize the string that you enter.</span></span> <span data-ttu-id="29361-115">I componenti possono accedere a queste stringhe a livello di codice usando [**IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct).</span><span class="sxs-lookup"><span data-stu-id="29361-115">Components can access these strings programmatically by using [**IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct).</span></span>

<span data-ttu-id="29361-116">Le stringhe del costruttore vengono passate in fase di creazione dell'oggetto solo quando la costruzione di oggetti è abilitata in un punto amministrativo.</span><span class="sxs-lookup"><span data-stu-id="29361-116">Constructor strings are passed in at object creation time only when object construction is administratively enabled.</span></span> <span data-ttu-id="29361-117">COM+ chiama il metodo [**IObjectConstruct:: Construct**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectconstruct-construct) che implementa.</span><span class="sxs-lookup"><span data-stu-id="29361-117">COM+ calls the [**IObjectConstruct::Construct**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectconstruct-construct) method that it implements.</span></span> <span data-ttu-id="29361-118">All'interno di questo metodo, è possibile accedere alla stringa del costruttore usando [**IObjectConstructString**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstructstring).</span><span class="sxs-lookup"><span data-stu-id="29361-118">Within that method, you can access the constructor string by using [**IObjectConstructString**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstructstring).</span></span> <span data-ttu-id="29361-119">Le stringhe vuote possono essere voci valide.</span><span class="sxs-lookup"><span data-stu-id="29361-119">Empty strings can be valid entries.</span></span>

## <a name="related-topics"></a><span data-ttu-id="29361-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="29361-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29361-121">Pool di oggetti COM+</span><span class="sxs-lookup"><span data-stu-id="29361-121">COM+ Object Pooling</span></span>](com--object-pooling.md)
</dt> <dt>

[<span data-ttu-id="29361-122">Specifica di una stringa del costruttore di oggetti per un componente</span><span class="sxs-lookup"><span data-stu-id="29361-122">Specifying an Object Constructor String for a Component</span></span>](specifying-an-object-constructor-string-for-a-component.md)
</dt> <dt>

[<span data-ttu-id="29361-123">Uso di una stringa del costruttore di oggetti per costruire un componente</span><span class="sxs-lookup"><span data-stu-id="29361-123">Using an Object Constructor String to Construct a Component</span></span>](using-an-object-constructor-string-to-construct-a-component.md)
</dt> </dl>

 

 



