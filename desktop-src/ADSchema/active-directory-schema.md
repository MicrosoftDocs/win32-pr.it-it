---
title: Schema di Active Directory (schema AD)
description: Lo schema Microsoft Active Directory contiene definizioni formali di ogni classe di oggetti che è possibile creare in una foresta Active Directory.
ms.assetid: b3da4519-d0c6-47eb-9455-ada653ad5c9e
ms.tgt_platform: multiple
keywords:
- Schema di Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b4c3393a6da1b8d1bd2c2418084c8f7fc657732
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299630"
---
# <a name="active-directory-schema-ad-schema"></a><span data-ttu-id="01fb3-104">Schema di Active Directory (schema AD)</span><span class="sxs-lookup"><span data-stu-id="01fb3-104">Active Directory Schema (AD Schema)</span></span>

<span data-ttu-id="01fb3-105">Lo schema Microsoft Active Directory contiene definizioni formali di ogni classe di oggetti che è possibile creare in una foresta Active Directory.</span><span class="sxs-lookup"><span data-stu-id="01fb3-105">The Microsoft Active Directory schema contains formal definitions of every object class that can be created in an Active Directory forest.</span></span> <span data-ttu-id="01fb3-106">Lo schema contiene inoltre definizioni formali di ogni attributo che possono esistere in un oggetto Active Directory.</span><span class="sxs-lookup"><span data-stu-id="01fb3-106">The schema also contains formal definitions of every attribute that can exist in an Active Directory object.</span></span> <span data-ttu-id="01fb3-107">In questa sezione vengono forniti i riferimenti per ogni oggetto dello schema e viene fornita una breve spiegazione degli attributi, delle classi e di altri oggetti che costituiscono lo schema di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="01fb3-107">This section provides the reference for each schema object and provides a brief explanation of the attributes, classes, and other objects that make up the Active Directory schema.</span></span>

