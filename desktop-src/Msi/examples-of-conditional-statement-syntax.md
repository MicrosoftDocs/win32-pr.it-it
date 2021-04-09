---
description: Di seguito vengono fornite alcune istanze comuni di istruzioni condizionali. Per altre informazioni, vedere Sintassi dell'istruzione condizionale.
ms.assetid: 8b6bae7a-20ae-494c-bd96-66bd537c8630
title: Esempi di sintassi di istruzioni condizionali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca91a2b3e89160fad19ad5d9b1c6a3d33929e5d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967190"
---
# <a name="examples-of-conditional-statement-syntax"></a><span data-ttu-id="42aae-104">Esempi di sintassi di istruzioni condizionali</span><span class="sxs-lookup"><span data-stu-id="42aae-104">Examples of Conditional Statement Syntax</span></span>

<span data-ttu-id="42aae-105">Di seguito vengono fornite alcune istanze comuni di istruzioni condizionali.</span><span class="sxs-lookup"><span data-stu-id="42aae-105">The following provides some common instances of conditional statements.</span></span> <span data-ttu-id="42aae-106">Per altre informazioni, vedere [sintassi dell'istruzione condizionale](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="42aae-106">For more information, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

## <a name="run-action-on-removal"></a><span data-ttu-id="42aae-107">Eseguire un'azione durante la rimozione.</span><span class="sxs-lookup"><span data-stu-id="42aae-107">Run action on removal.</span></span>

<span data-ttu-id="42aae-108">Per informazioni, vedere [condizionare le azioni da eseguire durante la rimozione](conditioning-actions-to-run-during-removal.md).</span><span class="sxs-lookup"><span data-stu-id="42aae-108">For information, see [Conditioning Actions to Run During Removal](conditioning-actions-to-run-during-removal.md).</span></span>

## <a name="run-action-only-if-the-product-has-not-been-installed"></a><span data-ttu-id="42aae-109">Eseguire l'azione solo se il prodotto non è stato installato.</span><span class="sxs-lookup"><span data-stu-id="42aae-109">Run action only if the product has not been installed.</span></span>

``` syntax
NOT Installed
```

## <a name="run-action-only-if-the-product-will-be-installed-local-do-not-run-action-on-a-reinstallation"></a><span data-ttu-id="42aae-110">Eseguire l'azione solo se il prodotto verrà installato localmente.</span><span class="sxs-lookup"><span data-stu-id="42aae-110">Run action only if the product will be installed local.</span></span> <span data-ttu-id="42aae-111">Non eseguire un'azione su una reinstallazione.</span><span class="sxs-lookup"><span data-stu-id="42aae-111">Do not run action on a reinstallation.</span></span>

``` syntax
(&FeatureName=3) AND NOT(!FeatureName=3)
```

<span data-ttu-id="42aae-112">Il termine "&FeatureName = 3" indica che l'azione prevede l'installazione della funzionalità locale.</span><span class="sxs-lookup"><span data-stu-id="42aae-112">The term "&FeatureName=3" means the action is to install the feature local.</span></span> <span data-ttu-id="42aae-113">Il termine "NOT (! FeatureName = 3) "indica che la funzionalità non è installata localmente.</span><span class="sxs-lookup"><span data-stu-id="42aae-113">The term "NOT(!FeatureName=3)" means the feature is not installed local.</span></span>

## <a name="run-action-only-if-the-feature-will-be-uninstalled"></a><span data-ttu-id="42aae-114">Eseguire l'azione solo se la funzionalità verrà disinstallata.</span><span class="sxs-lookup"><span data-stu-id="42aae-114">Run action only if the feature will be uninstalled.</span></span>

``` syntax
(&FeatureName=2) AND (!FeatureName=3)
```

<span data-ttu-id="42aae-115">Questa condizione controlla solo la presenza di una transizione della funzionalità da uno stato installato locale a quello assente.</span><span class="sxs-lookup"><span data-stu-id="42aae-115">This condition only checks for a transition of the feature from an installed state of local to the absent state.</span></span>

## <a name="run-action-only-if-the-component-was-installed-local-but-is-transitioning-out-of-state"></a><span data-ttu-id="42aae-116">Eseguire l'azione solo se il componente è stato installato localmente, ma è in fase di transizione allo stato.</span><span class="sxs-lookup"><span data-stu-id="42aae-116">Run action only if the component was installed local, but is transitioning out of state.</span></span>

``` syntax
(?ComponentName=3) AND ($ComponentName=2 OR $ComponentName=4)
```

<span data-ttu-id="42aae-117">Il termine "? ComponetName = 3 "indica che il componente è installato localmente.</span><span class="sxs-lookup"><span data-stu-id="42aae-117">The term "?ComponetName=3" means the component is installed local.</span></span> <span data-ttu-id="42aae-118">Il termine "$ComponentName = 2" indica che lo stato dell'azione nel componente è assente.</span><span class="sxs-lookup"><span data-stu-id="42aae-118">The term "$ComponentName=2" means that the action state on the component is Absent.</span></span> <span data-ttu-id="42aae-119">Il termine "$ComponentName = 4" indica che lo stato dell'azione nel componente viene eseguito dall'origine.</span><span class="sxs-lookup"><span data-stu-id="42aae-119">The term "$ComponentName=4" means that the action state on the component is run from source.</span></span> <span data-ttu-id="42aae-120">Si noti che lo stato di un'azione di annuncio non è valido per un componente.</span><span class="sxs-lookup"><span data-stu-id="42aae-120">Note that an action state of advertise is not valid for a component.</span></span>

## <a name="run-action-only-on-the-reinstallation-of-a-component"></a><span data-ttu-id="42aae-121">Eseguire un'azione solo sulla reinstallazione di un componente.</span><span class="sxs-lookup"><span data-stu-id="42aae-121">Run action only on the reinstallation of a component.</span></span>

``` syntax
?ComponentName=$ComponentName
```

## <a name="run-action-only-when-a-particular-patch-is-applied"></a><span data-ttu-id="42aae-122">Eseguire un'azione solo quando viene applicata una particolare patch.</span><span class="sxs-lookup"><span data-stu-id="42aae-122">Run action only when a particular patch is applied.</span></span>

``` syntax
PATCH AND PATCH >< MEDIASRCPROPNAME
```

<span data-ttu-id="42aae-123">Per ulteriori informazioni, vedere la sezione Osservazioni nella pagina delle proprietà della [**patch**](patch.md) .</span><span class="sxs-lookup"><span data-stu-id="42aae-123">For more information, see the Remarks section on the [**PATCH**](patch.md) property page.</span></span>

 

 



