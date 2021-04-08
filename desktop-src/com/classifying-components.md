---
title: Classificazione di componenti
description: Classificazione di componenti
ms.assetid: 4d805532-96c9-400d-b78a-f8d0d9bdbf83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53ea1547c219a44262fdeaf7edb02f65c7a3aac6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856617"
---
# <a name="classifying-components"></a><span data-ttu-id="45845-103">Classificazione di componenti</span><span class="sxs-lookup"><span data-stu-id="45845-103">Classifying Components</span></span>

<span data-ttu-id="45845-104">Mentre un client è in grado di scorrere l'elenco dei CLSID nel registro di sistema e di selezionare un componente da usare, il caricamento di ogni componente nel registro di sistema e l'esecuzione di query per le interfacce supportate sono molto dispendiosi in termini di tempo.</span><span class="sxs-lookup"><span data-stu-id="45845-104">While a client is able to browse through the list of CLSIDs in the registry and select a component to use, loading each component in the registry and querying it for its supported interfaces is very time-consuming.</span></span> <span data-ttu-id="45845-105">Per determinare se un componente supporta le interfacce necessarie prima di creare un'istanza del componente, è stato sviluppato un metodo per classificare i componenti in categorie.</span><span class="sxs-lookup"><span data-stu-id="45845-105">To determine whether a component supports the interfaces required before creating an instance of the component, a method to classify components into categories was developed.</span></span>

<span data-ttu-id="45845-106">Una categoria di componenti è un set di interfacce a cui è stato assegnato un GUID denominato CATId.</span><span class="sxs-lookup"><span data-stu-id="45845-106">A component category is a set of interfaces that have been assigned a GUID named CATID.</span></span> <span data-ttu-id="45845-107">I componenti che implementano tutte le interfacce in una categoria di componenti si registrano come membri di tale categoria di componenti.</span><span class="sxs-lookup"><span data-stu-id="45845-107">Components that implement all of the interfaces in a component category register themselves as members of that component category.</span></span> <span data-ttu-id="45845-108">I componenti che appartengono a una determinata categoria di componenti possono quindi essere selezionati dal registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="45845-108">Components that belong to a certain component category can then be selected from the registry.</span></span> <span data-ttu-id="45845-109">Registrandosi come membro di una categoria di componenti, il componente garantisce che supporti tutte le interfacce membro nella categoria Component.</span><span class="sxs-lookup"><span data-stu-id="45845-109">By registering itself as a member of a component category, the component is guaranteeing that it supports all of the member interfaces in the component category.</span></span>

<span data-ttu-id="45845-110">Un componente può essere un membro di molte categorie.</span><span class="sxs-lookup"><span data-stu-id="45845-110">A component can be a member of many categories.</span></span> <span data-ttu-id="45845-111">Non è limitato al supporto delle interfacce in una categoria di componenti.</span><span class="sxs-lookup"><span data-stu-id="45845-111">It is not limited to supporting interfaces in a component category.</span></span> <span data-ttu-id="45845-112">Può supportare qualsiasi interfaccia, oltre a quelle presenti in una categoria di componenti.</span><span class="sxs-lookup"><span data-stu-id="45845-112">It can support any interface, in addition to those in a component category.</span></span>

<span data-ttu-id="45845-113">Diversamente dalla registrazione standard dei componenti, in cui gli sviluppatori devono scrivere codice che registri manualmente gli oggetti, le categorie di componenti automatizzano la maggior parte di queste operazioni.</span><span class="sxs-lookup"><span data-stu-id="45845-113">In contrast to the standard registration of components, in which developers must write code that manually registers objects, component categories automates much of this work.</span></span> <span data-ttu-id="45845-114">I sei metodi dell'interfaccia [**ICatRegister**](/windows/desktop/api/ComCat/nn-comcat-icatregister) definiscono le categorie di componenti e registrano gli oggetti che implementano o li richiedono.</span><span class="sxs-lookup"><span data-stu-id="45845-114">The six methods of the [**ICatRegister**](/windows/desktop/api/ComCat/nn-comcat-icatregister) interface define component categories and register objects that implement or require them.</span></span> <span data-ttu-id="45845-115">L'oggetto di [gestione delle categorie di componenti](the-component-categories-manager.md) implementa questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="45845-115">The [Component Categories Manager](the-component-categories-manager.md) object implements this interface.</span></span> <span data-ttu-id="45845-116">Per ulteriori informazioni sull'utilizzo delle categorie di componenti, vedere **ICatRegister** e [**ICatInformation**](/windows/desktop/api/ComCat/nn-comcat-icatinformation) .</span><span class="sxs-lookup"><span data-stu-id="45845-116">See **ICatRegister** and [**ICatInformation**](/windows/desktop/api/ComCat/nn-comcat-icatinformation) for additional information on using component categories.</span></span>

## <a name="related-topics"></a><span data-ttu-id="45845-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="45845-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45845-118">Registrazione di applicazioni COM</span><span class="sxs-lookup"><span data-stu-id="45845-118">Registering COM Applications</span></span>](registering-com-applications.md)
</dt> </dl>

 

 




