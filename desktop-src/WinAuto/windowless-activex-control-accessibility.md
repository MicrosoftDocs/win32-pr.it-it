---
title: Accessibilità controllo ActiveX senza finestra
description: In questa sezione viene descritto come utilizzare l'API di accessibilità di Windows per assicurarsi che i controlli ActiveX di Microsoft ActiveX siano accessibili.
ms.assetid: 93CBCF20-DADF-4A63-BE60-F2A0D8810C62
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb0489cdd5de3ac34df361bfa3e7b3624ee18f3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399414"
---
# <a name="windowless-activex-control-accessibility"></a><span data-ttu-id="62628-103">Accessibilità controllo ActiveX senza finestra</span><span class="sxs-lookup"><span data-stu-id="62628-103">Windowless ActiveX Control Accessibility</span></span>

<span data-ttu-id="62628-104">In questa sezione viene descritto come utilizzare l'API di accessibilità di Windows per assicurarsi che i controlli ActiveX di Microsoft ActiveX siano accessibili.</span><span class="sxs-lookup"><span data-stu-id="62628-104">This section describes how to use the Windows Accessibility API to ensure that windowless Microsoft ActiveX controls are accessible.</span></span>

<span data-ttu-id="62628-105">Windows 8 include nuove interfacce API per l'accessibilità di Windows che semplificano l'implementazione dell'accessibilità per i controlli ActiveX senza finestra.</span><span class="sxs-lookup"><span data-stu-id="62628-105">Windows 8 includes new Windows Accessibility API interfaces that simplify the task of implementing accessibility for windowless ActiveX controls.</span></span> <span data-ttu-id="62628-106">L'API include interfacce implementate in un controllo senza finestra e nel contenitore di controlli, consentendo al controllo senza finestra e al relativo contenitore di interagire per fornire informazioni sull'accessibilità sul controllo senza finestra.</span><span class="sxs-lookup"><span data-stu-id="62628-106">The API includes interfaces that are implemented on a windowless control and on the control container, enabling the windowless control and its container to work together to provide accessibility information about the windowless control.</span></span> <span data-ttu-id="62628-107">L'API supporta gli scenari seguenti:</span><span class="sxs-lookup"><span data-stu-id="62628-107">The API supports the following scenarios:</span></span>

-   <span data-ttu-id="62628-108">Microsoft Active Accessibility controlli senza finestra ospitati in un contenitore di controlli Active Accessibility Microsoft.</span><span class="sxs-lookup"><span data-stu-id="62628-108">Microsoft Active Accessibility windowless controls hosted in a Microsoft Active Accessibility control container.</span></span>
-   <span data-ttu-id="62628-109">Microsoft Active Accessibility controlli senza finestra ospitati in un contenitore di controlli di automazione interfaccia utente Microsoft.</span><span class="sxs-lookup"><span data-stu-id="62628-109">Microsoft Active Accessibility windowless controls hosted in a Microsoft UI Automation control container.</span></span>
-   <span data-ttu-id="62628-110">Controlli senza finestra di automazione interfaccia utente ospitati in un contenitore di controlli di Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="62628-110">UI Automation windowless controls hosted in a Microsoft Active Accessibility control container.</span></span>
-   <span data-ttu-id="62628-111">Controlli senza finestra di automazione interfaccia utente ospitati in un contenitore di controlli di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="62628-111">UI Automation windowless controls hosted in a UI Automation control container.</span></span>

<span data-ttu-id="62628-112">La tabella seguente elenca le interfacce che supportano i controlli ActiveX senza finestra e identifica gli oggetti che implementano le interfacce.</span><span class="sxs-lookup"><span data-stu-id="62628-112">The following table lists the interfaces that support windowless ActiveX controls and identifies the objects that implement the interfaces.</span></span>



| <span data-ttu-id="62628-113">Oggetto</span><span class="sxs-lookup"><span data-stu-id="62628-113">Object</span></span>              | <span data-ttu-id="62628-114">MSAA</span><span class="sxs-lookup"><span data-stu-id="62628-114">MSAA</span></span>                                                                             | <span data-ttu-id="62628-115">automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="62628-115">UI automation</span></span>                                                                                     |
|---------------------|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62628-116">Oggetto Control</span><span class="sxs-lookup"><span data-stu-id="62628-116">Control object</span></span>      | [<span data-ttu-id="62628-117">**IAccessibleHandler**</span><span class="sxs-lookup"><span data-stu-id="62628-117">**IAccessibleHandler**</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessiblehandler)                                 |                                                                                                   |
| <span data-ttu-id="62628-118">Sito di controllo</span><span class="sxs-lookup"><span data-stu-id="62628-118">Control site</span></span>        | [<span data-ttu-id="62628-119">**IAccessibleWindowlessSite**</span><span class="sxs-lookup"><span data-stu-id="62628-119">**IAccessibleWindowlessSite**</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessiblewindowlesssite)        | [<span data-ttu-id="62628-120">**IRawElementProviderWindowlessSite**</span><span class="sxs-lookup"><span data-stu-id="62628-120">**IRawElementProviderWindowlessSite**</span></span>](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderwindowlesssite)         |
| <span data-ttu-id="62628-121">Radice della finestra host</span><span class="sxs-lookup"><span data-stu-id="62628-121">Root of host window</span></span> | [<span data-ttu-id="62628-122">**IAccessibleHostingElementProviders**</span><span class="sxs-lookup"><span data-stu-id="62628-122">**IAccessibleHostingElementProviders**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessiblehostingelementproviders) | [<span data-ttu-id="62628-123">**IRawElementProviderHostingAccessibles**</span><span class="sxs-lookup"><span data-stu-id="62628-123">**IRawElementProviderHostingAccessibles**</span></span>](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderhostingaccessibles) |



 

## <a name="in-this-section"></a><span data-ttu-id="62628-124">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="62628-124">In this section</span></span>

-   [<span data-ttu-id="62628-125">Come usare l'automazione dell'interfaccia utente per rendere accessibile un controllo ActiveX senza finestra</span><span class="sxs-lookup"><span data-stu-id="62628-125">How to Use UI Automation to Make a Windowless ActiveX Control Accessible</span></span>](use-ui-automation-to-make-an-windowless-activex-control-accessible.md)
-   [<span data-ttu-id="62628-126">Come utilizzare MSAA per rendere accessibile un controllo ActiveX senza finestra</span><span class="sxs-lookup"><span data-stu-id="62628-126">How to Use MSAA to Make a Windowless ActiveX Control Accessible</span></span>](use-msaa-to-make-an-windowless-activex-control-accessible.md)
-   [<span data-ttu-id="62628-127">Come ospitare un controllo ActiveX senza finestra di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="62628-127">How to Host a UI Automation Windowless ActiveX Control</span></span>](host-a-ui-automation-windowless-activex-control.md)
-   [<span data-ttu-id="62628-128">Come ospitare un controllo ActiveX senza finestra MSAA</span><span class="sxs-lookup"><span data-stu-id="62628-128">How to Host an MSAA Windowless ActiveX Control</span></span>](host-an-msaa-windowless-activex-control.md)

 

 