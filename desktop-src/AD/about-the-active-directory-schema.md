---
title: Informazioni sullo schema di Active Directory
description: Ogni oggetto in Active Directory Domain Services è un'istanza di una classe di oggetti definita nello schema di Active Directory.
ms.assetid: 8fc9cd2d-8fed-4fda-918c-79b01f9a19bb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f55513b359a7ef293b005d93a20ac43f470d515
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855206"
---
# <a name="about-the-active-directory-schema"></a><span data-ttu-id="5c0a5-103">Informazioni sullo schema di Active Directory</span><span class="sxs-lookup"><span data-stu-id="5c0a5-103">About the Active Directory Schema</span></span>

<span data-ttu-id="5c0a5-104">Ogni oggetto in Active Directory Domain Services è un'istanza di una classe di oggetti definita nello schema di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5c0a5-104">Every object in Active Directory Domain Services is an instance of an object class defined in the Active Directory schema.</span></span> <span data-ttu-id="5c0a5-105">Una classe di oggetti rappresenta una categoria di oggetti, quali utenti, stampanti o applicazioni, che condividono un insieme di caratteristiche comuni.</span><span class="sxs-lookup"><span data-stu-id="5c0a5-105">An object class represents a category of objects, such as users, printers, or application programs, that share a set of common characteristics.</span></span> <span data-ttu-id="5c0a5-106">La definizione di ciascuna classe di oggetti contiene l'elenco degli attributi che possono essere utilizzati per descrivere le istanze della classe.</span><span class="sxs-lookup"><span data-stu-id="5c0a5-106">The definition for each object class contains a list of the attributes that can be used to describe instances of the class.</span></span> <span data-ttu-id="5c0a5-107">Ad esempio, la classe User dispone di attributi quali **givenName**, **surname** e **streetAddress**.</span><span class="sxs-lookup"><span data-stu-id="5c0a5-107">For example, the User class has attributes such as **givenName**, **surname**, and **streetAddress**.</span></span> <span data-ttu-id="5c0a5-108">L'elenco di attributi per una classe è diviso in quelli che un oggetto di tale classe deve contenere e attributi aggiuntivi che possono essere contenuti in un oggetto.</span><span class="sxs-lookup"><span data-stu-id="5c0a5-108">The list of attributes for a class is divided into those that an object of that class must contain, and additional attributes that an object may contain.</span></span> <span data-ttu-id="5c0a5-109">La directory viene disposta in una gerarchia. la definizione di ogni classe elenca anche le classi i cui oggetti possono essere elementi padre di oggetti di una determinata classe, che controlla la forma della gerarchia di directory.</span><span class="sxs-lookup"><span data-stu-id="5c0a5-109">The directory is arranged in a hierarchy; the definition of each class also lists the classes whose objects can be parents of objects of a given class—this controls the shape of the directory hierarchy.</span></span>

<span data-ttu-id="5c0a5-110">Lo schema definisce formalmente anche ogni attributo.</span><span class="sxs-lookup"><span data-stu-id="5c0a5-110">The schema also formally defines each attribute.</span></span> <span data-ttu-id="5c0a5-111">La definizione per ogni attributo include identificatori univoci per l'attributo, la sintassi per l'attributo (ovvero il tipo di dati per i valori dell'attributo), i limiti di intervallo facoltativi per i valori di attributo, se l'attributo può avere un solo valore o più valori e se l'attributo è indicizzato.</span><span class="sxs-lookup"><span data-stu-id="5c0a5-111">The definition for each attribute includes unique identifiers for the attribute, the syntax for the attribute (that is, the data type for the attribute's values), optional range limits for the attribute values, whether the attribute can have only one value or multiple values, and whether the attribute is indexed.</span></span> <span data-ttu-id="5c0a5-112">Lo schema di directory definisce ogni attributo una sola volta, ovvero le definizioni delle classi di oggetti contengono riferimenti agli attributi definiti nello schema.</span><span class="sxs-lookup"><span data-stu-id="5c0a5-112">The directory schema defines each attribute exactly once—object class definitions contain references to the attributes defined in the schema.</span></span> <span data-ttu-id="5c0a5-113">Ad esempio, l'attributo "Description" viene definito una sola volta e vi viene fatto riferimento da molte classi di oggetti.</span><span class="sxs-lookup"><span data-stu-id="5c0a5-113">For example, the "description" attribute is defined only once and is referenced by many object classes.</span></span> <span data-ttu-id="5c0a5-114">Questa operazione è diversa rispetto a uno schema di database relazionale, in cui gli "attributi" (colonne) sono definiti separatamente per ogni tabella.</span><span class="sxs-lookup"><span data-stu-id="5c0a5-114">This is different than a relational database schema, where the "attributes" (columns) are separately defined for each table.</span></span>

 

 




