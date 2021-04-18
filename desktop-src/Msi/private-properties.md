---
description: Le proprietà private vengono utilizzate internamente dal programma di installazione e i rispettivi valori devono essere immessi nel database dall'autore del pacchetto di installazione o impostati dal programma di installazione durante l'installazione ai valori determinati dall'ambiente operativo.
ms.assetid: 7d574bf0-bcb3-4e19-9659-fe741ace9f21
title: Proprietà private
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab7b0196be016fecb625e139f308219582620d40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315468"
---
# <a name="private-properties"></a><span data-ttu-id="8dd93-103">Proprietà private</span><span class="sxs-lookup"><span data-stu-id="8dd93-103">Private Properties</span></span>

<span data-ttu-id="8dd93-104">Le proprietà private vengono utilizzate internamente dal programma di installazione e i rispettivi valori devono essere immessi nel database dall'autore del pacchetto di installazione o impostati dal programma di installazione durante l'installazione ai valori determinati dall'ambiente operativo.</span><span class="sxs-lookup"><span data-stu-id="8dd93-104">Private properties are used internally by the installer and their values must be entered into the database by the author of the installation package or set by the installer during the installation to values determined by the operating environment.</span></span> <span data-ttu-id="8dd93-105">L'unico modo in cui un utente può interagire con le proprietà private è tramite [gli eventi di controllo](control-events.md) nell'interfaccia utente creata del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="8dd93-105">The only way a user can interact with private properties is through [Control Events](control-events.md) in the package's authored user interface.</span></span> <span data-ttu-id="8dd93-106">I nomi delle proprietà private devono includere lettere minuscole.</span><span class="sxs-lookup"><span data-stu-id="8dd93-106">Private property names must include lowercase letters.</span></span> <span data-ttu-id="8dd93-107">Vedere [restrizioni sui nomi di proprietà](restrictions-on-property-names.md).</span><span class="sxs-lookup"><span data-stu-id="8dd93-107">See [Restrictions on Property Names](restrictions-on-property-names.md).</span></span>

<span data-ttu-id="8dd93-108">Le proprietà private in genere descrivono l'ambiente operativo.</span><span class="sxs-lookup"><span data-stu-id="8dd93-108">Private properties commonly describe the operating environment.</span></span> <span data-ttu-id="8dd93-109">Se, ad esempio, l'installazione viene eseguita in una piattaforma Windows, il programma di installazione imposta la proprietà [**WindowsFolder**](windowsfolder.md) sul valore specificato nella tabella delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="8dd93-109">For example, if the installation is run on a Windows platform, the installer sets the [**WindowsFolder**](windowsfolder.md) property to the value specified in the Property table.</span></span>

<span data-ttu-id="8dd93-110">Non è possibile eseguire l'override dei valori delle proprietà private in una riga di comando.</span><span class="sxs-lookup"><span data-stu-id="8dd93-110">Private property values cannot be overridden at a command line.</span></span> <span data-ttu-id="8dd93-111">Per cancellare una proprietà privata da un'installazione, lasciarla fuori dalla [tabella delle proprietà](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="8dd93-111">To clear a private property from an installation, leave it out of the [Property table](property-table.md).</span></span> <span data-ttu-id="8dd93-112">In Windows XP e Windows 2000 non è possibile impostare una proprietà privata nella fase dell'interfaccia utente dell'installazione, quindi passare il valore alla fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="8dd93-112">On Windows XP, and Windows 2000 you cannot set a private property in the user interface phase of the installation and then pass the value to the execution phase.</span></span>

<span data-ttu-id="8dd93-113">Per un elenco di tutte le proprietà private standard usate dal programma di installazione, vedere [riferimento alle proprietà](property-reference.md).</span><span class="sxs-lookup"><span data-stu-id="8dd93-113">For a list of all the standard private properties used by the installer, see [Property Reference](property-reference.md).</span></span> <span data-ttu-id="8dd93-114">È possibile definire una proprietà privata personalizzata immettendo il nome e il valore iniziale della proprietà nella tabella delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="8dd93-114">You can define a custom private property by entering the property's name and initial value in the Property table.</span></span> <span data-ttu-id="8dd93-115">I nomi delle proprietà private devono sempre includere lettere minuscole.</span><span class="sxs-lookup"><span data-stu-id="8dd93-115">Private property names must always include lowercase letters.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8dd93-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8dd93-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8dd93-117">Proprietà pubbliche</span><span class="sxs-lookup"><span data-stu-id="8dd93-117">Public Properties</span></span>](public-properties.md)
</dt> </dl>

 

 



