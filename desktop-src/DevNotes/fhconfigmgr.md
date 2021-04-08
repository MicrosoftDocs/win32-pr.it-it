---
description: Rappresenta la configurazione della cronologia file dell'utente in cui viene creato l'oggetto FhConfigMgr. Tutte le operazioni di configurazione vengono eseguite chiamando i metodi dell'interfaccia IFhConfigMgr.
ms.assetid: CC97FC0F-3AA4-4D8A-81B3-14F68FDF5788
title: Classe FhConfigMgr (Fhcfg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FhConfigMgr
api_type:
- COM
api_location:
- Fhcfg.idl
ms.openlocfilehash: 083ce344e44035b5872d91ad14465659defc8229
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877721"
---
# <a name="fhconfigmgr-class"></a><span data-ttu-id="eb481-104">Classe FhConfigMgr</span><span class="sxs-lookup"><span data-stu-id="eb481-104">FhConfigMgr class</span></span>

<span data-ttu-id="eb481-105">Rappresenta la configurazione della cronologia file dell'utente in cui viene creato l'oggetto **FhConfigMgr** .</span><span class="sxs-lookup"><span data-stu-id="eb481-105">Represents the File History configuration of the user under which the **FhConfigMgr** object is created.</span></span> <span data-ttu-id="eb481-106">Tutte le operazioni di configurazione vengono eseguite chiamando i metodi dell'interfaccia [**IFhConfigMgr**](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhconfigmgr) .</span><span class="sxs-lookup"><span data-stu-id="eb481-106">All configuration operations are performed by calling the methods of the [**IFhConfigMgr**](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhconfigmgr) interface.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="eb481-107">Quando implementare</span><span class="sxs-lookup"><span data-stu-id="eb481-107">When to implement</span></span>

<span data-ttu-id="eb481-108">L'API cronologia file implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="eb481-108">The File History API implements this class.</span></span> <span data-ttu-id="eb481-109">Per creare un'istanza di questa classe, utilizzare la funzione [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .</span><span class="sxs-lookup"><span data-stu-id="eb481-109">To create an instance of this class, use the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb481-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eb481-110">Requirements</span></span>



| <span data-ttu-id="eb481-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb481-111">Requirement</span></span> | <span data-ttu-id="eb481-112">Valore</span><span class="sxs-lookup"><span data-stu-id="eb481-112">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="eb481-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eb481-113">Minimum supported client</span></span><br/> | <span data-ttu-id="eb481-114">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="eb481-114">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="eb481-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eb481-115">Minimum supported server</span></span><br/> | <span data-ttu-id="eb481-116">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="eb481-116">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="eb481-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eb481-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb481-118"><dt>Fhcfg. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb481-118"><dt>Fhcfg.h</dt></span></span> </dl>   |
| <span data-ttu-id="eb481-119">IDL</span><span class="sxs-lookup"><span data-stu-id="eb481-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="eb481-120"><dt>Fhcfg. idl</dt></span><span class="sxs-lookup"><span data-stu-id="eb481-120"><dt>Fhcfg.idl</dt></span></span> </dl> |



 

 
