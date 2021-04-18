---
title: Proprietà NetworkConnectionType di IMsRdpClientAdvancedSettings7
description: Ottiene o imposta il tipo di connessione di rete utilizzato tra il client e il server. Le informazioni sul tipo di connessione di rete passate al server consentono al server di ottimizzare diversi parametri in base al tipo di connessione di rete.
ms.assetid: 4dd4fa17-f121-412d-a30d-1c01f4c892b0
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà NetworkConnectionType
- Servizi Desktop remoto proprietà NetworkConnectionType, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà NetworkConnectionType
- Servizi Desktop remoto proprietà NetworkConnectionType, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà NetworkConnectionType
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.NetworkConnectionType
- IMsRdpClientAdvancedSettings7.get_NetworkConnectionType
- IMsRdpClientAdvancedSettings7.put_NetworkConnectionType
- IMsRdpClientAdvancedSettings8.NetworkConnectionType
- IMsRdpClientAdvancedSettings8.get_NetworkConnectionType
- IMsRdpClientAdvancedSettings8.put_NetworkConnectionType
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5df4c1e944920759f56f5d4b493b9cd47e7ebc29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301891"
---
# <a name="imsrdpclientadvancedsettings7networkconnectiontype-property"></a><span data-ttu-id="7869b-109">Proprietà IMsRdpClientAdvancedSettings7:: NetworkConnectionType</span><span class="sxs-lookup"><span data-stu-id="7869b-109">IMsRdpClientAdvancedSettings7::NetworkConnectionType property</span></span>

<span data-ttu-id="7869b-110">Ottiene o imposta il tipo di connessione di rete utilizzato tra il client e il server.</span><span class="sxs-lookup"><span data-stu-id="7869b-110">Gets or sets the type of network connection used between the client and server.</span></span> <span data-ttu-id="7869b-111">Le informazioni sul tipo di connessione di rete passate al server consentono al server di ottimizzare diversi parametri in base al tipo di connessione di rete.</span><span class="sxs-lookup"><span data-stu-id="7869b-111">The network connection type information passed on to the server helps the server tune several parameters based on the network connection type.</span></span>

<span data-ttu-id="7869b-112">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="7869b-112">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7869b-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7869b-113">Syntax</span></span>


```C++
HRESULT put_NetworkConnectionType(
  [in]          UINT connectionType
);

HRESULT get_NetworkConnectionType(
  [out, retval] UINT *pConnectionType
);
```



## <a name="property-value"></a><span data-ttu-id="7869b-114">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="7869b-114">Property value</span></span>

<span data-ttu-id="7869b-115">Tipo di connessione di rete.</span><span class="sxs-lookup"><span data-stu-id="7869b-115">The network connection type.</span></span>

<dt>

<span id="CONNECTION_TYPE_MODEM"></span><span id="connection_type_modem"></span>

<span data-ttu-id="7869b-116"><span id="CONNECTION_TYPE_MODEM"></span><span id="connection_type_modem"></span>**Connessione \_ a TIPO \_ modem** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="7869b-116"><span id="CONNECTION_TYPE_MODEM"></span><span id="connection_type_modem"></span>**CONNECTION\_TYPE\_MODEM** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="7869b-117">Modem (56 Kbps)</span><span class="sxs-lookup"><span data-stu-id="7869b-117">Modem (56 Kbps)</span></span>

</dd> <dt>

<span id="CONNECTION_TYPE_BROADBAND_LOW"></span><span id="connection_type_broadband_low"></span>

<span data-ttu-id="7869b-118"><span id="CONNECTION_TYPE_BROADBAND_LOW"></span><span id="connection_type_broadband_low"></span>**Connessione \_ a TIPO \_ Broadband \_ low** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="7869b-118"><span id="CONNECTION_TYPE_BROADBAND_LOW"></span><span id="connection_type_broadband_low"></span>**CONNECTION\_TYPE\_BROADBAND\_LOW** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="7869b-119">Banda larga a bassa velocità (256 kbps a 2 Mbps)</span><span class="sxs-lookup"><span data-stu-id="7869b-119">Low-speed broadband (256 Kbps to 2 Mbps)</span></span>

</dd> <dt>

<span id="CONNECTION_TYPE_SATELLITE"></span><span id="connection_type_satellite"></span>

