---
description: L'interfaccia IAMSetErrorLog imposta o recupera un log degli errori in servizi di modifica DirectShow (DES).
ms.assetid: ce658533-eacf-4b5d-9910-dca918de09e7
title: Interfaccia IAMSetErrorLog (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMSetErrorLog
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c0a24d29625bf08bc2f4c728a61f5188e8bec211
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326809"
---
# <a name="iamseterrorlog-interface"></a><span data-ttu-id="c8274-103">Interfaccia IAMSetErrorLog</span><span class="sxs-lookup"><span data-stu-id="c8274-103">IAMSetErrorLog interface</span></span>

> [!Note]  
> <span data-ttu-id="c8274-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="c8274-104">\[Deprecated.</span></span> <span data-ttu-id="c8274-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c8274-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c8274-106">L' `IAMSetErrorLog` interfaccia imposta o recupera un log degli errori in [servizi di modifica DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="c8274-106">The `IAMSetErrorLog` interface sets or retrieves an error log in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="c8274-107">L'oggetto sequenza temporale implementa questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="c8274-107">The timeline object implements this interface.</span></span> <span data-ttu-id="c8274-108">Le applicazioni possono utilizzare questa interfaccia per registrare gli errori di rendering in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="c8274-108">Applications can use this interface to log rendering errors at run time.</span></span> <span data-ttu-id="c8274-109">Implementare l'interfaccia [**IAMErrorLog**](iamerrorlog.md) nell'applicazione, quindi chiamare il metodo [**IAMSetErrorLog::p log degli \_ errori UT**](iamseterrorlog-put-errorlog.md) nella sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="c8274-109">Implement the [**IAMErrorLog**](iamerrorlog.md) interface in your application, and then call the [**IAMSetErrorLog::put\_ErrorLog**](iamseterrorlog-put-errorlog.md) method on the timeline.</span></span>

<span data-ttu-id="c8274-110">Per ulteriori informazioni sull'utilizzo di questa interfaccia, vedere [registrazione degli errori](logging-errors.md).</span><span class="sxs-lookup"><span data-stu-id="c8274-110">For more information on using this interface, see [Logging Errors](logging-errors.md).</span></span>

## <a name="members"></a><span data-ttu-id="c8274-111">Membri</span><span class="sxs-lookup"><span data-stu-id="c8274-111">Members</span></span>

<span data-ttu-id="c8274-112">L'interfaccia **IAMSetErrorLog** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="c8274-112">The **IAMSetErrorLog** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c8274-113">**IAMSetErrorLog** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c8274-113">**IAMSetErrorLog** also has these types of members:</span></span>

-   [<span data-ttu-id="c8274-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="c8274-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c8274-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="c8274-115">Methods</span></span>

<span data-ttu-id="c8274-116">L'interfaccia **IAMSetErrorLog** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="c8274-116">The **IAMSetErrorLog** interface has these methods.</span></span>



| <span data-ttu-id="c8274-117">Metodo</span><span class="sxs-lookup"><span data-stu-id="c8274-117">Method</span></span>                                               | <span data-ttu-id="c8274-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c8274-118">Description</span></span>                                                 |
|:-----------------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="c8274-119">**Ottieni \_ log degli errori**</span><span class="sxs-lookup"><span data-stu-id="c8274-119">**get\_ErrorLog**</span></span>](iamseterrorlog-get-errorlog.md) | <span data-ttu-id="c8274-120">Recupera il log degli errori corrente per questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="c8274-120">Retrieves the current error log for this object.</span></span><br/> |
| [<span data-ttu-id="c8274-121">**Inserisci \_ log degli errori**</span><span class="sxs-lookup"><span data-stu-id="c8274-121">**put\_ErrorLog**</span></span>](iamseterrorlog-put-errorlog.md) | <span data-ttu-id="c8274-122">Specifica un log degli errori per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c8274-122">Specifies an error log for the object.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="c8274-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="c8274-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c8274-124">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="c8274-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c8274-125">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="c8274-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c8274-126">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="c8274-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c8274-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c8274-127">Requirements</span></span>



| <span data-ttu-id="c8274-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8274-128">Requirement</span></span> | <span data-ttu-id="c8274-129">Valore</span><span class="sxs-lookup"><span data-stu-id="c8274-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8274-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c8274-130">Header</span></span><br/>  | <dl> <span data-ttu-id="c8274-131"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8274-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c8274-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="c8274-132">Library</span></span><br/> | <dl> <span data-ttu-id="c8274-133"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c8274-133"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
