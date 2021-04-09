---
description: L'interfaccia IWiaErrorHandler fornisce i metodi per gestire gli errori che possono verificarsi quando un'applicazione richiede i dati dell'immagine, sia per l'anteprima che per i bit finali.
ms.assetid: 33d8ccc5-6856-4a54-b1f0-d015933d63ab
title: Interfaccia IWiaErrorHandler (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaErrorHandler
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 7b3ea9f5556f1f919336e4abb4085f9e0c32d81d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130011"
---
# <a name="iwiaerrorhandler-interface"></a><span data-ttu-id="b976c-103">Interfaccia IWiaErrorHandler</span><span class="sxs-lookup"><span data-stu-id="b976c-103">IWiaErrorHandler interface</span></span>

<span data-ttu-id="b976c-104">L'interfaccia **IWiaErrorHandler** fornisce i metodi per gestire gli errori che possono verificarsi quando un'applicazione richiede i dati dell'immagine, sia per l'anteprima che per i bit finali.</span><span class="sxs-lookup"><span data-stu-id="b976c-104">The **IWiaErrorHandler** interface provides methods to handle errors that may occur when an application requests image data, whether for preview or final bits.</span></span>

## <a name="members"></a><span data-ttu-id="b976c-105">Membri</span><span class="sxs-lookup"><span data-stu-id="b976c-105">Members</span></span>

<span data-ttu-id="b976c-106">L'interfaccia **IWiaErrorHandler** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="b976c-106">The **IWiaErrorHandler** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b976c-107">**IWiaErrorHandler** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b976c-107">**IWiaErrorHandler** also has these types of members:</span></span>

-   [<span data-ttu-id="b976c-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="b976c-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b976c-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="b976c-109">Methods</span></span>

<span data-ttu-id="b976c-110">L'interfaccia **IWiaErrorHandler** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="b976c-110">The **IWiaErrorHandler** interface has these methods.</span></span>



| <span data-ttu-id="b976c-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="b976c-111">Method</span></span>                                                                     | <span data-ttu-id="b976c-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b976c-112">Description</span></span>                                                                                             |
|:---------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b976c-113">**GetStatusDescription**</span><span class="sxs-lookup"><span data-stu-id="b976c-113">**GetStatusDescription**</span></span>](-wia-iwiaerrorhandler-getstatusdescription.md) | <span data-ttu-id="b976c-114">Restituisce una stringa che descrive il codice di stato.</span><span class="sxs-lookup"><span data-stu-id="b976c-114">Returns a string that describes the status code.</span></span><br/>                                             |
| [<span data-ttu-id="b976c-115">**ReportStatus**</span><span class="sxs-lookup"><span data-stu-id="b976c-115">**ReportStatus**</span></span>](-wia-iwiaerrorhandler-reportstatus.md)                 | <span data-ttu-id="b976c-116">Gestisce i messaggi di stato e di errore durante il trasferimento dei dati dell'immagine e li visualizza all'utente.</span><span class="sxs-lookup"><span data-stu-id="b976c-116">Handles status and error messages during image data transfers and displays them to the user.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b976c-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="b976c-117">Remarks</span></span>

<span data-ttu-id="b976c-118">L'oggetto callback dell'applicazione può implementare **IWiaErrorHandler**.</span><span class="sxs-lookup"><span data-stu-id="b976c-118">The application callback object can implement **IWiaErrorHandler**.</span></span>

<span data-ttu-id="b976c-119">Questa interfaccia non è progettata per gestire gli errori riscontrati al di fuori dei trasferimenti di dati di immagini, ad esempio errori durante il recupero o l'impostazione delle proprietà del dispositivo o callback non restituiti in un driver.</span><span class="sxs-lookup"><span data-stu-id="b976c-119">This interface is not designed to handle errors encountered outside of image data transfers, for example, errors in getting or setting device properties or unreturned callbacks into a driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="b976c-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b976c-120">Requirements</span></span>



| <span data-ttu-id="b976c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b976c-121">Requirement</span></span> | <span data-ttu-id="b976c-122">Valore</span><span class="sxs-lookup"><span data-stu-id="b976c-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b976c-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b976c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b976c-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b976c-124">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b976c-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b976c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b976c-126">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b976c-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b976c-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b976c-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b976c-128"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="b976c-128"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="b976c-129">IDL</span><span class="sxs-lookup"><span data-stu-id="b976c-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b976c-130"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b976c-130"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="b976c-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="b976c-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="b976c-132"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b976c-132"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
