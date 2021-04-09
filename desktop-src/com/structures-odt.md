---
title: Strutture (OLE e Trasferimento dati)
description: Le strutture seguenti vengono utilizzate per implementare documenti composti ed eseguire il trasferimento dei dati tra le applicazioni.
ms.assetid: 76fef2dd-4cfb-4526-a1e0-8e3218aa6145
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa9dde7f81d388943dbc05b2d38065be262d7f29
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104047706"
---
# <a name="structures-ole-and-data-transfer"></a><span data-ttu-id="dca01-103">Strutture (OLE e Trasferimento dati)</span><span class="sxs-lookup"><span data-stu-id="dca01-103">Structures (OLE and Data Transfer)</span></span>

<span data-ttu-id="dca01-104">Le strutture seguenti vengono utilizzate per implementare documenti composti ed eseguire il trasferimento dei dati tra le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="dca01-104">The following structures are used to implement compound documents and perform data transfer between applications.</span></span>

-   [<span data-ttu-id="dca01-105">**DVASPECTINFO**</span><span class="sxs-lookup"><span data-stu-id="dca01-105">**DVASPECTINFO**</span></span>](/windows/win32/api/ocidl/ne-ocidl-dvaspectinfoflag)
-   [<span data-ttu-id="dca01-106">**DVEXTENTINFO**</span><span class="sxs-lookup"><span data-stu-id="dca01-106">**DVEXTENTINFO**</span></span>](/windows/win32/api/ocidl/ns-ocidl-dvextentinfo)
-   [<span data-ttu-id="dca01-107">**DVTARGETDEVICE**</span><span class="sxs-lookup"><span data-stu-id="dca01-107">**DVTARGETDEVICE**</span></span>](/windows/win32/api/objidl/ns-objidl-dvtargetdevice)
-   [<span data-ttu-id="dca01-108">**FORMATETC**</span><span class="sxs-lookup"><span data-stu-id="dca01-108">**FORMATETC**</span></span>](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc)
-   [<span data-ttu-id="dca01-109">**OBJECTDESCRIPTOR**</span><span class="sxs-lookup"><span data-stu-id="dca01-109">**OBJECTDESCRIPTOR**</span></span>](/windows/win32/api/oleidl/ns-oleidl-objectdescriptor)
-   [<span data-ttu-id="dca01-110">**OLECMD**</span><span class="sxs-lookup"><span data-stu-id="dca01-110">**OLECMD**</span></span>](/windows/desktop/api/DocObj/ns-docobj-olecmd)
-   [<span data-ttu-id="dca01-111">**OLECMDTEXT**</span><span class="sxs-lookup"><span data-stu-id="dca01-111">**OLECMDTEXT**</span></span>](/windows/desktop/api/DocObj/ns-docobj-olecmdtext)
-   [<span data-ttu-id="dca01-112">**OLEINPLACEFRAMEINFO**</span><span class="sxs-lookup"><span data-stu-id="dca01-112">**OLEINPLACEFRAMEINFO**</span></span>](/windows/win32/api/oleidl/ns-oleidl-oleinplaceframeinfo)
-   [<span data-ttu-id="dca01-113">**OLEMENUGROUPWIDTHS**</span><span class="sxs-lookup"><span data-stu-id="dca01-113">**OLEMENUGROUPWIDTHS**</span></span>](/windows/win32/api/oleidl/ns-oleidl-olemenugroupwidths)
-   [<span data-ttu-id="dca01-114">**OLEUIBUSY**</span><span class="sxs-lookup"><span data-stu-id="dca01-114">**OLEUIBUSY**</span></span>](/windows/win32/api/oledlg/ns-oledlg-oleuibusya)
-   [<span data-ttu-id="dca01-115">**OLEUICHANGEICON**</span><span class="sxs-lookup"><span data-stu-id="dca01-115">**OLEUICHANGEICON**</span></span>](/windows/win32/api/oledlg/nf-oledlg-oleuichangeicona)
-   [<span data-ttu-id="dca01-116">**OLEUICHANGESOURCE**</span><span class="sxs-lookup"><span data-stu-id="dca01-116">**OLEUICHANGESOURCE**</span></span>](/windows/win32/api/oledlg/ns-oledlg-oleuichangesourcea)
-   [<span data-ttu-id="dca01-117">**OLEUICONVERT**</span><span class="sxs-lookup"><span data-stu-id="dca01-117">**OLEUICONVERT**</span></span>](/windows/win32/api/oledlg/ns-oledlg-oleuiconverta)
-   [<span data-ttu-id="dca01-118">**OLEUIEDITLINKS**</span><span class="sxs-lookup"><span data-stu-id="dca01-118">**OLEUIEDITLINKS**</span></span>](/windows/win32/api/oledlg/ns-oledlg-oleuieditlinksa)
-   [<span data-ttu-id="dca01-119">**OLEUIGNRLPROPS**</span><span class="sxs-lookup"><span data-stu-id="dca01-119">**OLEUIGNRLPROPS**</span></span>](/windows/win32/api/oledlg/ns-oledlg-oleuignrlpropsa)
-   [<span data-ttu-id="dca01-120">**OLEUIINSERTOBJECT**</span><span class="sxs-lookup"><span data-stu-id="dca01-120">**OLEUIINSERTOBJECT**</span></span>](/windows/win32/api/oledlg/ns-oledlg-oleuiinsertobjecta)
-   [<span data-ttu-id="dca01-121">**OLEUILINKPROPS**</span><span class="sxs-lookup"><span data-stu-id="dca01-121">**OLEUILINKPROPS**</span></span>](/windows/win32/api/oledlg/ns-oledlg-oleuilinkpropsa)
-   [<span data-ttu-id="dca01-122">**OLEUIOBJECTPROPS**</span><span class="sxs-lookup"><span data-stu-id="dca01-122">**OLEUIOBJECTPROPS**</span></span>](/windows/win32/api/oledlg/ns-oledlg-oleuiobjectpropsa)
-   [<span data-ttu-id="dca01-123">**OLEUIPASTEENTRY**</span><span class="sxs-lookup"><span data-stu-id="dca01-123">**OLEUIPASTEENTRY**</span></span>](/windows/win32/api/oledlg/ns-oledlg-oleuipasteentrya)
-   [<span data-ttu-id="dca01-124">**OLEUIPASTESPECIAL**</span><span class="sxs-lookup"><span data-stu-id="dca01-124">**OLEUIPASTESPECIAL**</span></span>](/windows/win32/api/oledlg/ns-oledlg-oleuipastespeciala)
-   [<span data-ttu-id="dca01-125">**OLEUIVIEWPROPS**</span><span class="sxs-lookup"><span data-stu-id="dca01-125">**OLEUIVIEWPROPS**</span></span>](/windows/win32/api/oledlg/ns-oledlg-oleuiviewpropsa)
-   [<span data-ttu-id="dca01-126">**OLEVERB**</span><span class="sxs-lookup"><span data-stu-id="dca01-126">**OLEVERB**</span></span>](/windows/win32/api/oleidl/ne-oleidl-oleverbattrib)
-   [<span data-ttu-id="dca01-127">**POINTF**</span><span class="sxs-lookup"><span data-stu-id="dca01-127">**POINTF**</span></span>](/windows/win32/api/ocidl/ns-ocidl-pointf)
-   [<span data-ttu-id="dca01-128">**STATDATA**</span><span class="sxs-lookup"><span data-stu-id="dca01-128">**STATDATA**</span></span>](/windows/desktop/api/ObjIdl/nn-objidl-ienumstatdata)
-   [<span data-ttu-id="dca01-129">**STGMEDIUM**</span><span class="sxs-lookup"><span data-stu-id="dca01-129">**STGMEDIUM**</span></span>](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1)

 

 




