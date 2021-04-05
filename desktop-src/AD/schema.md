---
title: Schema (AD DS)
description: Active Directory schema viene implementato come un set di istanze della classe di oggetti archiviate nella directory.
ms.assetid: 77c297ca-0dfc-4545-9832-4202e066822b
ms.tgt_platform: multiple
keywords:
- Active Directory schema Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7965232dd756272eb016ca251aa29716a22a088a
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/11/2019
ms.locfileid: "103719885"
---
# <a name="schema-ad-ds"></a><span data-ttu-id="d0ee9-104">Schema (AD DS)</span><span class="sxs-lookup"><span data-stu-id="d0ee9-104">Schema (AD DS)</span></span>

<span data-ttu-id="d0ee9-105">Active Directory schema viene implementato come un set di istanze della classe di oggetti archiviate nella directory.</span><span class="sxs-lookup"><span data-stu-id="d0ee9-105">Active Directory schema is implemented as a set of object class instances stored in the directory.</span></span> <span data-ttu-id="d0ee9-106">Si tratta di un comportamento molto diverso rispetto a quello di molte directory che dispongono di uno schema, che però viene archiviato come file di testo letto all'avvio.</span><span class="sxs-lookup"><span data-stu-id="d0ee9-106">This is very different than many directories that have a schema but store it as a text file read at startup.</span></span> <span data-ttu-id="d0ee9-107">L'archiviazione dello schema nella directory presenta molti vantaggi.</span><span class="sxs-lookup"><span data-stu-id="d0ee9-107">Storing the schema in the directory has many advantages.</span></span> <span data-ttu-id="d0ee9-108">Ad esempio, le applicazioni utente possono leggerlo per individuare gli oggetti e le proprietà disponibili.</span><span class="sxs-lookup"><span data-stu-id="d0ee9-108">For example, user applications can read it to discover what objects and properties are available.</span></span>

<span data-ttu-id="d0ee9-109">Active Directory schema può essere aggiornato dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="d0ee9-109">Active Directory schema can be updated dynamically.</span></span> <span data-ttu-id="d0ee9-110">Ovvero, un'applicazione può estendere lo schema con nuovi attributi e classi e utilizzare immediatamente le estensioni.</span><span class="sxs-lookup"><span data-stu-id="d0ee9-110">That is, an application can extend the schema with new attributes and classes and use the extensions immediately.</span></span> <span data-ttu-id="d0ee9-111">Gli aggiornamenti dello schema vengono eseguiti creando o modificando gli oggetti dello schema archiviati nella directory.</span><span class="sxs-lookup"><span data-stu-id="d0ee9-111">Schema updates are accomplished by creating or modifying the schema objects stored in the directory.</span></span> <span data-ttu-id="d0ee9-112">Analogamente a ogni oggetto in Active Directory, gli elenchi di controllo di accesso (ACL) proteggono gli oggetti dello schema, quindi gli utenti autorizzati possono solo modificare lo schema.</span><span class="sxs-lookup"><span data-stu-id="d0ee9-112">Like every object in Active Directory, access-control lists (ACLs) protect schema objects, so authorized users only may alter the schema.</span></span>

<span data-ttu-id="d0ee9-113">Per ulteriori informazioni, vedere [Active Directory schema](active-directory-schema.md).</span><span class="sxs-lookup"><span data-stu-id="d0ee9-113">For more information, see [Active Directory Schema](active-directory-schema.md).</span></span>

 

 




