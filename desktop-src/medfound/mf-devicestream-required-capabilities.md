---
description: Specifica un elenco di stringhe Unicode che rappresentano le funzionalità del dispositivo richieste dalla trasformazione del sensore.
ms.assetid: 4A129FEB-E650-47C9-ABC0-9A512EE4121D
title: Attributo MF_DEVICESTREAM_REQUIRED_CAPABILITIES (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cac47d60c38e41d44ecf0776ea8bf7588559dfe1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129790"
---
# <a name="mf_devicestream_required_capabilities-attribute"></a><span data-ttu-id="3bab5-103">\_Attributo delle \_ \_ funzionalità obbligatorie di MF DEVICESTREAM</span><span class="sxs-lookup"><span data-stu-id="3bab5-103">MF\_DEVICESTREAM\_REQUIRED\_CAPABILITIES attribute</span></span>

<span data-ttu-id="3bab5-104">Specifica un elenco di stringhe Unicode che rappresentano le funzionalità del dispositivo richieste dalla trasformazione del sensore.</span><span class="sxs-lookup"><span data-stu-id="3bab5-104">Specifies a list of unicode strings representing the device capabilities required by the sensor transform.</span></span>

## <a name="data-type"></a><span data-ttu-id="3bab5-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="3bab5-105">Data type</span></span>

<span data-ttu-id="3bab5-106">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="3bab5-106">\**WCHAR\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="3bab5-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="3bab5-107">Remarks</span></span>

<span data-ttu-id="3bab5-108">Questo attributo è facoltativo ed è necessario solo se la trasformazione del sensore accede a una risorsa protetta.</span><span class="sxs-lookup"><span data-stu-id="3bab5-108">This attribute is optional and only required if the sensor transform accesses a protected resource.</span></span> <span data-ttu-id="3bab5-109">Il valore deve essere un elenco delimitato da punti e virgola di token di stringa definiti in [_ *DeviceCapability* \*](/uwp/schemas/appxpackage/appxmanifestschema/element-devicecapability).</span><span class="sxs-lookup"><span data-stu-id="3bab5-109">The value must be a semicolon delimited list of string tokens defined in [_ *DeviceCapability*\*](/uwp/schemas/appxpackage/appxmanifestschema/element-devicecapability).</span></span>

## <a name="requirements"></a><span data-ttu-id="3bab5-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3bab5-110">Requirements</span></span>



| <span data-ttu-id="3bab5-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="3bab5-111">Requirement</span></span> | <span data-ttu-id="3bab5-112">Valore</span><span class="sxs-lookup"><span data-stu-id="3bab5-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3bab5-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3bab5-113">Minimum supported client</span></span><br/> | <span data-ttu-id="3bab5-114">Solo app desktop Windows 10 versione 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="3bab5-114">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3bab5-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3bab5-115">Minimum supported server</span></span><br/> | <span data-ttu-id="3bab5-116">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="3bab5-116">None supported</span></span><br/>                                                          |
| <span data-ttu-id="3bab5-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3bab5-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="3bab5-118"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3bab5-118"><dt>Mfidl.h</dt></span></span> </dl> |



 

 
