---
title: Denominazione di attributi e classi
description: Questo argomento include le linee guida per la denominazione degli attributi e delle classi.
ms.assetid: ccbc2859-332f-4ded-9125-5bf507cad960
ms.tgt_platform: multiple
keywords:
- Denominazione di attributi e classi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80bfd2614033e12f68ba2727cc7aec689c16071e
ms.sourcegitcommit: 02e6e0b58720bf6b77797dd7a9ddc11c95f42b33
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/21/2020
ms.locfileid: "106300680"
---
# <a name="naming-attributes-and-classes"></a><span data-ttu-id="c59ce-104">Denominazione di attributi e classi</span><span class="sxs-lookup"><span data-stu-id="c59ce-104">Naming Attributes and Classes</span></span>

<span data-ttu-id="c59ce-105">Questo argomento include le linee guida per la denominazione degli attributi e delle classi.</span><span class="sxs-lookup"><span data-stu-id="c59ce-105">This topic includes guidelines for naming attributes and classes.</span></span>

<span data-ttu-id="c59ce-106">Per creare una nuova classe o attributo, attenersi alle seguenti regole di denominazione:</span><span class="sxs-lookup"><span data-stu-id="c59ce-106">To create a new class or attribute, adhere to the following naming rules:</span></span>

-   <span data-ttu-id="c59ce-107">Usare lo stesso nome per le proprietà **CN** e **ldapDisplayName** di un nuovo oggetto **attributeSchema** o **classSchema** .</span><span class="sxs-lookup"><span data-stu-id="c59ce-107">Use the same name for both the **cn** and **lDAPDisplayName** properties of a new **attributeSchema** or **classSchema** object.</span></span>
-   <span data-ttu-id="c59ce-108">Identificare la società con un prefisso minuscolo nella prima sezione del nome.</span><span class="sxs-lookup"><span data-stu-id="c59ce-108">Identify the company with a lower-case prefix in the first section of the name.</span></span> <span data-ttu-id="c59ce-109">Questo prefisso può essere un nome DNS, un acronimo o un'altra stringa che identifica in modo univoco l'azienda.</span><span class="sxs-lookup"><span data-stu-id="c59ce-109">This prefix can be a DNS name, acronym, or other string that uniquely identifies the company.</span></span> <span data-ttu-id="c59ce-110">Il prefisso garantisce che tutti gli attributi e le classi per una società specifica vengano visualizzati consecutivamente durante l'esplorazione dello schema.</span><span class="sxs-lookup"><span data-stu-id="c59ce-110">The prefix ensures that all attributes and classes for a specific company are displayed consecutively when browsing the schema.</span></span>
-   <span data-ttu-id="c59ce-111">Se si sviluppa un'estensione dello schema come fornitore di software indipendente, aggiungere un'abbreviazione del nome del prodotto del prefisso.</span><span class="sxs-lookup"><span data-stu-id="c59ce-111">If you are developing a schema extension as an independent software vendor, add an abbreviation of the product name of the prefix.</span></span> <span data-ttu-id="c59ce-112">In questo modo viene aggiunta la distinzione tra più prodotti che contengono estensioni dello schema LDAP.</span><span class="sxs-lookup"><span data-stu-id="c59ce-112">This adds distinction between multiple products that contain LDAP schema extensions.</span></span>
-   <span data-ttu-id="c59ce-113">Usare un trattino come carattere successivo dopo il prefisso.</span><span class="sxs-lookup"><span data-stu-id="c59ce-113">Use a hyphen as the next character after the prefix.</span></span>
-   <span data-ttu-id="c59ce-114">Specificare un attributo o un nome di classe univoco all'interno degli attributi della società dopo il segno meno.</span><span class="sxs-lookup"><span data-stu-id="c59ce-114">Specify an attribute or class name that is unique within the company's attributes after the hyphen.</span></span> <span data-ttu-id="c59ce-115">Questa parte del nome comune deve essere descrittiva.</span><span class="sxs-lookup"><span data-stu-id="c59ce-115">This part of the common-name should be descriptive.</span></span> <span data-ttu-id="c59ce-116">Non usare nomi illogici privi di significato per sviluppatori e visualizzatori dello schema.</span><span class="sxs-lookup"><span data-stu-id="c59ce-116">Do not use illogical names that are meaningless to developers and viewers of the schema.</span></span>

