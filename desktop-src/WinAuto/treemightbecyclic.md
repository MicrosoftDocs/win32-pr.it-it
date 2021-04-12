---
title: TreeMightBeCyclic
description: TreeMightBeCyclic
ms.assetid: 9A997949-A1A2-448C-9739-BE176621F1B4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9647f4429ba17226f342a8dceb3c51b033d08b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337670"
---
# <a name="treemightbecyclic"></a><span data-ttu-id="a5760-103">TreeMightBeCyclic</span><span class="sxs-lookup"><span data-stu-id="a5760-103">TreeMightBeCyclic</span></span>

## <a name="text"></a><span data-ttu-id="a5760-104">Testo</span><span class="sxs-lookup"><span data-stu-id="a5760-104">Text</span></span>

<span data-ttu-id="a5760-105">L'albero è a {0} livelli profondi.</span><span class="sxs-lookup"><span data-stu-id="a5760-105">Tree is {0} levels deep.</span></span> <span data-ttu-id="a5760-106">Questo potrebbe indicare che l'albero di accessibilità è ciclico e pertanto sembrerebbe essere infinito.</span><span class="sxs-lookup"><span data-stu-id="a5760-106">This might indicate that the accessibility tree is cyclic, and thus it would appear to be infinite.</span></span>

## <a name="type"></a><span data-ttu-id="a5760-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="a5760-107">Type</span></span>

<span data-ttu-id="a5760-108">Errore</span><span class="sxs-lookup"><span data-stu-id="a5760-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="a5760-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a5760-109">Description</span></span>

<span data-ttu-id="a5760-110">L'albero degli elementi è ciclico e la profondità dell'albero può essere infinita.</span><span class="sxs-lookup"><span data-stu-id="a5760-110">The element tree is cyclic and the tree depth might be infinite.</span></span>

<span data-ttu-id="a5760-111">Questo problema causa problemi per gli utenti che si affidano a un lettore di schermate e a una tastiera per la navigazione, perché non esiste alcun limite evidente all'attraversamento degli elementi nell'applicazione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a5760-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because there will be no apparent limit to the traversal of elements in the target application.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="a5760-112">Possibili cause</span><span class="sxs-lookup"><span data-stu-id="a5760-112">Possible causes</span></span>

<span data-ttu-id="a5760-113">Più elementi o i relativi padri sono controlli personalizzati che non implementano correttamente la tabulazione.</span><span class="sxs-lookup"><span data-stu-id="a5760-113">Multiple elements, or their parents, are custom controls that do not implement tabbing correctly.</span></span> <span data-ttu-id="a5760-114">Ad esempio, la proprietà [stato](state-property.md) MSAA non viene aggiornata correttamente.</span><span class="sxs-lookup"><span data-stu-id="a5760-114">For example, the MSAA [State](state-property.md) property is not updated correctly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a5760-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a5760-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5760-116">Linee guida per la progettazione dell'interfaccia utente della tastiera</span><span class="sxs-lookup"><span data-stu-id="a5760-116">Guidelines for Keyboard User Interface Design</span></span>](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> <dt>

[<span data-ttu-id="a5760-117">Linee guida per l'interazione con l'esperienza utente Windows-tastiera</span><span class="sxs-lookup"><span data-stu-id="a5760-117">Windows User Experience Interaction Guidelines - Keyboard</span></span>](https://msdn.microsoft.com/library/bb545460.aspx#guidelines)
</dt> </dl>

 

 