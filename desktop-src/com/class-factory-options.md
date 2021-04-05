---
title: Opzioni di class factory
description: Opzioni di class factory
ms.assetid: e9e33e07-7628-4c5e-965d-e12a9c1d69c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fab52ea11a0e7e20d10757eb8d6e86577afc35c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730431"
---
# <a name="class-factory-options"></a><span data-ttu-id="b8793-103">Opzioni di class factory</span><span class="sxs-lookup"><span data-stu-id="b8793-103">Class Factory Options</span></span>

<span data-ttu-id="b8793-104">Un controllo ActiveX, in virtù di un oggetto COM, deve disporre di codice server associato che supporta la creazione di controlli tramite [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) come minimo.</span><span class="sxs-lookup"><span data-stu-id="b8793-104">An ActiveX Control, by virtue of being a COM object, must have associated server code that supports control creation through [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) as a minimum.</span></span>

<span data-ttu-id="b8793-105">È facoltativo, non obbligatorio, che questo oggetto classe supporti anche [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) per la gestione delle licenze.</span><span class="sxs-lookup"><span data-stu-id="b8793-105">It is optional, not required, that this class object also support [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) for licensing management.</span></span> <span data-ttu-id="b8793-106">Solo i fornitori interessati alle licenze devono supportare il meccanismo di gestione delle licenze di COM.</span><span class="sxs-lookup"><span data-stu-id="b8793-106">Only those vendors that are concerned about licensing need to support COM's licensing mechanism.</span></span> <span data-ttu-id="b8793-107">In altre parole, poiché **IClassFactory2** è l'unico modo per ottenere le licenze a livello com, questa interfaccia è necessaria per l'oggetto classe per i controlli che vogliono avere la licenza.</span><span class="sxs-lookup"><span data-stu-id="b8793-107">In other words, because **IClassFactory2** is the only way to achieve COM-level licensing, this interface is required on the class object for those controls that want to be licensed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b8793-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b8793-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8793-109">Controlli</span><span class="sxs-lookup"><span data-stu-id="b8793-109">Controls</span></span>](controls.md)
</dt> </dl>

 

 