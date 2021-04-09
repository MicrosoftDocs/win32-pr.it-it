---
description: Nelle sezioni seguenti viene descritto l'utilizzo delle proprietà predefinite del programma di installazione e delle proprietà aggiuntive definite dall'autore del pacchetto.
ms.assetid: 5a2f1cd4-2bbd-414a-a814-8b9fdab434b4
title: Utilizzo delle proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edab44953f6ccd210d5baa3c446363a1131dc745
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129359"
---
# <a name="using-properties"></a><span data-ttu-id="8a52d-103">Utilizzo delle proprietà</span><span class="sxs-lookup"><span data-stu-id="8a52d-103">Using Properties</span></span>

<span data-ttu-id="8a52d-104">Nelle sezioni seguenti viene descritto l'utilizzo delle proprietà predefinite del programma di installazione e delle proprietà aggiuntive definite dall'autore del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="8a52d-104">The following sections describe using the built-in installer properties and additional properties defined by the package author.</span></span> <span data-ttu-id="8a52d-105">Le proprietà possono essere proprietà [pubbliche](public-properties.md) o [proprietà private](private-properties.md).</span><span class="sxs-lookup"><span data-stu-id="8a52d-105">Properties can be either [public properties](public-properties.md) or [private properties](private-properties.md).</span></span> <span data-ttu-id="8a52d-106">Ogni proprietà che deve essere definita al momento dell'inizializzazione del programma di installazione deve avere il nome e il valore iniziale elencati nella [tabella delle proprietà](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="8a52d-106">Every property that needs to be defined upon initialization of the installer must have its name and initial value listed in the [Property table](property-table.md).</span></span> <span data-ttu-id="8a52d-107">Le proprietà con un valore null non sono elencate nella tabella delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="8a52d-107">Properties having a Null value are not listed in the Property table.</span></span> <span data-ttu-id="8a52d-108">È possibile ottenere o impostare proprietà da programmi e azioni personalizzate e impostare proprietà pubbliche dalla riga di comando.</span><span class="sxs-lookup"><span data-stu-id="8a52d-108">You can get or set properties from programs and custom actions and set public properties from the command line.</span></span> <span data-ttu-id="8a52d-109">Il processo di installazione può essere modificato usando le proprietà nelle istruzioni condizionali.</span><span class="sxs-lookup"><span data-stu-id="8a52d-109">The installation process can be modified by using properties in conditional statements.</span></span>

[<span data-ttu-id="8a52d-110">Restrizioni per i nomi delle proprietà</span><span class="sxs-lookup"><span data-stu-id="8a52d-110">Restrictions on Property Names</span></span>](restrictions-on-property-names.md)

[<span data-ttu-id="8a52d-111">Inizializzazione dei valori delle proprietà</span><span class="sxs-lookup"><span data-stu-id="8a52d-111">Initialization of Property Values</span></span>](initialization-of-property-values.md)

[<span data-ttu-id="8a52d-112">Recupero e impostazione delle proprietà</span><span class="sxs-lookup"><span data-stu-id="8a52d-112">Getting and Setting Properties</span></span>](getting-and-setting-properties.md)

[<span data-ttu-id="8a52d-113">Uso delle proprietà nelle istruzioni condizionali</span><span class="sxs-lookup"><span data-stu-id="8a52d-113">Using Properties in Conditional Statements</span></span>](using-properties-in-conditional-statements.md)

[<span data-ttu-id="8a52d-114">Utilizzo di una proprietà di directory in un percorso</span><span class="sxs-lookup"><span data-stu-id="8a52d-114">Using a Directory Property in a Path</span></span>](using-a-directory-property-in-a-path.md)

> [!Note]  
> <span data-ttu-id="8a52d-115">Non usare le proprietà per le password o altre informazioni che devono rimanere sicure.</span><span class="sxs-lookup"><span data-stu-id="8a52d-115">Do not use properties for passwords or other information that must remain secure.</span></span> <span data-ttu-id="8a52d-116">Il programma di installazione può scrivere il valore di una proprietà creato nella tabella delle proprietà o creato in fase di esecuzione in un log o nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="8a52d-116">The installer may write the value of a property authored into the Property table or created at runtime into a log or the system registry.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="8a52d-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8a52d-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a52d-118">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="8a52d-118">About Properties</span></span>](about-properties.md)
</dt> <dt>

[<span data-ttu-id="8a52d-119">Riferimento alla proprietà</span><span class="sxs-lookup"><span data-stu-id="8a52d-119">Property Reference</span></span>](property-reference.md)
</dt> </dl>

 

 



