---
title: Proprietà e metodi di selezione e messa a fuoco
description: Analogamente a molti elementi in applicazioni in esecuzione su sistemi operativi Microsoft Windows, gli oggetti accessibili selezionano e ricevono lo stato attivo. Questi attributi consentono agli utenti di interagire con gli elementi dell'applicazione, modificare i valori e manipolarli in altro modo.
ms.assetid: 8170fe19-f157-4d7d-8eec-d384e51f1560
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bbb5eee361707ec4876245eef5b0eb352f8dfd6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728431"
---
# <a name="selection-and-focus-properties-and-methods"></a><span data-ttu-id="82285-104">Proprietà e metodi di selezione e messa a fuoco</span><span class="sxs-lookup"><span data-stu-id="82285-104">Selection and Focus Properties and Methods</span></span>

<span data-ttu-id="82285-105">Analogamente a molti elementi in applicazioni in esecuzione su sistemi operativi Microsoft Windows, gli oggetti accessibili *selezionano* e ricevono lo *stato attivo*.</span><span class="sxs-lookup"><span data-stu-id="82285-105">Like many elements in applications running on Microsoft Windows operating systems, accessible objects *select* and receive keyboard *focus*.</span></span> <span data-ttu-id="82285-106">Questi attributi consentono agli utenti di interagire con gli elementi dell'applicazione, modificare i valori e manipolarli in altro modo.</span><span class="sxs-lookup"><span data-stu-id="82285-106">These attributes enable users to interact with application elements, change values, and otherwise manipulate them.</span></span>

<span data-ttu-id="82285-107">Esistono alcune differenze principali tra la selezione degli oggetti e lo stato attivo dell'oggetto:</span><span class="sxs-lookup"><span data-stu-id="82285-107">There are some key differences between object selection and object focus:</span></span>

-   <span data-ttu-id="82285-108">Un oggetto con stato attivo è l'unico oggetto nell'intero sistema operativo che riceve l'input da tastiera.</span><span class="sxs-lookup"><span data-stu-id="82285-108">A focused object is the one object in the entire operating system that receives keyboard input.</span></span> <span data-ttu-id="82285-109">L'oggetto con lo stato attivo della tastiera è la finestra attiva o un oggetto figlio della finestra attiva.</span><span class="sxs-lookup"><span data-stu-id="82285-109">The object with the keyboard focus is either the active window or a child object of the active window.</span></span>
-   <span data-ttu-id="82285-110">Un oggetto selezionato è contrassegnato per partecipare a un determinato tipo di operazione di gruppo.</span><span class="sxs-lookup"><span data-stu-id="82285-110">A selected object is marked to participate in some type of group operation.</span></span>

<span data-ttu-id="82285-111">Ad esempio, un utente può selezionare più elementi in un controllo visualizzazione elenco, ma lo stato attivo viene assegnato solo a un oggetto nel sistema alla volta.</span><span class="sxs-lookup"><span data-stu-id="82285-111">For example, a user can select several items in a list-view control, but the focus is given only to one object in the system at a time.</span></span> <span data-ttu-id="82285-112">Si noti che gli elementi con stato attivo sono da una selezione di elementi.</span><span class="sxs-lookup"><span data-stu-id="82285-112">Note that focused items are from a selection of items.</span></span>

<span data-ttu-id="82285-113">I client determinano se un particolare oggetto accessibile o elemento figlio ha lo stato attivo chiamando [**IAccessible:: Get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus).</span><span class="sxs-lookup"><span data-stu-id="82285-113">Clients determine whether a particular accessible object or child element has the focus by calling [**IAccessible::get\_accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus).</span></span> <span data-ttu-id="82285-114">I client determinano se un oggetto è selezionato o quali elementi figlio all'interno di un oggetto accessibile sono selezionati chiamando [**IAccessible:: Get \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection).</span><span class="sxs-lookup"><span data-stu-id="82285-114">Clients determine whether an object is selected, or which children within an accessible object are selected, by calling [**IAccessible::get\_accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection).</span></span> <span data-ttu-id="82285-115">Per oggetti quali i controlli di visualizzazione elenco in cui sono selezionati più elementi figlio, l'oggetto padre deve supportare l'interfaccia [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) , che consente ai client di enumerare gli elementi figlio selezionati.</span><span class="sxs-lookup"><span data-stu-id="82285-115">For objects such as list-view controls in which more than one child is selected, the parent object must support the [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface, which allows clients to enumerate the selected children.</span></span>

## <a name="events-triggered-in-menus"></a><span data-ttu-id="82285-116">Eventi attivati nei menu</span><span class="sxs-lookup"><span data-stu-id="82285-116">Events Triggered in Menus</span></span>

<span data-ttu-id="82285-117">Microsoft Active Accessibility espone i menu standard creati con le API dei menu e i file di risorse di Microsoft Win32.</span><span class="sxs-lookup"><span data-stu-id="82285-117">Microsoft Active Accessibility exposes standard menus created with the Microsoft Win32 menu APIs and resource files.</span></span> <span data-ttu-id="82285-118">Per coerenza con i menu standard, i server con menu personalizzati attivano lo [**\_ \_ stato attivo dell'oggetto evento**](event-constants.md), non la [**\_ \_ selezione di oggetti evento**](event-constants.md), quando un utente evidenzia una voce di menu.</span><span class="sxs-lookup"><span data-stu-id="82285-118">To be consistent with standard menus, servers with custom menus trigger [**EVENT\_OBJECT\_FOCUS**](event-constants.md), not [**EVENT\_OBJECT\_SELECTION**](event-constants.md), when a user highlights a menu item.</span></span>

> [!Note]  
> <span data-ttu-id="82285-119">Microsoft Active Accessibility non supporta la selezione del testo contenuto nei controlli Edit e Rich Edit perché il testo viene esposto come una singola stringa nella proprietà [**value**](value-property.md) di questi controlli.</span><span class="sxs-lookup"><span data-stu-id="82285-119">Microsoft Active Accessibility does not support the selection of the text contained in edit and rich edit controls because the text is exposed as a single string in the [**Value**](value-property.md) property for these controls.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="82285-120">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="82285-120">In this section</span></span>

-   [<span data-ttu-id="82285-121">Selezione di oggetti figlio</span><span class="sxs-lookup"><span data-stu-id="82285-121">Selecting Child Objects</span></span>](selecting-child-objects.md)

 

 