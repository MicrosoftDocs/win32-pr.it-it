---
description: L'editor di controllo di accesso può includere una pagina delle proprietà Owner che consente all'utente di modificare il proprietario di un oggetto. Per ulteriori informazioni su un proprietario di oggetti, vedere proprietario di un nuovo oggetto e assunzione della proprietà di un oggetto in C++.
ms.assetid: b0c421db-450e-4030-98e9-e062202e482c
title: Pagina delle proprietà Owner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cee9d5c276071674ec274c9955a2e8c5cd5a856a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131930"
---
# <a name="owner-property-page"></a><span data-ttu-id="ad708-104">Pagina delle proprietà Owner</span><span class="sxs-lookup"><span data-stu-id="ad708-104">Owner Property Page</span></span>

<span data-ttu-id="ad708-105">L'editor di controllo di accesso può includere una pagina delle proprietà Owner che consente all'utente di modificare il proprietario di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="ad708-105">The access control editor can include an Owner property page that enables the user to change an object's owner.</span></span> <span data-ttu-id="ad708-106">Per ulteriori informazioni sul proprietario di un oggetto, vedere [proprietario di un nuovo oggetto](owner-of-a-new-object.md) e [assunzione della proprietà di un oggetto in C++](taking-object-ownership-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="ad708-106">For more information about an object's owner, see [Owner of a New Object](owner-of-a-new-object.md) and [Taking Object Ownership in C++](taking-object-ownership-in-c--.md).</span></span>

<span data-ttu-id="ad708-107">La pagina delle proprietà **proprietario** si trova nella [finestra delle proprietà sicurezza avanzata](advanced-security-property-sheet.md) visualizzata quando l'utente fa clic sul pulsante **Avanzate** nella [pagina delle proprietà sicurezza di base](basic-security-property-page.md).</span><span class="sxs-lookup"><span data-stu-id="ad708-107">The **Owner** property page is in the [advanced security property sheet](advanced-security-property-sheet.md) displayed when the user clicks the **Advanced** button on the [basic security property page](basic-security-property-page.md).</span></span> <span data-ttu-id="ad708-108">Per includere la pagina delle proprietà **owner** , impostare i \_ flag SI Advanced e si \_ modifica \_ proprietario nella struttura di [**\_ \_ informazioni sull'oggetto si**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) restituita dall'implementazione di [**ISecurityInformation:: GetObjectInformation**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) .</span><span class="sxs-lookup"><span data-stu-id="ad708-108">To include the **Owner** property page, set the SI\_ADVANCED and SI\_EDIT\_OWNER flags in the [**SI\_OBJECT\_INFO**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) structure returned by your [**ISecurityInformation::GetObjectInformation**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) implementation.</span></span>

 

 
