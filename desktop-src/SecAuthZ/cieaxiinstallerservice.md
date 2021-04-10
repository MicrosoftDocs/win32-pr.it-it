---
description: Implementa le interfacce IAxiService e IeAxiServiceCallback.
ms.assetid: 39f2ee3a-d4fd-4091-acd6-3d6b715bea75
title: Oggetto CIeAxiInstallerService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIeAxiInstallerService
api_type:
- COM
api_location: ''
ms.openlocfilehash: b5ae7ec2a2c904a523f3388fa08a3bf2e44fec9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966759"
---
# <a name="cieaxiinstallerservice-object"></a><span data-ttu-id="3addf-103">Oggetto CIeAxiInstallerService</span><span class="sxs-lookup"><span data-stu-id="3addf-103">CIeAxiInstallerService object</span></span>

<span data-ttu-id="3addf-104">L'oggetto **CIeAxiInstallerService** implementa le interfacce [**IAxiService**](ieaxiservice.md) e [**IeAxiServiceCallback**](ieaxiservicecallback.md) .</span><span class="sxs-lookup"><span data-stu-id="3addf-104">The **CIeAxiInstallerService** object implements the [**IAxiService**](ieaxiservice.md) and [**IeAxiServiceCallback**](ieaxiservicecallback.md) interfaces.</span></span>

<span data-ttu-id="3addf-105">Questo oggetto non è dichiarato in un'intestazione pubblica.</span><span class="sxs-lookup"><span data-stu-id="3addf-105">This object is not declared in a public header.</span></span> <span data-ttu-id="3addf-106">Le applicazioni devono definirle autonomamente.</span><span class="sxs-lookup"><span data-stu-id="3addf-106">Applications must define it themselves.</span></span> <span data-ttu-id="3addf-107">Il frammento IDL (Interface Definition Language) seguente descrive questo oggetto, incluso il relativo CLSID.</span><span class="sxs-lookup"><span data-stu-id="3addf-107">The following Interface Definition Language (IDL) fragment describes this object, including its CLSID.</span></span>

``` syntax
[
        uuid(90F18417-F0F1-484E-9D3C-59DCEEE5DBD8)
]
    coclass CIeAxiInstallerService
    {
        [default] interface IeAxiService;
        interface IeAxiServiceCallback;
    }

```

## <a name="requirements"></a><span data-ttu-id="3addf-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3addf-108">Requirements</span></span>



| <span data-ttu-id="3addf-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="3addf-109">Requirement</span></span> | <span data-ttu-id="3addf-110">Valore</span><span class="sxs-lookup"><span data-stu-id="3addf-110">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3addf-111">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3addf-111">Minimum supported client</span></span><br/> | <span data-ttu-id="3addf-112">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[ desktop apps\]</span><span class="sxs-lookup"><span data-stu-id="3addf-112">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="3addf-113">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3addf-113">Minimum supported server</span></span><br/> | <span data-ttu-id="3addf-114">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="3addf-114">None supported</span></span><br/>                                                                                 |



## <a name="see-also"></a><span data-ttu-id="3addf-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3addf-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3addf-116">**IAxiService**</span><span class="sxs-lookup"><span data-stu-id="3addf-116">**IAxiService**</span></span>](ieaxiservice.md)
</dt> <dt>

[<span data-ttu-id="3addf-117">**IeAxiServiceCallback**</span><span class="sxs-lookup"><span data-stu-id="3addf-117">**IeAxiServiceCallback**</span></span>](ieaxiservicecallback.md)
</dt> </dl>

 

 




