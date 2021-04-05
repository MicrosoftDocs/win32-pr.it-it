---
description: Ottiene la versione del motore di elaborazione WPAD.
ms.assetid: f9e9a867-d491-4d46-bbd8-c0c3d8d5b3d6
title: getClientVersion (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- dnsResolveEx
api_type:
- NA
api_location: ''
ms.openlocfilehash: e0bcf439c8a282e42a28126824ffb70630a341e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882874"
---
# <a name="getclientversion-function"></a><span data-ttu-id="c3a84-103">getClientVersion (funzione)</span><span class="sxs-lookup"><span data-stu-id="c3a84-103">getClientVersion function</span></span>

<span data-ttu-id="c3a84-104">Ottiene la versione del motore di elaborazione WPAD.</span><span class="sxs-lookup"><span data-stu-id="c3a84-104">Gets the version of the WPAD processing engine.</span></span>

## <a name="parameters"></a><span data-ttu-id="c3a84-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="c3a84-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3a84-106">*IpAddress*</span><span class="sxs-lookup"><span data-stu-id="c3a84-106">*IpAddressList*</span></span> 
</dt> <dd>

<span data-ttu-id="c3a84-107">Stringa delimitata da punto e virgola contenente indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="c3a84-107">A semi-colon delimited string containing IP addresses.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3a84-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c3a84-108">Return value</span></span>

<span data-ttu-id="c3a84-109">Elenco di indirizzi IP delimitati da punti e virgola o una stringa vuota se non è possibile ordinare l'elenco di indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="c3a84-109">A list of sorted semi-colon delimited IP addresses or an empty string if unable to sort the IP Address list.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3a84-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="c3a84-110">Remarks</span></span>

<span data-ttu-id="c3a84-111">Attualmente questa funzione restituisce la versione 1,0.</span><span class="sxs-lookup"><span data-stu-id="c3a84-111">Currently this function returns version 1.0.</span></span>

<span data-ttu-id="c3a84-112">Microsoft ha aggiunto questa funzione per consentire agli amministratori IT di aggiornare gli script WPAD per l'uso di versioni diverse del motore di elaborazione WPAD senza causare interruzioni della distribuzione esistente.</span><span class="sxs-lookup"><span data-stu-id="c3a84-112">Microsoft added this function to allow IT administrators to update their WPAD scripts to use different versions of the WPAD processing engine without causing breaks to their existing deployment.</span></span> <span data-ttu-id="c3a84-113">Se ad esempio Microsoft ha aggiunto una funzione alla versione 2,0 del motore WPAD, gli amministratori possono verificare la versione prima di tentare di chiamare tale funzione.</span><span class="sxs-lookup"><span data-stu-id="c3a84-113">For example, if Microsoft added a function to the 2.0 version of the WPAD engine, then administrators can check the version before attempting to call that function.</span></span> <span data-ttu-id="c3a84-114">Questo consente di usare lo script con il client che esegue le versioni 1,0 e 2,0 del motore WPAD.</span><span class="sxs-lookup"><span data-stu-id="c3a84-114">This allows their script to work with client running versions 1.0 and 2.0 of the WPAD engine.</span></span>

## <a name="examples"></a><span data-ttu-id="c3a84-115">Esempi</span><span class="sxs-lookup"><span data-stu-id="c3a84-115">Examples</span></span>

``` syntax
getClientVersion();
    returns the appropriate versions number of the WPAD engine.
```

## <a name="see-also"></a><span data-ttu-id="c3a84-116">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="c3a84-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3a84-117">Definizioni API helper proxy compatibili con IPv6</span><span class="sxs-lookup"><span data-stu-id="c3a84-117">IPv6-Aware Proxy Helper API Definitions</span></span>](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[<span data-ttu-id="c3a84-118">Estensioni IPv6 per il formato di file di configurazione automatica dello strumento di navigazione</span><span class="sxs-lookup"><span data-stu-id="c3a84-118">IPv6 Extensions to Navigator Auto-Config File Format</span></span>](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



