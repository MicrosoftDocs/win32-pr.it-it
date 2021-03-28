---
UID: NF:ntw.EtwEventUnregister
title: EtwEventUnregister (funzione)
description: Annulla la registrazione di un evento.
old-location: ''
ms.assetid: na
ms.date: 02/20/2018
ms.keywords: EtwEventUnregister
ms.topic: reference
req.header: ntetw.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1803 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 10, version 1803 [desktop apps \| UWP apps]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- ntetw.h
api_name:
- EtwEventUnregister
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: e61de5aa1c050aedd2c82dec471765baa7e6cdd7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104117687"
---
# <a name="etweventunregister-function"></a><span data-ttu-id="8942e-103">EtwEventUnregister (funzione)</span><span class="sxs-lookup"><span data-stu-id="8942e-103">EtwEventUnregister function</span></span>


## <a name="description"></a><span data-ttu-id="8942e-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8942e-104">Description</span></span>


<span data-ttu-id="8942e-105"><b>EtwEventUnregister</b> Annulla la registrazione di un evento.</span><span class="sxs-lookup"><span data-stu-id="8942e-105">The <b>EtwEventUnregister</b> unregisters an event.</span></span>
            

<span data-ttu-id="8942e-106">I provider possono chiamare questa funzione solo dalla relativa funzione <a href="/windows/desktop/ETW/controlcallback">ControlCallback</a> .</span><span class="sxs-lookup"><span data-stu-id="8942e-106">Providers can only call this function from their <a href="/windows/desktop/ETW/controlcallback">ControlCallback</a> function.</span></span>


## <a name="parameters"></a><span data-ttu-id="8942e-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="8942e-107">Parameters</span></span>




### <a name="reghandle-in"></a><span data-ttu-id="8942e-108">RegHandle [in]</span><span class="sxs-lookup"><span data-stu-id="8942e-108">RegHandle [in]</span></span>

<span data-ttu-id="8942e-109">Handle per un evento.</span><span class="sxs-lookup"><span data-stu-id="8942e-109">Handle to an event.</span></span>


## <a name="returns"></a><span data-ttu-id="8942e-110">Restituisce</span><span class="sxs-lookup"><span data-stu-id="8942e-110">Returns</span></span>



<span data-ttu-id="8942e-111">Restituisce un valore HRESULT.</span><span class="sxs-lookup"><span data-stu-id="8942e-111">Returns an HRESULT.</span></span>





## <a name="remarks"></a><span data-ttu-id="8942e-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="8942e-112">Remarks</span></span>



## <a name="see-also"></a><span data-ttu-id="8942e-113">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="8942e-113">See also</span></span>