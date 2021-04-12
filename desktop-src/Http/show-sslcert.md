---
title: show sslcert
description: Elenca i binding del certificato server SSL e i criteri dei certificati client corrispondenti per un indirizzo IP e una porta.
ms.assetid: 8e20f55e-a357-4f9c-a24e-e234607c3196
keywords:
- Mostra HTTP sslcert
topic_type:
- apiref
api_name:
- show sslcert
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b71c2faf370066f5ce8d5ce6a20b173a74d0f645
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/06/2019
ms.locfileid: "104335060"
---
# <a name="show-sslcert"></a><span data-ttu-id="f64ad-104">show sslcert</span><span class="sxs-lookup"><span data-stu-id="f64ad-104">show sslcert</span></span>

<span data-ttu-id="f64ad-105">Elenca i binding del certificato server SSL e i criteri dei certificati client corrispondenti per un indirizzo IP e una porta.</span><span class="sxs-lookup"><span data-stu-id="f64ad-105">Lists SSL server certificate bindings and the corresponding client certificate policies for an IP address and port.</span></span>

``` syntax
show sslcert [ipport=]IP Address:port
 
```

## <a name="parameters"></a><span data-ttu-id="f64ad-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f64ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f64ad-107"><span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>\**\[ipport = \] \* \* \* indirizzo IP: porta*</span><span class="sxs-lookup"><span data-stu-id="f64ad-107"><span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>\**\[ipport=\]\*\*\*IP Address:port*</span></span>
</dt> <dd>

<span data-ttu-id="f64ad-108">Specifica l'indirizzo IPv4 o IPv6 e la porta per cui verranno visualizzate le associazioni di certificati SSL.</span><span class="sxs-lookup"><span data-stu-id="f64ad-108">Specifies the IPv4 or IPv6 address and port for which the SSL certificate bindings will be displayed.</span></span> <span data-ttu-id="f64ad-109">Se non si specifica un ipport, vengono elencati tutti i binding.</span><span class="sxs-lookup"><span data-stu-id="f64ad-109">Not specifying an ipport lists all bindings.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="f64ad-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="f64ad-110">Examples</span></span>

<span data-ttu-id="f64ad-111">**Mostra sslcert ipport = \[ FE80:: 1 \] : 443**</span><span class="sxs-lookup"><span data-stu-id="f64ad-111">**show sslcert ipport=\[fe80::1\]:443**</span></span>

<span data-ttu-id="f64ad-112">**show sslcert ipport=1.1.1.1:443**</span><span class="sxs-lookup"><span data-stu-id="f64ad-112">**show sslcert ipport=1.1.1.1:443**</span></span>

<span data-ttu-id="f64ad-113">**show sslcert ipport=0.0.0.0:443**</span><span class="sxs-lookup"><span data-stu-id="f64ad-113">**show sslcert ipport=0.0.0.0:443**</span></span>

<span data-ttu-id="f64ad-114">**Mostra sslcert ipport = \[ :: \] : 443**</span><span class="sxs-lookup"><span data-stu-id="f64ad-114">**show sslcert ipport=\[::\]:443**</span></span>

 

 




