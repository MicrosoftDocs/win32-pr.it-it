---
description: Il catalogo COM+ archivia gli attributi dell'applicazione COM+, gli attributi della classe e gli attributi a livello di computer. Garantisce la coerenza tra questi attributi e fornisce operazioni comuni su questi attributi.
ms.assetid: 1838757c-aa8e-4678-8042-207498fb0bbc
title: Catalogo COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad869a6df6a61fc338fe07002512a1de27002788
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304607"
---
# <a name="the-com-catalog"></a><span data-ttu-id="e2850-104">Catalogo COM+</span><span class="sxs-lookup"><span data-stu-id="e2850-104">The COM+ Catalog</span></span>

<span data-ttu-id="e2850-105">Il catalogo COM+ archivia gli attributi dell'applicazione COM+, gli attributi della classe e gli attributi a livello di computer.</span><span class="sxs-lookup"><span data-stu-id="e2850-105">The COM+ catalog stores COM+ application attributes, class attributes, and computer-level attributes.</span></span> <span data-ttu-id="e2850-106">Garantisce la coerenza tra questi attributi e fornisce operazioni comuni su questi attributi.</span><span class="sxs-lookup"><span data-stu-id="e2850-106">It guarantees consistency among these attributes and provides common operations on top of these attributes.</span></span>

<span data-ttu-id="e2850-107">Il catalogo COM+ utilizza due archivi diversi, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="e2850-107">The COM+ catalog uses two different stores, as follows:</span></span>

-   <span data-ttu-id="e2850-108">Database di registrazione COM+</span><span class="sxs-lookup"><span data-stu-id="e2850-108">The COM+ registration database</span></span>
-   <span data-ttu-id="e2850-109">Registro di sistema di Windows (**\_ \_ radice delle classi HKEY**)</span><span class="sxs-lookup"><span data-stu-id="e2850-109">The Windows registry (**HKEY\_CLASSES\_ROOT**)</span></span>

<span data-ttu-id="e2850-110">Il catalogo presenta una visualizzazione logica unificata di questi due archivi e li espone tramite la libreria di amministrazione COM+.</span><span class="sxs-lookup"><span data-stu-id="e2850-110">The catalog presents a unified, logical view of these two stores and exposes them through the COM+ Administration Library.</span></span> <span data-ttu-id="e2850-111">Questa libreria fornisce, tramite un linguaggio di scripting, tutte le funzionalità dello strumento di amministrazione Servizi componenti.</span><span class="sxs-lookup"><span data-stu-id="e2850-111">This library provides, through a scripting language, all the functionality of the Component Services administrative tool.</span></span>

<span data-ttu-id="e2850-112">Per i componenti COM esistenti che non richiedono alcun nuovo servizio COM+, la ricerca viene eseguita nel registro di sistema di Windows esistente.</span><span class="sxs-lookup"><span data-stu-id="e2850-112">For existing COM components that do not require any new COM+ services, lookup occurs in the existing Windows registry.</span></span> <span data-ttu-id="e2850-113">Il catalogo COM+ usa anche il registro di sistema di Windows per la registrazione di librerie dei tipi e proxy/stub di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="e2850-113">The COM+ catalog also uses the Windows registry for type library and interface proxy/stub registration.</span></span>

## <a name="split-registration"></a><span data-ttu-id="e2850-114">Suddivisione registrazione</span><span class="sxs-lookup"><span data-stu-id="e2850-114">Split Registration</span></span>

<span data-ttu-id="e2850-115">Per i nuovi componenti che sono effettivamente già componenti COM esistenti utilizzati nell'ambiente dei servizi (ad esempio, i componenti MTS), l'aspetto COM di base della registrazione viene archiviato nel registro di sistema di Windows e i nuovi servizi e attributi (ad esempio, i componenti in coda) vengono archiviati nel database di registrazione COM+.</span><span class="sxs-lookup"><span data-stu-id="e2850-115">For new components that are actually already existing COM components that are used in the services environment (for example, MTS components), the basic COM aspect of the registration is stored in the Windows registry and new services and attributes (for example, queued components) are stored in the COM+ registration database.</span></span> <span data-ttu-id="e2850-116">Questa operazione è nota come *registrazione Split*.</span><span class="sxs-lookup"><span data-stu-id="e2850-116">This is known as a *split registration*.</span></span>

<span data-ttu-id="e2850-117">Ogni attributo viene archiviato in una sola posizione, ovvero il registro di sistema di Windows o il database di registrazione COM+.</span><span class="sxs-lookup"><span data-stu-id="e2850-117">Each attribute is stored in only one location: either the Windows registry or the COM+ registration database.</span></span> <span data-ttu-id="e2850-118">I nuovi componenti COM vengono registrati esclusivamente nel database di registrazione COM+, con alcune duplicazioni nel registro di sistema di Windows, in modo che gli strumenti esistenti possano usarli.</span><span class="sxs-lookup"><span data-stu-id="e2850-118">New COM components are registered exclusively in the COM+ registration database, with some duplication in the Windows registry so that existing tools can use them.</span></span>

## <a name="transactional-updates-to-the-catalog"></a><span data-ttu-id="e2850-119">Aggiornamenti transazionali al catalogo</span><span class="sxs-lookup"><span data-stu-id="e2850-119">Transactional Updates to the Catalog</span></span>

<span data-ttu-id="e2850-120">Alcune operazioni nel catalogo vengono eseguite in modo transazionale.</span><span class="sxs-lookup"><span data-stu-id="e2850-120">Some operations on the catalog are performed in a transactional manner.</span></span> <span data-ttu-id="e2850-121">Quando si richiama la libreria di amministrazione COM+ da un componente transazionale, gli aggiornamenti al database di registrazione COM+ avvengono all'interno del limite della transazione del componente chiamante.</span><span class="sxs-lookup"><span data-stu-id="e2850-121">When you invoke the COM+ Administration Library from a transactional component, the updates to the COM+ registration database will take place within the calling component's transaction boundary.</span></span>

<span data-ttu-id="e2850-122">Tuttavia, gli aggiornamenti che comportano modifiche ad altri archivi, ad esempio il file system e il registro di sistema di Windows, non sono necessariamente completamente transazionali.</span><span class="sxs-lookup"><span data-stu-id="e2850-122">However, updates that involve changes to other stores (such as the file system and Windows registry) are not guaranteed to be fully transactional.</span></span> <span data-ttu-id="e2850-123">Una transazione interrotta può lasciare questi archivi in uno stato non coerente con le modifiche apportate l'una all'altra o al database di registrazione COM+.</span><span class="sxs-lookup"><span data-stu-id="e2850-123">An aborted transaction can leave these stores in a state that is inconsistent with any changes made to one another or to the COM+ registration database.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e2850-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e2850-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2850-125">Creazione di pacchetti di installazione per applicazioni COM+</span><span class="sxs-lookup"><span data-stu-id="e2850-125">Creating Installation Packages for COM+ Applications</span></span>](creating-installation-packages-for-com--applications.md)
</dt> <dt>

[<span data-ttu-id="e2850-126">Distribuzione di proxy di applicazione</span><span class="sxs-lookup"><span data-stu-id="e2850-126">Deploying Application Proxies</span></span>](deploying-application-proxies.md)
</dt> <dt>

[<span data-ttu-id="e2850-127">Utilità di replica COMREPL</span><span class="sxs-lookup"><span data-stu-id="e2850-127">The COMREPL Replication Utility</span></span>](the-comrepl-replication-utility.md)
</dt> </dl>

 

 



