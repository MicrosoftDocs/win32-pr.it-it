---
description: Inizialmente è necessario creare un oggetto del programma di installazione per caricare il supporto di automazione necessario per accedere ai componenti del programma di installazione tramite COM.
ms.assetid: 113ed443-a866-43d4-86bd-fc3b244f2edb
title: Informazioni sull'interfaccia di automazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 655a01a4daccb805bec4a858337c1dce48f0fb82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227226"
---
# <a name="about-the-automation-interface"></a><span data-ttu-id="44b51-103">Informazioni sull'interfaccia di automazione</span><span class="sxs-lookup"><span data-stu-id="44b51-103">About the Automation Interface</span></span>

<span data-ttu-id="44b51-104">Inizialmente è necessario creare un [**oggetto del programma di installazione**](installer-object.md) per caricare il supporto di automazione necessario per accedere ai componenti del programma di installazione tramite com.</span><span class="sxs-lookup"><span data-stu-id="44b51-104">An [**Installer object**](installer-object.md) must be created initially to load the automation support required to access the installer components through COM.</span></span> <span data-ttu-id="44b51-105">Questo oggetto fornisce i wrapper per creare gli oggetti di primo livello e accedere ai relativi metodi.</span><span class="sxs-lookup"><span data-stu-id="44b51-105">This object provides wrappers to create the top-level objects and access their methods.</span></span> <span data-ttu-id="44b51-106">Questi wrapper forniscono semplicemente le traduzioni di parametri per esporre le funzioni del programma di installazione in modo coerente con Microsoft Visual Basic senza modificare il comportamento dei metodi.</span><span class="sxs-lookup"><span data-stu-id="44b51-106">These wrappers simply provide parameter translations to expose the installer functions in a manner consistent with Microsoft Visual Basic without changing the behavior of the methods.</span></span>

<span data-ttu-id="44b51-107">Quando possibile, una coppia di metodi get e set C++ vengono esposti per Visual Basic come una singola proprietà.</span><span class="sxs-lookup"><span data-stu-id="44b51-107">Whenever possible, a pair of Get and Set C++ methods are exposed to Visual Basic as a single property.</span></span> <span data-ttu-id="44b51-108">In alcuni casi, i metodi C++ che accettano un argomento di indice vengono esposti come proprietà indicizzata.</span><span class="sxs-lookup"><span data-stu-id="44b51-108">In some cases C++ methods taking an index argument are exposed as an indexed property.</span></span> <span data-ttu-id="44b51-109">Molti metodi C++ restituiscono il risultato tramite un parametro poiché il valore restituito viene usato per la restituzione dell'errore.</span><span class="sxs-lookup"><span data-stu-id="44b51-109">Many C++ methods return the result through a parameter because the return value is used for the error return.</span></span> <span data-ttu-id="44b51-110">Tuttavia, in Visual Basic, gli errori vengono gestiti da un meccanismo separato e il risultato viene sempre passato nel valore restituito.</span><span class="sxs-lookup"><span data-stu-id="44b51-110">However, in Visual Basic, errors are handled by a separate mechanism, and the result is always passed in the return value.</span></span>

<span data-ttu-id="44b51-111">Per informazioni sull'uso dell'automazione e sulla creazione dell'oggetto del programma di installazione, vedere [uso dell'interfaccia di automazione](using-the-automation-interface.md).</span><span class="sxs-lookup"><span data-stu-id="44b51-111">For information about using automation and creating the Installer object, see [Using the Automation Interface](using-the-automation-interface.md).</span></span>

<span data-ttu-id="44b51-112">Per materiale di riferimento per gli oggetti Windows Installer, vedere informazioni di [riferimento sull'interfaccia di automazione](automation-interface-reference.md).</span><span class="sxs-lookup"><span data-stu-id="44b51-112">For reference material for the Windows Installer objects, see [Automation Interface Reference](automation-interface-reference.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="44b51-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="44b51-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44b51-114">Esempi di script di Windows Installer</span><span class="sxs-lookup"><span data-stu-id="44b51-114">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 



