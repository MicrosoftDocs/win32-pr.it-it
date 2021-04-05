---
title: Linee guida sui client
description: Gli sviluppatori client devono utilizzare le funzionalità seguenti per ottenere informazioni sugli elementi dell'interfaccia utente
ms.assetid: 0e102e60-4d11-490e-88d5-dfadba620781
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9ced411c24ed0b7aa3ab97cbe1ce2511d4e6b05
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "103956137"
---
# <a name="client-guidelines"></a><span data-ttu-id="04869-103">Linee guida sui client</span><span class="sxs-lookup"><span data-stu-id="04869-103">Client Guidelines</span></span>

<span data-ttu-id="04869-104">Gli sviluppatori client devono utilizzare le funzionalità seguenti per ottenere informazioni sugli elementi dell'interfaccia utente:</span><span class="sxs-lookup"><span data-stu-id="04869-104">Client developers should use the following functionality to get information about the user interface elements:</span></span>

-   <span data-ttu-id="04869-105">Per ottenere un'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per gli oggetti, chiamare [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow), [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)o [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent).</span><span class="sxs-lookup"><span data-stu-id="04869-105">To get an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface to objects, call [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow), [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint), or [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent).</span></span>
-   <span data-ttu-id="04869-106">Per esaminare e modificare gli oggetti accessibili, utilizzare le proprietà e i metodi di [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="04869-106">To examine and manipulate accessible objects, use the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties and methods.</span></span>
-   <span data-ttu-id="04869-107">Per ricevere [winEvents](winevents-overview.md), chiamare [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) per registrare una funzione di callback WinEvent per gli eventi rilevanti per l'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="04869-107">To receive [WinEvents](winevents-overview.md), call [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) to register a WinEvent callback function for those events that are relevant to the client application.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="04869-108">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="04869-108">In this section</span></span>

-   [<span data-ttu-id="04869-109">Come i client ottengono gli ID figlio</span><span class="sxs-lookup"><span data-stu-id="04869-109">How Clients Obtain Child IDs</span></span>](how-clients-obtain-child-ids.md)

 

 




