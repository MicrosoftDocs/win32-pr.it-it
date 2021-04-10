---
description: Windows Installer possibile configurare l'installazione del software utilizzando i valori delle variabili definite in un pacchetto di installazione o dall'utente.
ms.assetid: b7b715e7-e92c-4b84-b60d-a0ff8412749b
title: Informazioni sulle proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dc5d8154533cfebf4163983a149a547372ef4a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227228"
---
# <a name="about-properties"></a><span data-ttu-id="b9fb6-103">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b9fb6-103">About Properties</span></span>

<span data-ttu-id="b9fb6-104">Windows Installer possibile configurare l'installazione del software utilizzando i valori delle variabili definite in un pacchetto di installazione o dall'utente.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-104">Windows Installer can configure software installation by using the values of variables defined in an installation package or by the user.</span></span>

<span data-ttu-id="b9fb6-105">Windows Installer usa tre categorie di variabili globali durante un'installazione:</span><span class="sxs-lookup"><span data-stu-id="b9fb6-105">Windows Installer uses three categories of global variables during an installation:</span></span>

-   <span data-ttu-id="b9fb6-106">Proprietà private: il programma di installazione utilizza internamente le proprietà private e i relativi valori devono essere creati nel database di installazione o impostati su valori determinati dall'ambiente operativo.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-106">Private properties: The installer uses private properties internally and their values must be authored into the installation database or set to values determined by the operating environment.</span></span>
-   <span data-ttu-id="b9fb6-107">Proprietà pubbliche: le proprietà pubbliche possono essere create nel database e modificate da un utente o da un amministratore di sistema nella riga di comando, applicando una trasformazione o interagendo con un'interfaccia utente creata.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-107">Public properties: Public properties can be authored into the database and changed by a user or system administrator on the command line, by applying a transform, or by interacting with an authored user interface.</span></span>
-   <span data-ttu-id="b9fb6-108">Proprietà pubbliche limitate: per motivi di sicurezza, l'autore di un pacchetto di installazione può limitare le proprietà pubbliche che un utente può modificare.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-108">Restricted public properties: For security purposes, the author of an installation package can restrict the public properties a user can change.</span></span>

<span data-ttu-id="b9fb6-109">Non è necessario definire tutte le proprietà in ogni pacchetto. è necessario definire un piccolo set di proprietà obbligatorie in ogni pacchetto.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-109">Not all properties need to be defined in every package, there is a small set of required properties that must be defined in every package.</span></span> <span data-ttu-id="b9fb6-110">Il programma di installazione imposta i valori delle proprietà in un ordine di precedenza particolare.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-110">The installer sets the values of properties in a particular order of precedence.</span></span>

[<span data-ttu-id="b9fb6-111">Proprietà private</span><span class="sxs-lookup"><span data-stu-id="b9fb6-111">Private Properties</span></span>](private-properties.md)

[<span data-ttu-id="b9fb6-112">Proprietà pubbliche</span><span class="sxs-lookup"><span data-stu-id="b9fb6-112">Public Properties</span></span>](public-properties.md)

[<span data-ttu-id="b9fb6-113">Proprietà pubbliche limitate</span><span class="sxs-lookup"><span data-stu-id="b9fb6-113">Restricted Public Properties</span></span>](restricted-public-properties.md)

[<span data-ttu-id="b9fb6-114">Proprietà obbligatorie</span><span class="sxs-lookup"><span data-stu-id="b9fb6-114">Required Properties</span></span>](required-properties.md)

[<span data-ttu-id="b9fb6-115">Ordine di precedenza delle proprietà</span><span class="sxs-lookup"><span data-stu-id="b9fb6-115">Order of Property Precedence</span></span>](order-of-property-precedence.md)

## <a name="related-topics"></a><span data-ttu-id="b9fb6-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b9fb6-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9fb6-117">Utilizzo delle proprietà</span><span class="sxs-lookup"><span data-stu-id="b9fb6-117">Using Properties</span></span>](using-properties.md)
</dt> <dt>

[<span data-ttu-id="b9fb6-118">Riferimento alla proprietà</span><span class="sxs-lookup"><span data-stu-id="b9fb6-118">Property Reference</span></span>](property-reference.md)
</dt> </dl>

 

 



