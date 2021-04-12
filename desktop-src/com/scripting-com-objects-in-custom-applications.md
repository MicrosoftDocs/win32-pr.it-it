---
title: Creazione di script per oggetti COM in applicazioni personalizzate
description: Creazione di script per oggetti COM in applicazioni personalizzate
ms.assetid: 14e8cd53-e2b2-4393-8961-32efdf269f76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31d16938747755dfb0c08907430837de5a1106ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221319"
---
# <a name="scripting-com-objects-in-custom-applications"></a><span data-ttu-id="9b854-103">Creazione di script per oggetti COM in applicazioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="9b854-103">Scripting COM Objects in Custom Applications</span></span>

<span data-ttu-id="9b854-104">Microsoft offre diversi ambienti per la creazione di script per gli oggetti COM: pagine Active Server, Windows script host e così via.</span><span class="sxs-lookup"><span data-stu-id="9b854-104">Microsoft provides several environments for scripting COM objects: Active Server Pages, Windows Script Host, and so on.</span></span> <span data-ttu-id="9b854-105">I fornitori di software indipendenti (ISV) possono anche concedere in licenza i motori di script Microsoft per l'uso nelle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="9b854-105">Independent software vendors (ISVs) can also license Microsoft scripting engines for use in their applications.</span></span> <span data-ttu-id="9b854-106">Ad esempio, un ISV che crea un elaboratore di testo potrebbe voler aggiungere un linguaggio macro all'applicazione in modo che gli utenti possano automatizzare le attività semplici.</span><span class="sxs-lookup"><span data-stu-id="9b854-106">For example, an ISV creating a word processor might want to add a macro language to the application so users could automate simple tasks.</span></span> <span data-ttu-id="9b854-107">Grazie alla gestione delle licenze di un motore di script, l'ISV può utilizzare un linguaggio come VBScript o JScript come linguaggio macro dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9b854-107">By licensing a scripting engine, the ISV can use a language such as VBScript or JScript as the application's macro language.</span></span>

<span data-ttu-id="9b854-108">Oltre alla gestione delle licenze dei motori di scripting VBScript e JScript, gli ISV possono scrivere i propri motori di script ActiveX.</span><span class="sxs-lookup"><span data-stu-id="9b854-108">In addition to licensing VBScript and JScript scripting engines, ISVs can write their own ActiveX scripting engines.</span></span> <span data-ttu-id="9b854-109">Questi motori di scripting possono quindi essere inseriti in qualsiasi ambiente host che supporti lo standard del motore di scripting ActiveX.</span><span class="sxs-lookup"><span data-stu-id="9b854-109">These scripting engines can then be plugged into any host environment that supports the ActiveX scripting engine standard.</span></span> <span data-ttu-id="9b854-110">Ad esempio, un ISV potrebbe scrivere un motore di script PerlScript e installarlo in un server ASP, consentendo così al server ASP di elaborare gli script PerlScript.</span><span class="sxs-lookup"><span data-stu-id="9b854-110">For example, an ISV might write a PerlScript scripting engine and install it on an ASP server, thus enabling the ASP server to process PerlScript scripts.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9b854-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9b854-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b854-112">Creazione di script con oggetti COM</span><span class="sxs-lookup"><span data-stu-id="9b854-112">Scripting with COM Objects</span></span>](scripting-with-com-objects.md)
</dt> </dl>

 

 




