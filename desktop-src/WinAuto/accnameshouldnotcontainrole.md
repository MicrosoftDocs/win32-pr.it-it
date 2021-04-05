---
title: AccNameShouldNotContainRole
description: AccNameShouldNotContainRole
ms.assetid: 271461FF-5123-482F-B66D-A323CB3361DD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fb91eeeb34d484c1f51cd0b7cd2d2947e86abda
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714194"
---
# <a name="accnameshouldnotcontainrole"></a><span data-ttu-id="ec42e-103">AccNameShouldNotContainRole</span><span class="sxs-lookup"><span data-stu-id="ec42e-103">AccNameShouldNotContainRole</span></span>

## <a name="text"></a><span data-ttu-id="ec42e-104">Testo</span><span class="sxs-lookup"><span data-stu-id="ec42e-104">Text</span></span>

<span data-ttu-id="ec42e-105">Il nome dell'elemento ( {0} ) non deve contenere il testo del ruolo dell'elemento ( {1} )</span><span class="sxs-lookup"><span data-stu-id="ec42e-105">Element's Name ({0}) should not contain the text of the Element's Role ({1})</span></span>

## <a name="type"></a><span data-ttu-id="ec42e-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="ec42e-106">Type</span></span>

<span data-ttu-id="ec42e-107">Avviso</span><span class="sxs-lookup"><span data-stu-id="ec42e-107">Warning</span></span>

## <a name="description"></a><span data-ttu-id="ec42e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ec42e-108">Description</span></span>

<span data-ttu-id="ec42e-109">Il nome di un elemento incorpora il proprio ruolo MSAA o il tipo di controllo UIA.</span><span class="sxs-lookup"><span data-stu-id="ec42e-109">The name of an element incorporates its MSAA role or UIA control type.</span></span> <span data-ttu-id="ec42e-110">Ad esempio, questo avviso può verificarsi se il metodo [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) , utilizzato per recuperare il nome MSAA di un elemento, restituisce "Role \_ System \_ ScrollBar \_ \* ".</span><span class="sxs-lookup"><span data-stu-id="ec42e-110">For example, this warning can occur if the [**get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) method—which is used to retrieve the MSAA name of an element—returns "ROLE\_SYSTEM\_SCROLLBAR\_\*".</span></span>

<span data-ttu-id="ec42e-111">Questo problema causa problemi per gli utenti che si affidano a un lettore di schermate e a una tastiera per la navigazione, perché il ruolo verrà letto due volte o potrebbe non essere pronunciabile o non intuitivo per gli utenti.</span><span class="sxs-lookup"><span data-stu-id="ec42e-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because the role will be read twice, or it may be unpronounceable or non-intuitive for users.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="ec42e-112">Possibili cause</span><span class="sxs-lookup"><span data-stu-id="ec42e-112">Possible causes</span></span>

-   <span data-ttu-id="ec42e-113">All'elemento o al relativo padre è assegnato un nome o un'etichetta non corretta.</span><span class="sxs-lookup"><span data-stu-id="ec42e-113">The element or its parent has an incorrectly assigned name or label.</span></span>
-   <span data-ttu-id="ec42e-114">L'elemento o il relativo padre ha un nome predefinito che non è stato modificato in un nome descrittivo.</span><span class="sxs-lookup"><span data-stu-id="ec42e-114">The element or its parent has a default name that has not been revised to a friendly name.</span></span> <span data-ttu-id="ec42e-115">Ad esempio, button1.</span><span class="sxs-lookup"><span data-stu-id="ec42e-115">For example, button1.</span></span>
-   <span data-ttu-id="ec42e-116">Uno sviluppatore non è in grado di leggere i nomi dei lettori dello schermo.</span><span class="sxs-lookup"><span data-stu-id="ec42e-116">A developer is not aware that screen readers read names.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ec42e-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ec42e-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec42e-118">**IAccessible:: Get \_ accName**</span><span class="sxs-lookup"><span data-stu-id="ec42e-118">**IAccessible::get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[<span data-ttu-id="ec42e-119">Proprietà Name</span><span class="sxs-lookup"><span data-stu-id="ec42e-119">Name Property</span></span>](name-property.md)
</dt> </dl>

 

 




