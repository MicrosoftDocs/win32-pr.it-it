---
description: I contesti di applicazione possono essere usati per creare classi di Windows affiancate.
ms.assetid: 4941ae1b-f9c6-45ff-b39b-a4078a12a58c
title: Creazione di classi di Windows affiancate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 161732522a12fb6924a2850031d77cff53e44eeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882666"
---
# <a name="creating-side-by-side-windows-classes"></a><span data-ttu-id="20f6f-103">Creazione di classi di Windows affiancate</span><span class="sxs-lookup"><span data-stu-id="20f6f-103">Creating Side-By-Side Windows Classes</span></span>

<span data-ttu-id="20f6f-104">I contesti di applicazione possono essere usati per creare classi di Windows affiancate.</span><span class="sxs-lookup"><span data-stu-id="20f6f-104">Application contexts can be used to create side-by-side Windows classes.</span></span> <span data-ttu-id="20f6f-105">Con le classi Windows affiancate, l'applicazione può avere versioni diverse di una classe attiva contemporaneamente in una finestra padre solitaria.</span><span class="sxs-lookup"><span data-stu-id="20f6f-105">By using side-by-side Windows classes, your application can have different versions of a class active at the same time in a lone parent window.</span></span> <span data-ttu-id="20f6f-106">Per creare una classe Windows affiancata, l'applicazione deve attivare un contesto di attivazione prima di chiamare [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) per ottenere un handle per la nuova finestra.</span><span class="sxs-lookup"><span data-stu-id="20f6f-106">To create a side-by-side Windows class, your application must activate an activation context before calling [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) to obtain a handle to the new window.</span></span>

<span data-ttu-id="20f6f-107">I controlli comuni di Windows versione 5,82 e la versione 6,0 hanno ad esempio un controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="20f6f-107">For example, Windows Common Controls version 5.82 and version 6.0 both had an Edit control.</span></span> <span data-ttu-id="20f6f-108">Per impostazione predefinita, Windows utilizza il controllo di modifica della versione 5,82.</span><span class="sxs-lookup"><span data-stu-id="20f6f-108">Windows defaults to using the version 5.82 Edit control.</span></span> <span data-ttu-id="20f6f-109">Per ottenere una finestra affiancata con il controllo di modifica della versione 6,0, prima di chiamare [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) come di consueto, l'applicazione può fare riferimento a un assembly che espone le classi finestra denominate e quindi attivare il contesto di attivazione che fa riferimento ai controlli della versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="20f6f-109">To obtain a side-by-side window that has the version 6.0 Edit control, before calling [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) as usual, your application can reference an assembly that exposes named window classes and then activate the activation context that references the version 6.0 controls.</span></span>

 

 
