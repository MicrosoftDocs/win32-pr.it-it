---
title: Come supportare gli elementi di callback
description: In questo argomento viene illustrato come fornire supporto per gli elementi di callback.
ms.assetid: BD32666F-9445-4871-AE21-5DC9F5FC9C1B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 056f64c086aeda94ccf928d93ae2c5db5e2187a4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "103963570"
---
# <a name="how-to-support-callback-items"></a><span data-ttu-id="46e89-103">Come supportare gli elementi di callback</span><span class="sxs-lookup"><span data-stu-id="46e89-103">How to Support Callback Items</span></span>

<span data-ttu-id="46e89-104">In questo argomento viene illustrato come fornire supporto per gli elementi di callback.</span><span class="sxs-lookup"><span data-stu-id="46e89-104">This topic demonstrates how to provide support for callback items.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="46e89-105">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="46e89-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="46e89-106">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="46e89-106">Technologies</span></span>

-   [<span data-ttu-id="46e89-107">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="46e89-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="46e89-108">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="46e89-108">Prerequisites</span></span>

-   <span data-ttu-id="46e89-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="46e89-109">C/C++</span></span>
-   <span data-ttu-id="46e89-110">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="46e89-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="46e89-111">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="46e89-111">Instructions</span></span>


<span data-ttu-id="46e89-112">Se l'applicazione userà gli elementi di callback in un controllo ComboBoxEx, è necessario prepararsi a gestire il codice di notifica [ \_ GETDISPINFO CBEN](cben-getdispinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="46e89-112">If your application is going to use callback items in a ComboBoxEx control, it must be prepared to handle the [CBEN\_GETDISPINFO](cben-getdispinfo.md) notification code.</span></span> <span data-ttu-id="46e89-113">Un controllo ComboBoxEx Invia questa notifica ogni volta che è necessario che il proprietario fornisca informazioni specifiche sull'elemento.</span><span class="sxs-lookup"><span data-stu-id="46e89-113">A ComboBoxEx control sends this notification whenever it needs the owner to provide specific item information.</span></span> <span data-ttu-id="46e89-114">Per altre informazioni sugli elementi di callback, vedere [elementi callback](comboboxex-controls.md).</span><span class="sxs-lookup"><span data-stu-id="46e89-114">For more information about callback items, see [Callback Items](comboboxex-controls.md).</span></span>

<span data-ttu-id="46e89-115">La funzione definita dall'applicazione seguente elabora [CBEN \_ GETDISPINFO](cben-getdispinfo.md) fornendo attributi per un determinato elemento.</span><span class="sxs-lookup"><span data-stu-id="46e89-115">The following application-defined function processes [CBEN\_GETDISPINFO](cben-getdispinfo.md) by providing attributes for a given item.</span></span> <span data-ttu-id="46e89-116">Si noti che imposta il membro **mask** della struttura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) in ingresso su CBEIF \_ di \_ elemento.</span><span class="sxs-lookup"><span data-stu-id="46e89-116">Note that it sets the **mask** member of the incoming [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure to CBEIF\_DI\_SETITEM.</span></span> <span data-ttu-id="46e89-117">Impostando **mask** su questo valore, il controllo mantiene le informazioni sull'elemento in modo che non sia necessario richiedere nuovamente le informazioni.</span><span class="sxs-lookup"><span data-stu-id="46e89-117">Setting **mask** to this value makes the control retain the item information so that it will not need to request the information again.</span></span>

## <a name="complete-example"></a><span data-ttu-id="46e89-118">Esempio completo</span><span class="sxs-lookup"><span data-stu-id="46e89-118">Complete example</span></span>


```C++
// DoItemCallback - Processes CBEN_GETDISPINFO by providing item
// attributes for a given callback item.

void WINAPI DoItemCallback(PNMCOMBOBOXEX pNMCBex)
{
    DWORD dwMask = pNMCBex->ceItem.mask;

    if(dwMask & CBEIF_TEXT)
    {
            // Insert code to provide item text.
    }

    if(dwMask & CBEIF_IMAGE) 
    {
        // Insert code to provide an item image index.
    }

    // Insert code to provide other callback information as desired.

    // Make the ComboBoxEx control hold onto the item information.
    pNMCBex->ceItem.mask = CBEIF_DI_SETITEM;
}
```



## <a name="related-topics"></a><span data-ttu-id="46e89-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="46e89-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46e89-120">Informazioni sui controlli ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="46e89-120">About ComboBoxEx Controls</span></span>](comboboxex-controls.md)
</dt> <dt>

[<span data-ttu-id="46e89-121">Riferimento al controllo ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="46e89-121">ComboBoxEx Control Reference</span></span>](bumper-comboboxex-comboboxex-control-reference.md)
</dt> <dt>

[<span data-ttu-id="46e89-122">Uso di controlli ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="46e89-122">Using ComboBoxEx Controls</span></span>](/windows/desktop/Controls/using-comboboxex)
</dt> <dt>

[<span data-ttu-id="46e89-123">ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="46e89-123">ComboBoxEx</span></span>](comboboxex-control-reference.md)
</dt> </dl>

 

 