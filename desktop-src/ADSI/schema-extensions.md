---
title: Estensioni dello schema
description: L'architettura dello schema ADSI fornisce che le nuove classi dello schema possono essere aggiunte al contenitore della classe dello schema e nuove proprietà a un oggetto della classe di schema esistente in fase di esecuzione.
ms.assetid: 935d39ca-cfb9-4aa3-aa0e-b614f7b359f2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b86491966e2bfddbef72d68d7a96869448c38188
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116673"
---
# <a name="schema-extensions"></a><span data-ttu-id="6b91a-103">Estensioni dello schema</span><span class="sxs-lookup"><span data-stu-id="6b91a-103">Schema Extensions</span></span>

<span data-ttu-id="6b91a-104">L'architettura dello schema ADSI fornisce che le nuove classi dello schema possono essere aggiunte al contenitore della classe dello schema e nuove proprietà a un oggetto della classe di schema esistente in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="6b91a-104">The architecture of the ADSI schema provides that new schema classes can be added to the schema class container and new properties to an existing schema class object at run time.</span></span> <span data-ttu-id="6b91a-105">La seconda possibilità non richiede alcun nuovo codice.</span><span class="sxs-lookup"><span data-stu-id="6b91a-105">The latter ability requires no new code.</span></span> <span data-ttu-id="6b91a-106">Si tratta di una funzionalità importante per gli spazi dei nomi che consentono Extensible Directory Services.</span><span class="sxs-lookup"><span data-stu-id="6b91a-106">This is an important feature for namespaces that allow extensible directory services.</span></span> <span data-ttu-id="6b91a-107">Il componente provider deve consentire questa estendibilità e stabilire dove accedere e archiviare l'istanza della classe e i valori delle relative proprietà.</span><span class="sxs-lookup"><span data-stu-id="6b91a-107">The provider component must allow for this extensibility and know where to access and store the class instance and the values of its properties.</span></span> <span data-ttu-id="6b91a-108">In un tipico servizio directory estendibile, queste informazioni vengono archiviate nel database del servizio directory in modo analogo a qualsiasi altra definizione di classe e proprietà dello schema.</span><span class="sxs-lookup"><span data-stu-id="6b91a-108">In a typical extensible directory service, this information is stored in the directory service database in the same manner as any other schema class and property definitions.</span></span>

> [!Note]  
> <span data-ttu-id="6b91a-109">Nella terminologia dell'interfaccia COM, solo le proprietà possono essere aggiunte a una classe di schema esistente, non a metodi.</span><span class="sxs-lookup"><span data-stu-id="6b91a-109">In COM interface terminology, only properties can be added to an existing schema class, not methods.</span></span> <span data-ttu-id="6b91a-110">L'aggiunta di un nuovo metodo richiederebbe l'aggiunta di una nuova implementazione del metodo e richiederebbe quindi altro codice.</span><span class="sxs-lookup"><span data-stu-id="6b91a-110">Adding a new method would require adding a new implementation of that method and thus require additional code.</span></span>

 

<span data-ttu-id="6b91a-111">Per un esempio di uno schema del provider specifico, vedere [gestione degli schemi](schema-management.md).</span><span class="sxs-lookup"><span data-stu-id="6b91a-111">For an example of a specific provider schema, see [Schema Management](schema-management.md).</span></span>

 

 




