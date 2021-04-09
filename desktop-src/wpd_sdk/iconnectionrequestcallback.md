---
description: Definisce un singolo metodo di callback.
ms.assetid: 579f7a29-cd98-4d97-9f8e-9b786897df1c
title: Interfaccia IConnectionRequestCallback (Devpkey. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IConnectionRequestCallback
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: aca827de068ce221f013f03b35f88fd76a030dd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968600"
---
# <a name="iconnectionrequestcallback-interface"></a><span data-ttu-id="fdf2e-103">Interfaccia IConnectionRequestCallback</span><span class="sxs-lookup"><span data-stu-id="fdf2e-103">IConnectionRequestCallback interface</span></span>

<span data-ttu-id="fdf2e-104">L'interfaccia **IConnectionRequestCallback** definisce un solo metodo di callback.</span><span class="sxs-lookup"><span data-stu-id="fdf2e-104">The **IConnectionRequestCallback** interface defines a single callback method.</span></span> <span data-ttu-id="fdf2e-105">Un'applicazione Windows Portable Devices (WPD) implementa questa interfaccia facoltativa Component Object Model (COM) per ricevere notifiche sulle richieste completate e per annullare le richieste in sospeso.</span><span class="sxs-lookup"><span data-stu-id="fdf2e-105">A Windows Portable Devices (WPD) application implements this optional Component Object Model (COM) interface to receive notifications about completed requests and to cancel pending requests.</span></span> <span data-ttu-id="fdf2e-106">Le richieste vengono inviate usando i metodi [**IPortableDeviceConnector:: Connect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-connect) e [**IPortableDeviceConnector::D di connessione**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-disconnect) .</span><span class="sxs-lookup"><span data-stu-id="fdf2e-106">The requests are sent using the [**IPortableDeviceConnector::Connect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-connect) and [**IPortableDeviceConnector::Disconnect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-disconnect) methods.</span></span>

## <a name="members"></a><span data-ttu-id="fdf2e-107">Membri</span><span class="sxs-lookup"><span data-stu-id="fdf2e-107">Members</span></span>

<span data-ttu-id="fdf2e-108">L'interfaccia **IConnectionRequestCallback** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="fdf2e-108">The **IConnectionRequestCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="fdf2e-109">**IConnectionRequestCallback** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="fdf2e-109">**IConnectionRequestCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="fdf2e-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="fdf2e-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="fdf2e-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="fdf2e-111">Methods</span></span>

<span data-ttu-id="fdf2e-112">L'interfaccia **IConnectionRequestCallback** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="fdf2e-112">The **IConnectionRequestCallback** interface has these methods.</span></span>



| <span data-ttu-id="fdf2e-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="fdf2e-113">Method</span></span>                                                      | <span data-ttu-id="fdf2e-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fdf2e-114">Description</span></span>                                                                           |
|:------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="fdf2e-115">**OnComplete**</span><span class="sxs-lookup"><span data-stu-id="fdf2e-115">**OnComplete**</span></span>](iconnectionrequestcallback-oncomplete.md) | <span data-ttu-id="fdf2e-116">Notifica a un'applicazione che una richiesta pianificata in precedenza è stata completata.</span><span class="sxs-lookup"><span data-stu-id="fdf2e-116">Notifies an application that a previously scheduled request has completed.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="fdf2e-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fdf2e-117">Requirements</span></span>



| <span data-ttu-id="fdf2e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="fdf2e-118">Requirement</span></span> | <span data-ttu-id="fdf2e-119">Valore</span><span class="sxs-lookup"><span data-stu-id="fdf2e-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fdf2e-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fdf2e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fdf2e-121">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="fdf2e-121">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                             |
| <span data-ttu-id="fdf2e-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fdf2e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fdf2e-123">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="fdf2e-123">None supported</span></span><br/>                                                                                                                                              |
| <span data-ttu-id="fdf2e-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fdf2e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="fdf2e-125"><dt>Devpkey. h; </dt> <dt>PortableDeviceConnectApi. h</dt></span><span class="sxs-lookup"><span data-stu-id="fdf2e-125"><dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt></span></span> </dl> |
| <span data-ttu-id="fdf2e-126">IDL</span><span class="sxs-lookup"><span data-stu-id="fdf2e-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fdf2e-127"><dt>PortableDeviceConnectApi. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fdf2e-127"><dt>Portabledeviceconnectapi.idl</dt></span></span> </dl>                                                                |
| <span data-ttu-id="fdf2e-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="fdf2e-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="fdf2e-129"><dt>PortableDeviceGuids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fdf2e-129"><dt>PortableDeviceGuids.lib</dt></span></span> </dl>                                                                     |



 

