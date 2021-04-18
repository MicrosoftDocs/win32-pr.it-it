---
description: Per impostazione predefinita, le trasformazioni che non sono state protette come descritto in trasformazioni protette sono trasformazioni non protette.
ms.assetid: feace6c3-7828-44d0-8d2b-482a02e8e0c0
title: Trasformazioni non protette
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6743898142197d87d4e3fef5d0f48778f6261ff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319416"
---
# <a name="unsecured-transforms"></a><span data-ttu-id="2bfb3-103">Trasformazioni non protette</span><span class="sxs-lookup"><span data-stu-id="2bfb3-103">Unsecured Transforms</span></span>

<span data-ttu-id="2bfb3-104">Per impostazione predefinita, le trasformazioni che non sono state protette come descritto in [trasformazioni protette](secured-transforms.md) sono trasformazioni non protette.</span><span class="sxs-lookup"><span data-stu-id="2bfb3-104">Transforms that have not been secured as described in [Secured Transforms](secured-transforms.md) are unsecured transforms by default.</span></span>

<span data-ttu-id="2bfb3-105">Per applicare una trasformazione non protetta durante l'installazione di un pacchetto, passare i nomi dei file di trasformazione nella proprietà [**TRANSforms**](transforms.md) o nella stringa della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="2bfb3-105">To apply an unsecured transform when installing a package, pass the transform file names in the [**TRANSFORMS**](transforms.md) property or command line string.</span></span> <span data-ttu-id="2bfb3-106">Non iniziare la stringa con i caratteri @ o \| o impostare il [criterio TRANSFORMSSECURE](transformssecure-policy.md) o la proprietà [**TRANSFORMSSECURE**](transformssecure.md) .</span><span class="sxs-lookup"><span data-stu-id="2bfb3-106">Do not begin the string with the @ or \| characters or set the [TransformsSecure policy](transformssecure-policy.md) or the [**TRANSFORMSSECURE**](transformssecure.md) property.</span></span> <span data-ttu-id="2bfb3-107">Si noti che non è possibile combinare trasformazioni non protette e [trasformazioni protette](secured-transforms.md) nello stesso elenco di trasformazioni.</span><span class="sxs-lookup"><span data-stu-id="2bfb3-107">Note that you cannot combine unsecured transforms and [secured transforms](secured-transforms.md) in the same transforms list.</span></span>

<span data-ttu-id="2bfb3-108">Se il pacchetto viene installato o annunciato nel [contesto di installazione](installation-context.md)per utente e presenta trasformazioni non protette, il programma di installazione salva l'origine di trasformazione nella cartella Application Data nel profilo dell'utente.</span><span class="sxs-lookup"><span data-stu-id="2bfb3-108">If the package is installed or advertised in the per-user [installation context](installation-context.md), and has unsecured transforms, the installer saves the transform source in the Application Data folder in the user's profile.</span></span> <span data-ttu-id="2bfb3-109">Questo consente a un utente di mantenere la personalizzazione di un prodotto durante il passaggio da un computer all'altra.</span><span class="sxs-lookup"><span data-stu-id="2bfb3-109">This enables a user to maintain their customization of a product while moving between computers.</span></span>

<span data-ttu-id="2bfb3-110">Se il pacchetto viene installato o annunciato nel [contesto di installazione](installation-context.md)per computer e utilizza trasformazioni non protette, il programma di installazione salva l'origine di trasformazione nella cartella% windir% \\ Installer.</span><span class="sxs-lookup"><span data-stu-id="2bfb3-110">If the package is installed or advertised in the per-machine [installation context](installation-context.md), and uses unsecured transforms, the installer saves the transform source in the %windir%\\Installer folder.</span></span>

<span data-ttu-id="2bfb3-111">Durante una prima installazione del pacchetto, il programma di installazione cerca innanzitutto la trasformazione nell'origine fornita dalla proprietà [**TRANSforms**](transforms.md) o dalla stringa della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="2bfb3-111">During a first-time installation of the package, the installer first searches for the transform at the source supplied by the [**TRANSFORMS**](transforms.md) property or command line string.</span></span> <span data-ttu-id="2bfb3-112">Se l'origine non è disponibile, il programma di installazione cerca la trasformazione in corrispondenza dell'origine del pacchetto accanto al file con estensione msi.</span><span class="sxs-lookup"><span data-stu-id="2bfb3-112">If this source is unavailable, the installer then searches for the transform at the source of the package next to the .msi file.</span></span>

<span data-ttu-id="2bfb3-113">Durante un' [installazione di manutenzione](maintenance-installation.md), il programma di installazione cerca la trasformazione nel percorso della cache.</span><span class="sxs-lookup"><span data-stu-id="2bfb3-113">During a [maintenance installation](maintenance-installation.md), the installer searches for the transform at the cache location.</span></span> <span data-ttu-id="2bfb3-114">Se la copia della trasformazione memorizzata nella cache non è più disponibile, il programma di installazione cerca la trasformazione in corrispondenza dell'origine del pacchetto accanto al file con estensione msi.</span><span class="sxs-lookup"><span data-stu-id="2bfb3-114">If the cached copy of the transform becomes unavailable, the installer searches for the transform at the source of the package next to the .msi file.</span></span>

<span data-ttu-id="2bfb3-115">Per altre informazioni, vedere [applicazione di trasformazioni](applying-transforms.md) e [resilienza dell'origine](source-resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="2bfb3-115">For more information, see [Applying Transforms](applying-transforms.md) and [Source Resiliency](source-resiliency.md).</span></span>

 

 



