---
title: Interfaccia IWMDRMLicenseBackupRestoreStatus
description: L'interfaccia IWMDRMLicenseBackupRestoreStatus fornisce un metodo per recuperare informazioni dettagliate sullo stato di un'operazione di backup o ripristino delle licenze. Questa interfaccia viene fornita con gli eventi di stato generati durante le operazioni di backup e ripristino delle licenze.
ms.assetid: fbcd059f-13d9-4edb-8946-b55c9da6dca4
keywords:
- Formato Windows Media Interface IWMDRMLicenseBackupRestoreStatus
- Interfaccia IWMDRMLicenseBackupRestoreStatus-formato Windows Media, descritto
topic_type:
- apiref
api_name:
- IWMDRMLicenseBackupRestoreStatus
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a9db5d95daab78a506a3cc994fb9dd22153d0907
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338622"
---
# <a name="iwmdrmlicensebackuprestorestatus-interface"></a><span data-ttu-id="af292-105">Interfaccia IWMDRMLicenseBackupRestoreStatus</span><span class="sxs-lookup"><span data-stu-id="af292-105">IWMDRMLicenseBackupRestoreStatus interface</span></span>

<span data-ttu-id="af292-106">L'interfaccia **IWMDRMLicenseBackupRestoreStatus** fornisce un metodo per recuperare informazioni dettagliate sullo stato di un'operazione di backup o ripristino delle licenze.</span><span class="sxs-lookup"><span data-stu-id="af292-106">The **IWMDRMLicenseBackupRestoreStatus** interface provides a method to retrieve detailed status information about a license backup or restore operation.</span></span>

<span data-ttu-id="af292-107">Questa interfaccia viene fornita con gli eventi di stato generati durante le operazioni di backup e ripristino delle licenze.</span><span class="sxs-lookup"><span data-stu-id="af292-107">This interface is delivered with progress events generated during license backup and restore operations.</span></span> <span data-ttu-id="af292-108">Durante il backup delle licenze vengono generati diversi eventi **MEWMDRMLicenseBackupProgress** , ognuno dei quali dispone di un'istanza associata di questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="af292-108">Several **MEWMDRMLicenseBackupProgress** events are generated during license backup, each of which has an accompanying instance of this interface.</span></span> <span data-ttu-id="af292-109">Lo stesso vale per gli eventi **MEWMDRMLicenseRestoreProgress** , che vengono generati durante il ripristino delle licenze.</span><span class="sxs-lookup"><span data-stu-id="af292-109">The same is true of **MEWMDRMLicenseRestoreProgress** events, which are generated during license restoration.</span></span>

<span data-ttu-id="af292-110">Per recuperare un puntatore a un'istanza dell'interfaccia **IWMDRMLicenseBackupRestoreStatus** , è prima necessario chiamare il metodo **IMFMediaEvent:: GetValue** dell'evento Progress.</span><span class="sxs-lookup"><span data-stu-id="af292-110">To retrieve a pointer to an instance of the **IWMDRMLicenseBackupRestoreStatus** interface, you must first call the **IMFMediaEvent::GetValue** method of the progress event.</span></span> <span data-ttu-id="af292-111">Il valore recuperato dall'evento è un puntatore all'interfaccia **IUnknown** dell'oggetto che implementa l'interfaccia **IWMDRMLicenseBackupRestoreStatus** .</span><span class="sxs-lookup"><span data-stu-id="af292-111">The value you retrieve from the event is a pointer to the **IUnknown** interface of the object that implements the **IWMDRMLicenseBackupRestoreStatus** interface.</span></span>

## <a name="members"></a><span data-ttu-id="af292-112">Membri</span><span class="sxs-lookup"><span data-stu-id="af292-112">Members</span></span>

<span data-ttu-id="af292-113">L'interfaccia **IWMDRMLicenseBackupRestoreStatus** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="af292-113">The **IWMDRMLicenseBackupRestoreStatus** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="af292-114">**IWMDRMLicenseBackupRestoreStatus** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="af292-114">**IWMDRMLicenseBackupRestoreStatus** also has these types of members:</span></span>

-   [<span data-ttu-id="af292-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="af292-115">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="af292-116">Metodi</span><span class="sxs-lookup"><span data-stu-id="af292-116">Methods</span></span>

<span data-ttu-id="af292-117">L'interfaccia **IWMDRMLicenseBackupRestoreStatus** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="af292-117">The **IWMDRMLicenseBackupRestoreStatus** interface has these methods.</span></span>



| <span data-ttu-id="af292-118">Metodo</span><span class="sxs-lookup"><span data-stu-id="af292-118">Method</span></span>                                                          | <span data-ttu-id="af292-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="af292-119">Description</span></span>                                                                                   |
|:----------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="af292-120">**GetStatus**</span><span class="sxs-lookup"><span data-stu-id="af292-120">**GetStatus**</span></span>](iwmdrmlicensebackuprestorestatus-getstatus.md) | <span data-ttu-id="af292-121">Recupera informazioni dettagliate sullo stato di un'operazione di backup o ripristino delle licenze.</span><span class="sxs-lookup"><span data-stu-id="af292-121">Retrieves detailed status information about a license backup or restore operation.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="af292-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="af292-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af292-123">**Interfacce**</span><span class="sxs-lookup"><span data-stu-id="af292-123">**Interfaces**</span></span>](drm-interfaces.md)
</dt> </dl>

 

