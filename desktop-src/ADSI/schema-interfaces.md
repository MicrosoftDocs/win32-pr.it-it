---
title: Interfacce dello schema
description: Interfacce dello schema
ms.assetid: b3427202-352b-4b35-877e-d28fb3d3906a
ms.tgt_platform: multiple
keywords:
- interfacce dello schema ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f414fdea2418fb92a0a3c8c9e8bf88eb6d7f00b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955087"
---
# <a name="schema-interfaces"></a><span data-ttu-id="10756-104">Interfacce dello schema</span><span class="sxs-lookup"><span data-stu-id="10756-104">Schema Interfaces</span></span>

<span data-ttu-id="10756-105">Il contenitore dello schema contiene un set di definizioni dello schema associate a una parte della struttura dello spazio dei nomi del provider.</span><span class="sxs-lookup"><span data-stu-id="10756-105">The schema container contains a set of schema definitions that are attached to part of the namespace tree of the provider.</span></span> <span data-ttu-id="10756-106">In genere, ogni istanza di uno spazio dei nomi dispone di un proprio schema.</span><span class="sxs-lookup"><span data-stu-id="10756-106">Typically, each instance of a namespace has its own schema.</span></span> <span data-ttu-id="10756-107">Nella figura seguente, ad esempio, il provider di esempio ADSI definisce un contenitore dello schema in ognuno dei nodi radice "Seattle" e "Toronto".</span><span class="sxs-lookup"><span data-stu-id="10756-107">For example, in the following figure, the ADSI example provider defines a schema container in each of the root nodes "Seattle" and "Toronto".</span></span>

![contenimento dello schema](images/schemacont.png)

<span data-ttu-id="10756-109">Per creare un'implementazione ADSI per un provider, è necessario fornire oggetti gestione schema che riflettano lo spazio dei nomi sottostante del provider e che supportano le interfacce dello schema ADSI.</span><span class="sxs-lookup"><span data-stu-id="10756-109">To create an ADSI implementation for a provider, you need to supply schema management objects that reflect the underlying namespace of the provider and which support ADSI schema interfaces.</span></span> <span data-ttu-id="10756-110">Di seguito è riportato un elenco delle interfacce dello schema ADSI, contenute nel contenitore dello schema.</span><span class="sxs-lookup"><span data-stu-id="10756-110">The following is a list of the ADSI schema interfaces, which are contained in the schema container.</span></span>

-   <span data-ttu-id="10756-111">[**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) rappresenta le classi del servizio directory.</span><span class="sxs-lookup"><span data-stu-id="10756-111">[**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) represents directory service classes.</span></span>
-   <span data-ttu-id="10756-112">[**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) rappresenta le proprietà del servizio directory con valori singoli o multipli.</span><span class="sxs-lookup"><span data-stu-id="10756-112">[**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) represents directory service properties that have single or multiple values.</span></span>
-   <span data-ttu-id="10756-113">[**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax) rappresenta il tipo Variant singolo.</span><span class="sxs-lookup"><span data-stu-id="10756-113">[**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax) represents the single VARIANT type.</span></span>

<span data-ttu-id="10756-114">Le interfacce definite da ADSI possono supportare proprietà e sintassi specifiche per il provider.</span><span class="sxs-lookup"><span data-stu-id="10756-114">Interfaces defined by ADSI can support specific properties and syntaxes for your provider.</span></span> <span data-ttu-id="10756-115">I provider possono scegliere di estendere una definizione ADSI usando i metodi che creano e accedono alle proprietà, ad esempio, è possibile usare i metodi dell'interfaccia [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) come [**Get**](/windows/desktop/api/Iads/nf-iads-iads-get), [**GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex), [**put**](/windows/desktop/api/Iads/nf-iads-iads-put) e [**PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex).</span><span class="sxs-lookup"><span data-stu-id="10756-115">Providers can choose to extend an ADSI definition by using the methods that create and access properties, for example, you can use the methods of the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface such as [**Get**](/windows/desktop/api/Iads/nf-iads-iads-get), [**GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex), [**Put**](/windows/desktop/api/Iads/nf-iads-iads-put) and [**PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex).</span></span> <span data-ttu-id="10756-116">I provider possono inoltre supportare proprietà aggiuntive tramite interfacce aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="10756-116">Providers can also support additional properties through additional interfaces.</span></span> <span data-ttu-id="10756-117">Per un elenco completo delle interfacce ADSI, vedere [interfacce ADSI](adsi-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="10756-117">For a complete list of ADSI interfaces, see [ADSI Interfaces](adsi-interfaces.md).</span></span>

<span data-ttu-id="10756-118">Un componente del provider ADSI con uno spazio dei nomi complesso può consentire l'esistenza di più schemi in un'istanza dello spazio dei nomi, ciascuno in una parte diversa dell'albero.</span><span class="sxs-lookup"><span data-stu-id="10756-118">An ADSI provider component with a complex namespace might allow multiple schemas to exist in a namespace instance, each at a different part of the tree.</span></span> <span data-ttu-id="10756-119">Tuttavia, la proprietà [**IADs:: schema**](iads-property-methods.md) di un oggetto denomina sempre la propria definizione dello schema.</span><span class="sxs-lookup"><span data-stu-id="10756-119">The [**IADs::Schema**](iads-property-methods.md) property of an object, however, always names its own schema definition.</span></span>

 

 




