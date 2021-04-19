---
description: ICE97 verifica che due componenti non Isolino un componente condiviso nella stessa directory.
ms.assetid: 76eeb238-02a1-43c1-a3d7-5178e3c3eaee
title: ICE97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34c41701ce04c0071d6599f888083dfbea4bfc0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313814"
---
# <a name="ice97"></a><span data-ttu-id="3d37e-103">ICE97</span><span class="sxs-lookup"><span data-stu-id="3d37e-103">ICE97</span></span>

<span data-ttu-id="3d37e-104">ICE97 verifica che due componenti non Isolino un componente condiviso nella stessa directory.</span><span class="sxs-lookup"><span data-stu-id="3d37e-104">ICE97 verifies that two components do not isolate a shared component to the same directory.</span></span>

## <a name="result"></a><span data-ttu-id="3d37e-105">Risultato</span><span class="sxs-lookup"><span data-stu-id="3d37e-105">Result</span></span>

<span data-ttu-id="3d37e-106">ICE97 invia gli avvisi seguenti.</span><span class="sxs-lookup"><span data-stu-id="3d37e-106">ICE97 posts the following warnings.</span></span>



| <span data-ttu-id="3d37e-107">Avviso di ICE97</span><span class="sxs-lookup"><span data-stu-id="3d37e-107">ICE97 Warning</span></span>                                                                                                                                                                    | <span data-ttu-id="3d37e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3d37e-108">Description</span></span>                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span data-ttu-id="3d37e-109">Questo componente \[ 1 \] installa il componente condiviso nella stessa directory \[ 2 \] di un altro, che interrompe le regole dei componenti se per l'installazione sono selezionati entrambi i componenti.</span><span class="sxs-lookup"><span data-stu-id="3d37e-109">This component \[1\] installs the Shared component into the same directory \[2\] as another, which breaks component rules if both (or more) components are selected for install.</span></span> | <span data-ttu-id="3d37e-110">Due componenti non devono isolare un componente condiviso nella stessa directory.</span><span class="sxs-lookup"><span data-stu-id="3d37e-110">Two components must not isolate a shared component to the same directory.</span></span> |



 

<span data-ttu-id="3d37e-111">Ad esempio, Component1 e Component2, che condividono ComponentShared, vengono installati nella stessa directory.</span><span class="sxs-lookup"><span data-stu-id="3d37e-111">For example, Component1 and Component2, which share ComponentShared, are installed to the same directory.</span></span> <span data-ttu-id="3d37e-112">Entrambi specificano ComponentShared come componente isolato.</span><span class="sxs-lookup"><span data-stu-id="3d37e-112">Both specify ComponentShared as an isolated component.</span></span> <span data-ttu-id="3d37e-113">A causa dell'isolamento, i file in ComponentShared vengono copiati due volte nel \_ riferimento alla directory per Component1 e Component2.</span><span class="sxs-lookup"><span data-stu-id="3d37e-113">Because of the isolation, the files in ComponentShared are copied twice into the Directory\_ reference for Component1 and Component2.</span></span> <span data-ttu-id="3d37e-114">Ai componenti è ora associato un conteggio dei riferimenti per la copia dei file.</span><span class="sxs-lookup"><span data-stu-id="3d37e-114">The components now have one reference count on the copy of files.</span></span> <span data-ttu-id="3d37e-115">Questo problema si verifica in violazione delle regole dei componenti del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="3d37e-115">This is in violation of the Installer component rules.</span></span> <span data-ttu-id="3d37e-116">Se Component1 viene disinstallato, i file dei componenti isolati vengono rimossi e Component2 è danneggiato.</span><span class="sxs-lookup"><span data-stu-id="3d37e-116">If Component1 is uninstalled, the isolated components files are removed and Component2 is broken.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3d37e-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3d37e-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d37e-118">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="3d37e-118">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



