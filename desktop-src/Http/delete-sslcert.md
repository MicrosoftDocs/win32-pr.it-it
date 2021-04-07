---
title: delete sslcert
description: Elimina i binding del certificato server SSL e i criteri dei certificati client corrispondenti per un indirizzo IP e una porta.
ms.assetid: 2adea7a8-f31f-4c02-8279-7d452e36cd9b
keywords:
- Elimina HTTP sslcert
topic_type:
- apiref
api_name:
- delete sslcert
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7672df5eee1634c41ff153435edcbecc58c2595
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/06/2019
ms.locfileid: "103719003"
---
# <a name="delete-sslcert"></a><span data-ttu-id="bdf56-104">delete sslcert</span><span class="sxs-lookup"><span data-stu-id="bdf56-104">delete sslcert</span></span>

<span data-ttu-id="bdf56-105">Elimina i binding del certificato server SSL e i criteri dei certificati client corrispondenti per un indirizzo IP e una porta.</span><span class="sxs-lookup"><span data-stu-id="bdf56-105">Deletes SSL server certificate bindings and the corresponding client certificate policies for an IP address and port.</span></span>

``` syntax
delete sslcert [ipport=]IP Address:port
 
```

## <a name="parameters"></a><span data-ttu-id="bdf56-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bdf56-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdf56-107"><span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>\**\[ipport = \] \* \* \* indirizzo IP: porta*</span><span class="sxs-lookup"><span data-stu-id="bdf56-107"><span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>\**\[ipport=\]\*\*\*IP Address:port*</span></span>
</dt> <dd>

<span data-ttu-id="bdf56-108">Specifica l'indirizzo IPv4 o IPv6 e la porta per cui verranno eliminati i binding del certificato SSL.</span><span class="sxs-lookup"><span data-stu-id="bdf56-108">Specifies the IPv4 or IPv6 address and port for which the SSL certificate bindings will be deleted.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="bdf56-109">Esempio</span><span class="sxs-lookup"><span data-stu-id="bdf56-109">Examples</span></span>

<span data-ttu-id="bdf56-110">**delete sslcert ipport=1.1.1.1:443**</span><span class="sxs-lookup"><span data-stu-id="bdf56-110">**delete sslcert ipport=1.1.1.1:443**</span></span>

<span data-ttu-id="bdf56-111">**delete sslcert ipport=0.0.0.0:443**</span><span class="sxs-lookup"><span data-stu-id="bdf56-111">**delete sslcert ipport=0.0.0.0:443**</span></span>

<span data-ttu-id="bdf56-112">**Elimina sslcert ipport = \[ :: \] : 443**</span><span class="sxs-lookup"><span data-stu-id="bdf56-112">**delete sslcert ipport=\[::\]:443**</span></span>

 

 




