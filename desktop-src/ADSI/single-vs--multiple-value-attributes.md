---
title: Attributi singolo e più valori
description: Gli attributi che possono esistere in una directory sono in genere definiti nello schema per la directory.
ms.assetid: ea06ca66-6407-448f-8238-c8de5353663b
ms.tgt_platform: multiple
keywords:
- ADSI singolo e più attributi di valore
- attributi ADSI, Single rispetto a più attributi di valore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cdfabd985be3446e4f104d300d75f891ef0ce60
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044051"
---
# <a name="single-vs-multiple-value-attributes"></a><span data-ttu-id="6f88a-105">Attributi singolo e più valori</span><span class="sxs-lookup"><span data-stu-id="6f88a-105">Single vs. Multiple Value Attributes</span></span>

<span data-ttu-id="6f88a-106">Gli attributi che possono esistere in una directory sono in genere definiti nello schema per la directory.</span><span class="sxs-lookup"><span data-stu-id="6f88a-106">The attributes that can exist in a directory are typically defined in the schema for the directory.</span></span> <span data-ttu-id="6f88a-107">La definizione dello schema di un attributo specifica un numero di caratteristiche dell'attributo, ad esempio il tipo di dati e se un'istanza dell'attributo può avere più valori.</span><span class="sxs-lookup"><span data-stu-id="6f88a-107">The schema definition of an attribute specifies a number of characteristics of the attribute, such as the data type and whether an instance of the attribute can have multiple values.</span></span>

<span data-ttu-id="6f88a-108">Un'istanza di un attributo a valore singolo può contenere un solo valore.</span><span class="sxs-lookup"><span data-stu-id="6f88a-108">An instance of a single-valued attribute can contain a single value.</span></span> <span data-ttu-id="6f88a-109">Un'istanza di un attributo multivalore può contenere un solo valore o più valori.</span><span class="sxs-lookup"><span data-stu-id="6f88a-109">An instance of a multivalued attribute can contain either a single value or multiple values.</span></span> <span data-ttu-id="6f88a-110">Active Directory non crea attributi con valori vuoti, l'attributo contiene un valore valido o non esiste nell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6f88a-110">Active Directory does not create attributes with empty values—either the attribute contains a valid value or it does not exist on the object.</span></span>

> [!Note]  
> <span data-ttu-id="6f88a-111">In Active Directory e nella maggior parte degli altri server LDAP, l'ordine dei valori in un attributo multivalore non è definito.</span><span class="sxs-lookup"><span data-stu-id="6f88a-111">In Active Directory and most other LDAP servers, the order of values in a multi-valued attribute is undefined.</span></span> <span data-ttu-id="6f88a-112">Inoltre, ogni valore di un attributo multivalore deve essere univoco.</span><span class="sxs-lookup"><span data-stu-id="6f88a-112">Also, each value of a multi-valued attribute must be unique.</span></span>

 

<span data-ttu-id="6f88a-113">In genere, ADSI carica i dati dello schema se la directory supporta uno schema, come Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6f88a-113">ADSI normally loads schema data if your directory supports a schema, as Active Directory does.</span></span> <span data-ttu-id="6f88a-114">Poiché ADSI conosce la sintassi degli attributi nello schema, non è necessario specificare il tipo di attributo durante l'accesso.</span><span class="sxs-lookup"><span data-stu-id="6f88a-114">Because ADSI knows the syntax of attributes in the schema, you are not required to specify the attribute type when accessing it.</span></span> <span data-ttu-id="6f88a-115">ADSI esegue il marshalling dei valori di attributo nel tipo di dati appropriato come definito nello schema.</span><span class="sxs-lookup"><span data-stu-id="6f88a-115">ADSI marshals attribute values to the appropriate data type as defined in the schema.</span></span>

<span data-ttu-id="6f88a-116">Se la directory non dispone di alcuno schema, specificare il tipo di dati per l'accesso a un attributo.</span><span class="sxs-lookup"><span data-stu-id="6f88a-116">If your directory has no schema, supply the data type when accessing an attribute.</span></span>

> [!Note]  
> <span data-ttu-id="6f88a-117">Active Directory, Exchange, Windows NT 4,0 e il server del sito hanno tutti uno schema.</span><span class="sxs-lookup"><span data-stu-id="6f88a-117">Active Directory, Exchange, Windows NT 4.0, and Site Server all have a schema.</span></span> <span data-ttu-id="6f88a-118">Inoltre, Active Directory dispone di uno schema estendibile.</span><span class="sxs-lookup"><span data-stu-id="6f88a-118">In addition, Active Directory has an extensible schema.</span></span>

 

 

 




