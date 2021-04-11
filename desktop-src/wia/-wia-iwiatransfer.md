---
description: L'interfaccia IWiaTransfer fornisce il trasferimento dei dati basato sul flusso.
ms.assetid: 7bc6d3b8-9bf0-4b77-aa2b-b7c64c5730c0
title: Interfaccia IWiaTransfer (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 623cc21591289f4c1fff33cabe1d504b3682708c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226145"
---
# <a name="iwiatransfer-interface"></a><span data-ttu-id="b3415-103">Interfaccia IWiaTransfer</span><span class="sxs-lookup"><span data-stu-id="b3415-103">IWiaTransfer interface</span></span>

<span data-ttu-id="b3415-104">L'interfaccia **IWiaTransfer** fornisce il trasferimento dei dati basato sul flusso.</span><span class="sxs-lookup"><span data-stu-id="b3415-104">The **IWiaTransfer** interface provides stream-based transfer of data.</span></span>

## <a name="members"></a><span data-ttu-id="b3415-105">Membri</span><span class="sxs-lookup"><span data-stu-id="b3415-105">Members</span></span>

<span data-ttu-id="b3415-106">L'interfaccia **IWiaTransfer** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="b3415-106">The **IWiaTransfer** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b3415-107">**IWiaTransfer** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b3415-107">**IWiaTransfer** also has these types of members:</span></span>

-   [<span data-ttu-id="b3415-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="b3415-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b3415-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="b3415-109">Methods</span></span>

<span data-ttu-id="b3415-110">L'interfaccia **IWiaTransfer** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="b3415-110">The **IWiaTransfer** interface has these methods.</span></span>



| <span data-ttu-id="b3415-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="b3415-111">Method</span></span>                                                                 | <span data-ttu-id="b3415-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3415-112">Description</span></span>                                                                                 |
|:-----------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b3415-113">**Annulla**</span><span class="sxs-lookup"><span data-stu-id="b3415-113">**Cancel**</span></span>](-wia-iwiatransfer-cancel.md)                             | <span data-ttu-id="b3415-114">Annulla l'operazione di trasferimento corrente.</span><span class="sxs-lookup"><span data-stu-id="b3415-114">Cancels the current transfer operation.</span></span> <br/>                                         |
| [<span data-ttu-id="b3415-115">**Scarica**</span><span class="sxs-lookup"><span data-stu-id="b3415-115">**Download**</span></span>](-wia-iwiatransfer-download.md)                         | <span data-ttu-id="b3415-116">Avvia un download di dati al chiamante.</span><span class="sxs-lookup"><span data-stu-id="b3415-116">Initiates a data download to the caller.</span></span> <br/>                                        |
| [<span data-ttu-id="b3415-117">**\_Informazioni sul formato EnumWIA \_**</span><span class="sxs-lookup"><span data-stu-id="b3415-117">**EnumWIA\_FORMAT\_INFO**</span></span>](-wia-iwiatransfer-enumwia-format-info.md) | <span data-ttu-id="b3415-118">Crea un enumeratore per i formati di trasferimento supportati dal dispositivo WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="b3415-118">Creates an enumerator for the transfer formats that the WIA 2.0 device supports.</span></span><br/> |
| [<span data-ttu-id="b3415-119">**Carica**</span><span class="sxs-lookup"><span data-stu-id="b3415-119">**Upload**</span></span>](-wia-iwiatransfer-upload.md)                             | <span data-ttu-id="b3415-120">Avvia un caricamento di dati di un singolo elemento dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="b3415-120">Initiates a data upload of a single item from the caller.</span></span> <br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="b3415-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="b3415-121">Remarks</span></span>

<span data-ttu-id="b3415-122">L'interfaccia **IWiaTransfer** , come tutte le interfacce Component Object Model (com), eredita i metodi di interfaccia [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="b3415-122">The **IWiaTransfer** interface, like all Component Object Model (COM) interfaces, inherits the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface methods.</span></span>



| <span data-ttu-id="b3415-123">Metodi IUnknown</span><span class="sxs-lookup"><span data-stu-id="b3415-123">IUnknown Methods</span></span>                                        | <span data-ttu-id="b3415-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3415-124">Description</span></span>                               |
|---------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="b3415-125">[IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="b3415-125">[IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span> | <span data-ttu-id="b3415-126">Restituisce puntatori alle interfacce supportate.</span><span class="sxs-lookup"><span data-stu-id="b3415-126">Returns pointers to supported interfaces.</span></span> |
| [<span data-ttu-id="b3415-127">IUnknown:: AddRef</span><span class="sxs-lookup"><span data-stu-id="b3415-127">IUnknown::AddRef</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | <span data-ttu-id="b3415-128">Incrementa il conteggio dei riferimenti.</span><span class="sxs-lookup"><span data-stu-id="b3415-128">Increments reference count.</span></span>               |
| [<span data-ttu-id="b3415-129">IUnknown:: Release</span><span class="sxs-lookup"><span data-stu-id="b3415-129">IUnknown::Release</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | <span data-ttu-id="b3415-130">Riduce il conteggio dei riferimenti.</span><span class="sxs-lookup"><span data-stu-id="b3415-130">Decrements reference count.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="b3415-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b3415-131">Requirements</span></span>



| <span data-ttu-id="b3415-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3415-132">Requirement</span></span> | <span data-ttu-id="b3415-133">Valore</span><span class="sxs-lookup"><span data-stu-id="b3415-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3415-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3415-134">Minimum supported client</span></span><br/> | <span data-ttu-id="b3415-135">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b3415-135">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b3415-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3415-136">Minimum supported server</span></span><br/> | <span data-ttu-id="b3415-137">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b3415-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b3415-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b3415-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3415-139"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3415-139"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="b3415-140">IDL</span><span class="sxs-lookup"><span data-stu-id="b3415-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b3415-141"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b3415-141"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="b3415-142">Libreria</span><span class="sxs-lookup"><span data-stu-id="b3415-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="b3415-143"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b3415-143"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
