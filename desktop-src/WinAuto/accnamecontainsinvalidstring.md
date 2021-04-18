---
title: AccNameContainsInvalidString
description: AccNameContainsInvalidString
ms.assetid: 392E4D10-4A8E-4118-B0E7-F74571812043
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 670672769c22cba556c164b8d03b2e9148fb8b1d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298881"
---
# <a name="accnamecontainsinvalidstring"></a><span data-ttu-id="f6a86-103">AccNameContainsInvalidString</span><span class="sxs-lookup"><span data-stu-id="f6a86-103">AccNameContainsInvalidString</span></span>

## <a name="text"></a><span data-ttu-id="f6a86-104">Testo</span><span class="sxs-lookup"><span data-stu-id="f6a86-104">Text</span></span>

<span data-ttu-id="f6a86-105">accName non deve contenere la stringa {0}</span><span class="sxs-lookup"><span data-stu-id="f6a86-105">accName should not contain the string {0}</span></span>

## <a name="type"></a><span data-ttu-id="f6a86-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="f6a86-106">Type</span></span>

<span data-ttu-id="f6a86-107">Errore</span><span class="sxs-lookup"><span data-stu-id="f6a86-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="f6a86-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f6a86-108">Description</span></span>

<span data-ttu-id="f6a86-109">Il nome di un elemento contiene caratteri non validi. questi caratteri sono sostituiti da AccChecker.</span><span class="sxs-lookup"><span data-stu-id="f6a86-109">The name of an element contains invalid characters (these characters are replaced by AccChecker).</span></span> <span data-ttu-id="f6a86-110">Ad esempio, il metodo [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) usato per recuperare il nome MSAA di un elemento restituisce una stringa che contiene i caratteri di tabulazione, nuova riga o e commerciale.</span><span class="sxs-lookup"><span data-stu-id="f6a86-110">For example, the [**get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) method used to retrieve the MSAA name of an element returns a string that contains tab, newline, or ampersand characters.</span></span>

<span data-ttu-id="f6a86-111">Questo problema causa problemi per gli utenti che si affidano a un lettore di schermate e a una tastiera per la navigazione, perché un elemento potrebbe avere un nome non pronunciabile e non intuitivo.</span><span class="sxs-lookup"><span data-stu-id="f6a86-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because an element might have an unpronounceable, non-intuitive name.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="f6a86-112">Possibili cause</span><span class="sxs-lookup"><span data-stu-id="f6a86-112">Possible causes</span></span>

<span data-ttu-id="f6a86-113">All'elemento o al relativo padre è assegnato un nome o un'etichetta non corretta.</span><span class="sxs-lookup"><span data-stu-id="f6a86-113">The element or its parent has an incorrectly assigned name or label.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f6a86-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f6a86-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6a86-115">**IAccessible:: Get \_ accName**</span><span class="sxs-lookup"><span data-stu-id="f6a86-115">**IAccessible::get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[<span data-ttu-id="f6a86-116">Proprietà Name</span><span class="sxs-lookup"><span data-stu-id="f6a86-116">Name Property</span></span>](name-property.md)
</dt> </dl>

 

 