> [!Note]  
> <span data-ttu-id="01fb3-108">Nella documentazione seguente sono contenuti i riferimenti di programmazione per Active Directory schema.</span><span class="sxs-lookup"><span data-stu-id="01fb3-108">The following documentation contains the programming reference for Active Directory schema.</span></span> <span data-ttu-id="01fb3-109">Se si è un utente finale che tenta di eseguire il debug di un errore della stampante, provare a eseguire ricerche nel [sito della community Microsoft](https://answers.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="01fb3-109">If you are an end-user attempting to debug a printer error, try searching on the [Microsoft community site](https://answers.microsoft.com).</span></span> <span data-ttu-id="01fb3-110">Per gli sviluppatori che cercano una panoramica generale dello schema Active Directory, vedere gli argomenti Cenni preliminari sullo [schema di Active Directory](/windows/desktop/AD/active-directory-schema) .</span><span class="sxs-lookup"><span data-stu-id="01fb3-110">If you are a developer looking for a general overview of Active Directory schema, see the [Active Directory Schema](/windows/desktop/AD/active-directory-schema) overview topics.</span></span> <span data-ttu-id="01fb3-111">Se si desiderano linee guida di programmazione per l'aggiornamento o la modifica dello schema, per ulteriori informazioni sull'estensione e la personalizzazione dello schema, vedere [estensione](/windows/desktop/AD/extending-the-schema)dello schema, nonché molti degli argomenti inclusi nella [Active Directory Domain Services](/windows/desktop/AD/active-directory-domain-services) e [Active Directory Lightweight Directory Services](/previous-versions/windows/desktop/adam/active-directory-lightweight-directory-services) guide di programmazione.</span><span class="sxs-lookup"><span data-stu-id="01fb3-111">If you are looking for programming guidelines for updating or modifying the schema, For more information about extending and customizing the schema, see [Extending the Schema](/windows/desktop/AD/extending-the-schema), as well as many of the topics in the [Active Directory Domain Services](/windows/desktop/AD/active-directory-domain-services) and [Active Directory Lightweight Directory Services](/previous-versions/windows/desktop/adam/active-directory-lightweight-directory-services) programming guides.</span></span>

 

<span data-ttu-id="01fb3-112">In ognuno degli argomenti di riferimento è presente una sezione per ogni sistema operativo a cui si applica l'argomento.</span><span class="sxs-lookup"><span data-stu-id="01fb3-112">In each of the reference topics, there is a section for each operating system that the topic applies to.</span></span> <span data-ttu-id="01fb3-113">Attualmente sono supportati i sistemi operativi seguenti.</span><span class="sxs-lookup"><span data-stu-id="01fb3-113">The following operating systems are currently supported.</span></span> 

| <span data-ttu-id="01fb3-114">Piattaforma</span><span class="sxs-lookup"><span data-stu-id="01fb3-114">Platform</span></span>                                                      | <span data-ttu-id="01fb3-115">Nome nell'argomento</span><span class="sxs-lookup"><span data-stu-id="01fb3-115">Name in topic</span></span>                               |
|---------------------------------------------------------------|---------------------------------------------|
| <span data-ttu-id="01fb3-116">Microsoft Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="01fb3-116">Microsoft Windows Server 2003</span></span><br/>                      | <span data-ttu-id="01fb3-117">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="01fb3-117">Windows Server 2003</span></span><br/>              |
| <span data-ttu-id="01fb3-118">Microsoft Active Directory Application Mode (ADAM)</span><span class="sxs-lookup"><span data-stu-id="01fb3-118">Microsoft Active Directory Application Mode (ADAM)</span></span><br/> | <span data-ttu-id="01fb3-119">ADAM</span><span class="sxs-lookup"><span data-stu-id="01fb3-119">ADAM</span></span><br/>                             |
| <span data-ttu-id="01fb3-120">Microsoft Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="01fb3-120">Microsoft Windows Server 2003 R2</span></span><br/>                   | <span data-ttu-id="01fb3-121">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="01fb3-121">Windows Server 2003 R2</span></span><br/>           |
| <span data-ttu-id="01fb3-122">Microsoft Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="01fb3-122">Microsoft Windows Server 2008</span></span><br/>                      | <span data-ttu-id="01fb3-123">Microsoft Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="01fb3-123">Microsoft Windows Server 2008</span></span><br/>    |
| <span data-ttu-id="01fb3-124">Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="01fb3-124">Microsoft Windows Server 2008 R2</span></span><br/>                   | <span data-ttu-id="01fb3-125">Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="01fb3-125">Microsoft Windows Server 2008 R2</span></span><br/> |
| <span data-ttu-id="01fb3-126">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="01fb3-126">Microsoft Windows Server 2012</span></span><br/>                      | <span data-ttu-id="01fb3-127">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="01fb3-127">Microsoft Windows Server 2012</span></span><br/>    |



 

<span data-ttu-id="01fb3-128">Se un sistema operativo non è elencato nell'argomento, l'argomento non è supportato in tale sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="01fb3-128">If an operating system is not listed in the topic, the topic is not supported on that operating system.</span></span> <span data-ttu-id="01fb3-129">Se, ad esempio, un argomento elenca solo Windows Server 2003 e ADAM, l'argomento non si applica a Windows Server 2003 R2.</span><span class="sxs-lookup"><span data-stu-id="01fb3-129">For example, if a topic only lists Windows Server 2003 and ADAM, then the topic does not apply to Windows Server 2003 R2.</span></span>

<span data-ttu-id="01fb3-130">Le sezioni seguenti contengono informazioni dettagliate sugli elementi dello schema Active Directory.</span><span class="sxs-lookup"><span data-stu-id="01fb3-130">The following sections contain detailed information about the Active Directory schema elements.</span></span>

-   [<span data-ttu-id="01fb3-131">Terminologia dello schema Active Directory</span><span class="sxs-lookup"><span data-stu-id="01fb3-131">Active Directory Schema Terminology</span></span>](active-directory-schema-site.md)
-   [<span data-ttu-id="01fb3-132">Classi</span><span class="sxs-lookup"><span data-stu-id="01fb3-132">Classes</span></span>](classes.md)
-   [<span data-ttu-id="01fb3-133">Attributes (Attributi)</span><span class="sxs-lookup"><span data-stu-id="01fb3-133">Attributes</span></span>](attributes.md)
-   [<span data-ttu-id="01fb3-134">Sintassi</span><span class="sxs-lookup"><span data-stu-id="01fb3-134">Syntaxes</span></span>](syntaxes.md)
-   [<span data-ttu-id="01fb3-135">Controllo dei diritti di accesso</span><span class="sxs-lookup"><span data-stu-id="01fb3-135">Control Access Rights</span></span>](control-access-rights.md)
-   [<span data-ttu-id="01fb3-136">RootDSE</span><span class="sxs-lookup"><span data-stu-id="01fb3-136">RootDSE</span></span>](rootdse.md)

 