<span data-ttu-id="7869b-120"><span id="CONNECTION_TYPE_SATELLITE"></span><span id="connection_type_satellite"></span>**Connessione \_ a Digitare \_ satellite** (3 (0x3))</span><span class="sxs-lookup"><span data-stu-id="7869b-120"><span id="CONNECTION_TYPE_SATELLITE"></span><span id="connection_type_satellite"></span>**CONNECTION\_TYPE\_SATELLITE** (3 (0x3))</span></span>


</dt> <dd>

<span data-ttu-id="7869b-121">Satellite (da 2 Mbps a 16 Mbps, con latenza elevata)</span><span class="sxs-lookup"><span data-stu-id="7869b-121">Satellite (2 Mbps to 16 Mbps, with high latency)</span></span>

</dd> <dt>

<span id="CONNECTION_TYPE_BROADBAND_HIGH"></span><span id="connection_type_broadband_high"></span>

<span data-ttu-id="7869b-122"><span id="CONNECTION_TYPE_BROADBAND_HIGH"></span><span id="connection_type_broadband_high"></span>**Connessione \_ a Digitare \_ Broadband \_ High** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="7869b-122"><span id="CONNECTION_TYPE_BROADBAND_HIGH"></span><span id="connection_type_broadband_high"></span>**CONNECTION\_TYPE\_BROADBAND\_HIGH** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="7869b-123">Banda larga ad alta velocità (da 2 Mbps a 10 Mbps)</span><span class="sxs-lookup"><span data-stu-id="7869b-123">High-speed broadband (2 Mbps to 10 Mbps)</span></span>

</dd> <dt>

<span id="CONNECTION_TYPE_WAN"></span><span id="connection_type_wan"></span>

<span data-ttu-id="7869b-124"><span id="CONNECTION_TYPE_WAN"></span><span id="connection_type_wan"></span>**Connessione \_ a Digitare \_ WAN** (5 (0x5))</span><span class="sxs-lookup"><span data-stu-id="7869b-124"><span id="CONNECTION_TYPE_WAN"></span><span id="connection_type_wan"></span>**CONNECTION\_TYPE\_WAN** (5 (0x5))</span></span>


</dt> <dd>

<span data-ttu-id="7869b-125">WAN (Wide Area Network) (10 Mbps o superiore, con latenza elevata)</span><span class="sxs-lookup"><span data-stu-id="7869b-125">Wide area network (WAN) (10 Mbps or higher, with high latency)</span></span>

</dd> <dt>

<span id="CONNECTION_TYPE_LAN"></span><span id="connection_type_lan"></span>

<span data-ttu-id="7869b-126"><span id="CONNECTION_TYPE_LAN"></span><span id="connection_type_lan"></span>**Connessione \_ a Digitare \_ LAN** (6 (0x6))</span><span class="sxs-lookup"><span data-stu-id="7869b-126"><span id="CONNECTION_TYPE_LAN"></span><span id="connection_type_lan"></span>**CONNECTION\_TYPE\_LAN** (6 (0x6))</span></span>


</dt> <dd>

<span data-ttu-id="7869b-127">LAN (Local Area Network) (10 Mbps o versione successiva)</span><span class="sxs-lookup"><span data-stu-id="7869b-127">Local area network (LAN) (10 Mbps or higher)</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7869b-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7869b-128">Requirements</span></span>



| <span data-ttu-id="7869b-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="7869b-129">Requirement</span></span> | <span data-ttu-id="7869b-130">Valore</span><span class="sxs-lookup"><span data-stu-id="7869b-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7869b-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7869b-131">Minimum supported client</span></span><br/> | <span data-ttu-id="7869b-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7869b-132">Windows 7</span></span><br/>                                                                             |
| <span data-ttu-id="7869b-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7869b-133">Minimum supported server</span></span><br/> | <span data-ttu-id="7869b-134">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7869b-134">Windows Server 2008 R2</span></span><br/>                                                                |
| <span data-ttu-id="7869b-135">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="7869b-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="7869b-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7869b-136"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="7869b-137">DLL</span><span class="sxs-lookup"><span data-stu-id="7869b-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7869b-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7869b-138"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="7869b-139">IID</span><span class="sxs-lookup"><span data-stu-id="7869b-139">IID</span></span><br/>                      | <span data-ttu-id="7869b-140">IID \_ IMsRdpClientAdvancedSettings7 è definito come 26036036-4010-4578-8091-0db9a1edf9c3</span><span class="sxs-lookup"><span data-stu-id="7869b-140">IID\_IMsRdpClientAdvancedSettings7 is defined as 26036036-4010-4578-8091-0db9a1edf9c3</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7869b-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7869b-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7869b-142">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="7869b-142">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="7869b-143">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="7869b-143">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





