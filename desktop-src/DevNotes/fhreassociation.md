---
description: Rappresenta la funzionalità di riassociazione cronologia file che consente a un utente di ristabilire una relazione con una destinazione di backup utilizzata dallo stesso utente in passato. La riassociazione viene eseguita chiamando i metodi dell'interfaccia IFhReassociation.
ms.assetid: BB81F8ED-4DFB-4FA5-B3ED-ACBAB32BBE3D
title: Classe FhReassociation (Fhcfg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FhReassociation
api_type:
- COM
api_location:
- Fhcfg.idl
ms.openlocfilehash: 1e303799a792e788fcb948ad6d3c6e2fd732e26e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304844"
---
# <a name="fhreassociation-class"></a><span data-ttu-id="ebb6e-104">Classe FhReassociation</span><span class="sxs-lookup"><span data-stu-id="ebb6e-104">FhReassociation class</span></span>

<span data-ttu-id="ebb6e-105">Rappresenta la funzionalità di riassociazione cronologia file che consente a un utente di ristabilire una relazione con una destinazione di backup utilizzata dallo stesso utente in passato.</span><span class="sxs-lookup"><span data-stu-id="ebb6e-105">Represents the File History reassociation feature, which allows a user to reestablish a relationship with a backup target that was used by the same user in the past.</span></span> <span data-ttu-id="ebb6e-106">La riassociazione viene eseguita chiamando i metodi dell'interfaccia [**IFhReassociation**](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhreassociation) .</span><span class="sxs-lookup"><span data-stu-id="ebb6e-106">Reassociation is performed by calling the methods of the [**IFhReassociation**](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhreassociation) interface.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="ebb6e-107">Quando implementare</span><span class="sxs-lookup"><span data-stu-id="ebb6e-107">When to implement</span></span>

<span data-ttu-id="ebb6e-108">L'API cronologia file implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="ebb6e-108">The File History API implements this class.</span></span> <span data-ttu-id="ebb6e-109">Per creare un'istanza di questa classe, utilizzare la funzione [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .</span><span class="sxs-lookup"><span data-stu-id="ebb6e-109">To create an instance of this class, use the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebb6e-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ebb6e-110">Requirements</span></span>



| <span data-ttu-id="ebb6e-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebb6e-111">Requirement</span></span> | <span data-ttu-id="ebb6e-112">Valore</span><span class="sxs-lookup"><span data-stu-id="ebb6e-112">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ebb6e-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ebb6e-113">Minimum supported client</span></span><br/> | <span data-ttu-id="ebb6e-114">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ebb6e-114">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ebb6e-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ebb6e-115">Minimum supported server</span></span><br/> | <span data-ttu-id="ebb6e-116">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ebb6e-116">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ebb6e-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ebb6e-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="ebb6e-118"><dt>Fhcfg. h</dt></span><span class="sxs-lookup"><span data-stu-id="ebb6e-118"><dt>Fhcfg.h</dt></span></span> </dl>   |
| <span data-ttu-id="ebb6e-119">IDL</span><span class="sxs-lookup"><span data-stu-id="ebb6e-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ebb6e-120"><dt>Fhcfg. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ebb6e-120"><dt>Fhcfg.idl</dt></span></span> </dl> |



 

 