<span data-ttu-id="c59ce-117">Se, ad esempio, la società fittizia Fabrikam ha esteso lo schema aggiungendo un attributo per l'archiviazione di un identificatore della posta vocale, il **CN** e il **ldapDisplayName** del nuovo attributo potrebbero essere "Fabrikam-VoiceMailID".</span><span class="sxs-lookup"><span data-stu-id="c59ce-117">For example, if the fictitious Fabrikam company extended the schema by adding an attribute for storing a voice-mail identifier, the **cn** and **lDAPDisplayName** of the new attribute could be "fabrikam-VoiceMailID".</span></span>

<span data-ttu-id="c59ce-118">Se il **ldapDisplayName** di un attributo o di una classe non è specificato, il sistema usa il **CN** per generarne uno.</span><span class="sxs-lookup"><span data-stu-id="c59ce-118">If the **lDAPDisplayName** of an attribute or class is not specified, the system uses the **cn** to generate one.</span></span> <span data-ttu-id="c59ce-119">Tuttavia, l'algoritmo di sistema per la generazione del nome può causare conflitti di nomi o nomi difficili da leggere.</span><span class="sxs-lookup"><span data-stu-id="c59ce-119">However, the system algorithm for generating the name may result in name collisions or names that are difficult to read.</span></span> <span data-ttu-id="c59ce-120">Per evitare questi problemi, è consigliabile specificare in modo esplicito un **ldapDisplayName** per tutti gli attributi e le classi.</span><span class="sxs-lookup"><span data-stu-id="c59ce-120">To avoid these problems, it is recommended that an **lDAPDisplayName** be explicitly specified for all attributes and classes.</span></span>

<span data-ttu-id="c59ce-121">Per finalità di sviluppo e test, potrebbe essere opportuno aggiungere un suffisso di versione a **CN** e **ldapDisplayName**, ad esempio "Fabrikam-VoiceMailID-001".</span><span class="sxs-lookup"><span data-stu-id="c59ce-121">For development and testing purposes, it may be desirable to append a version suffix to the **cn** and **lDAPDisplayName**, for example, "fabrikam-VoiceMailID-001".</span></span> <span data-ttu-id="c59ce-122">In un ambiente di sviluppo/test distribuito, un suffisso di versione consente agli sviluppatori di eseguire contemporaneamente più versioni del software.</span><span class="sxs-lookup"><span data-stu-id="c59ce-122">In a distributed development/test environment, a version suffix enables developers to run multiple versions of their software simultaneously.</span></span> <span data-ttu-id="c59ce-123">Al termine del test, rinominare l'attributo o la classe per rimuovere il suffisso.</span><span class="sxs-lookup"><span data-stu-id="c59ce-123">After testing is complete, rename the attribute or class to remove the suffix.</span></span>

<span data-ttu-id="c59ce-124">Non è possibile eliminare le versioni inattive di un'estensione dello schema, ma è possibile disabilitarle e rinominarle con nomi oscuri.</span><span class="sxs-lookup"><span data-stu-id="c59ce-124">It is not possible to delete defunct versions of a schema extensions, but it is possible to disable them and rename them with obscure names.</span></span> <span data-ttu-id="c59ce-125">Per ulteriori informazioni, vedere la pagina relativa alla [disabilitazione di classi e attributi esistenti](disabling-existing-classes-and-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="c59ce-125">For more information, see [Disabling Existing Classes and Attributes](disabling-existing-classes-and-attributes.md).</span></span>

 

 




