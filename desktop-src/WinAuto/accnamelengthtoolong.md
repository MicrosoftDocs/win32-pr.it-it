---
title: AccNameLengthTooLong
description: AccNameLengthTooLong
ms.assetid: 68997AE9-91FC-4DAD-8356-FEE6C6919939
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d1efcb2b7d13c83a5972cb6e100d70500f9c5ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298880"
---
# <a name="accnamelengthtoolong"></a><span data-ttu-id="748b2-103">AccNameLengthTooLong</span><span class="sxs-lookup"><span data-stu-id="748b2-103">AccNameLengthTooLong</span></span>

## <a name="text"></a><span data-ttu-id="748b2-104">Testo</span><span class="sxs-lookup"><span data-stu-id="748b2-104">Text</span></span>

<span data-ttu-id="748b2-105">Il nome dell'elemento non deve restituire una stringa più lunga di un {0} carattere</span><span class="sxs-lookup"><span data-stu-id="748b2-105">Element's name should not return a string longer than {0} character</span></span>

## <a name="type"></a><span data-ttu-id="748b2-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="748b2-106">Type</span></span>

<span data-ttu-id="748b2-107">Errore</span><span class="sxs-lookup"><span data-stu-id="748b2-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="748b2-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="748b2-108">Description</span></span>

<span data-ttu-id="748b2-109">Il nome di un elemento contiene troppi caratteri.</span><span class="sxs-lookup"><span data-stu-id="748b2-109">The name of an element contains too many characters.</span></span> <span data-ttu-id="748b2-110">Ad esempio, il metodo [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) usato per recuperare il nome MSAA di un elemento restituisce una stringa superiore al limite di 32000 caratteri.</span><span class="sxs-lookup"><span data-stu-id="748b2-110">For example, the [**get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) method used to retrieve the MSAA name of an element returns a string greater than the limit of 32000 characters.</span></span>

<span data-ttu-id="748b2-111">Questo problema causa problemi per gli utenti che si affidano a un lettore di schermate e a una tastiera per la navigazione, perché un elemento potrebbe avere un nome non pronunciabile e non intuitivo.</span><span class="sxs-lookup"><span data-stu-id="748b2-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because an element might have an unpronounceable, non-intuitive name.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="748b2-112">Possibili cause</span><span class="sxs-lookup"><span data-stu-id="748b2-112">Possible causes</span></span>

<span data-ttu-id="748b2-113">All'elemento o al relativo padre è assegnato un nome o un'etichetta non corretta.</span><span class="sxs-lookup"><span data-stu-id="748b2-113">The element or its parent has an incorrectly assigned name or label.</span></span>

## <a name="related-topics"></a><span data-ttu-id="748b2-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="748b2-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="748b2-115">**IAccessible:: Get \_ accName**</span><span class="sxs-lookup"><span data-stu-id="748b2-115">**IAccessible::get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[<span data-ttu-id="748b2-116">Proprietà Name</span><span class="sxs-lookup"><span data-stu-id="748b2-116">Name Property</span></span>](name-property.md)
</dt> </dl>

 

 




