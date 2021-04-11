---
title: Modalità di implementazione degli ID figlio da server
description: Gli sviluppatori di server possono assegnare gli ID figlio sia agli elementi semplici che agli oggetti accessibili. Tuttavia, l'approccio consigliato consiste nel supportare l'interfaccia COM (standard Component Object Model) IEnumVARIANT in tutti gli oggetti accessibili che dispongono di elementi figlio.
ms.assetid: 236de46e-8fe0-4f53-b989-267c9ee87545
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0721c9660aa02fb16e9ec33495279cd90e872a37
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963255"
---
# <a name="how-servers-implement-child-ids"></a><span data-ttu-id="24521-104">Modalità di implementazione degli ID figlio da server</span><span class="sxs-lookup"><span data-stu-id="24521-104">How Servers Implement Child IDs</span></span>

<span data-ttu-id="24521-105">Gli sviluppatori di server possono assegnare gli ID figlio sia agli elementi semplici che agli oggetti accessibili.</span><span class="sxs-lookup"><span data-stu-id="24521-105">Server developers can assign child IDs to both simple elements and accessible objects.</span></span> <span data-ttu-id="24521-106">Tuttavia, l'approccio consigliato consiste nel supportare l'interfaccia COM (standard Component Object Model) [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) in tutti gli oggetti accessibili che dispongono di elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="24521-106">However, the recommended approach is to support the standard Component Object Model (COM) interface [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) in every accessible object that has children.</span></span>

<span data-ttu-id="24521-107">Se si implementa [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant), è necessario:</span><span class="sxs-lookup"><span data-stu-id="24521-107">If you implement [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant), you must:</span></span>

-   <span data-ttu-id="24521-108">Enumerare tutti gli elementi figlio, sia semplici che oggetti accessibili.</span><span class="sxs-lookup"><span data-stu-id="24521-108">Enumerate all children, both simple elements and accessible objects.</span></span> <span data-ttu-id="24521-109">Fornire gli ID figlio per tutti gli elementi semplici e fornire [**IDispatch**](idispatch-interface.md) a ogni oggetto accessibile.</span><span class="sxs-lookup"><span data-stu-id="24521-109">Provide child IDs for all simple elements and provide the [**IDispatch**](idispatch-interface.md) to each accessible object.</span></span>
-   <span data-ttu-id="24521-110">Per gli oggetti accessibili, impostare il membro **VT** della [**variante**](variant-structure.md) sul \_ Dispatch VT.</span><span class="sxs-lookup"><span data-stu-id="24521-110">For accessible objects, set the **vt** member of the [**VARIANT**](variant-structure.md) to VT\_DISPATCH.</span></span> <span data-ttu-id="24521-111">Il membro **pdispVal** deve contenere un puntatore all'interfaccia [**IDispatch**](idispatch-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="24521-111">The **pdispVal** member must contain a pointer to the [**IDispatch**](idispatch-interface.md) interface.</span></span> <span data-ttu-id="24521-112">Si noti che il **Variant** viene allocato e liberato dal client.</span><span class="sxs-lookup"><span data-stu-id="24521-112">Note that the **VARIANT** is allocated and freed by the client.</span></span>
-   <span data-ttu-id="24521-113">Per gli elementi semplici, l'ID figlio è qualsiasi numero intero positivo a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="24521-113">For simple elements, the child ID is any 32-bit positive integer.</span></span> <span data-ttu-id="24521-114">Si noti che gli Integer zero e negativi sono riservati da Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="24521-114">Note that zero and negative integers are reserved by Microsoft Active Accessibility.</span></span> <span data-ttu-id="24521-115">Impostare il membro **VT** della struttura [**Variant**](variant-structure.md) su VT \_ I4 e il membro **LVAL** sull'ID figlio.</span><span class="sxs-lookup"><span data-stu-id="24521-115">Set the [**VARIANT**](variant-structure.md) structure **vt** member to VT\_I4 and the **lVal** member to the child ID.</span></span>

<span data-ttu-id="24521-116">Se non si supporta [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant), è necessario assegnare gli ID figlio e numerare gli elementi figlio in ogni oggetto a partire da uno in sequenza.</span><span class="sxs-lookup"><span data-stu-id="24521-116">If you do not support [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant), you must assign child IDs and number the children in each object sequentially starting with one.</span></span>

<span data-ttu-id="24521-117">È consigliabile che i client usino la funzione Microsoft Active Accessibility [**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren) invece di chiamare direttamente l'interfaccia [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) del server.</span><span class="sxs-lookup"><span data-stu-id="24521-117">It is recommended that clients use the Microsoft Active Accessibility function [**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren) rather than call the server [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface directly.</span></span>

 

 