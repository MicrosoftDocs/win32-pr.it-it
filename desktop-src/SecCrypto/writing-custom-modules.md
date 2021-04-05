---
description: È possibile scrivere moduli criteri nel linguaggio di programmazione C, C++ o Visual Basic.
ms.assetid: 37a93c67-02f2-4c4e-a000-2bb98e0ca948
title: Scrittura di moduli personalizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92247cd6b975bac520032dcc3aada1328f7b6c2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967617"
---
# <a name="writing-custom-modules"></a><span data-ttu-id="56864-103">Scrittura di moduli personalizzati</span><span class="sxs-lookup"><span data-stu-id="56864-103">Writing Custom Modules</span></span>

<span data-ttu-id="56864-104">È possibile scrivere moduli criteri nel linguaggio di programmazione C, C++ o Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="56864-104">You can write policy modules in the C, C++, or Visual Basic programming language.</span></span> <span data-ttu-id="56864-105">Il compilatore Microsoft richiesto è disponibile in Visual C++ versione 5,0 o successiva o in Visual Basic versione 5,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="56864-105">The required Microsoft compiler is available in Visual C++ version 5.0 or later or in Visual Basic version 5.0 or later.</span></span> <span data-ttu-id="56864-106">Un' [*autorità di certificazione*](../secgloss/c-gly.md) (CA) dell'organizzazione (Enterprise) deve usare solo il modulo criteri di organizzazione fornito da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="56864-106">An enterprise [*certification authority*](../secgloss/c-gly.md) (CA) should use only the Microsoft-provided enterprise policy module.</span></span>

<span data-ttu-id="56864-107">Quando si scrive un modulo criteri personalizzato, è necessario implementare [**ICertPolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy) .</span><span class="sxs-lookup"><span data-stu-id="56864-107">You must implement [**ICertPolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy) when writing a custom policy module.</span></span> <span data-ttu-id="56864-108">Inoltre, è necessario implementare [**ICertManageModule**](/windows/desktop/api/Certmod/nn-certmod-icertmanagemodule) quando si scrive un modulo criteri personalizzato.</span><span class="sxs-lookup"><span data-stu-id="56864-108">Additionally, you must implement [**ICertManageModule**](/windows/desktop/api/Certmod/nn-certmod-icertmanagemodule) when writing a custom policy module.</span></span>

<span data-ttu-id="56864-109">I moduli criteri possono chiamare i metodi di [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) per facilitare l'elaborazione di una [*richiesta di certificato*](../secgloss/c-gly.md). **ICertServerPolicy** consente di impostare e recuperare le proprietà e le estensioni del certificato.</span><span class="sxs-lookup"><span data-stu-id="56864-109">Policy modules can call methods from [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) to assist in the processing of a [*certificate request*](../secgloss/c-gly.md); **ICertServerPolicy** allows properties and certificate extensions to be set and retrieved.</span></span>

<span data-ttu-id="56864-110">Per ulteriori informazioni, vedere gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="56864-110">For more information, see the following topics.</span></span>



| <span data-ttu-id="56864-111">Argomento</span><span class="sxs-lookup"><span data-stu-id="56864-111">Topic</span></span>                                                                      | <span data-ttu-id="56864-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="56864-112">Description</span></span>                             |
|----------------------------------------------------------------------------|-----------------------------------------|
| [<span data-ttu-id="56864-113">Impostazione delle proprietà del certificato</span><span class="sxs-lookup"><span data-stu-id="56864-113">Setting Certificate Properties</span></span>](setting-certificate-properties.md)       | <span data-ttu-id="56864-114">Impostazione delle proprietà di un certificato</span><span class="sxs-lookup"><span data-stu-id="56864-114">Setting the properties of a certificate</span></span> |
| [<span data-ttu-id="56864-115">Scrittura di moduli di uscita personalizzati</span><span class="sxs-lookup"><span data-stu-id="56864-115">Writing Custom Exit Modules</span></span>](writing-custom-exit-modules.md)             | <span data-ttu-id="56864-116">Scrittura di moduli di uscita personalizzati</span><span class="sxs-lookup"><span data-stu-id="56864-116">Writing custom exit modules</span></span>             |
| [<span data-ttu-id="56864-117">Scrittura di gestori estensioni personalizzati</span><span class="sxs-lookup"><span data-stu-id="56864-117">Writing Custom Extension Handlers</span></span>](writing-custom-extension-handlers.md) | <span data-ttu-id="56864-118">Scrittura di gestori estensioni personalizzati</span><span class="sxs-lookup"><span data-stu-id="56864-118">Writing custom extension handlers</span></span>       |



 

 

 
