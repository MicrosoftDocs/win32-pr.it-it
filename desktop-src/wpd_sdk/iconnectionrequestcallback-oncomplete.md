---
description: Notifica a un'applicazione che una richiesta di connessione o disconnessione pianificata in precedenza al dispositivo MTP/Bluetooth è stata completata.
ms.assetid: 1588d0ec-0d6a-4379-bfdc-4ba5fdaa4665
title: 'Metodo IConnectionRequestCallback:: OnComplete (Devpkey. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IConnectionRequestCallback.OnComplete
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: 922169b7e17335c47425665bb9a9e54891e68723
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883166"
---
# <a name="iconnectionrequestcallbackoncomplete-method"></a><span data-ttu-id="c58a5-103">Metodo IConnectionRequestCallback:: OnComplete</span><span class="sxs-lookup"><span data-stu-id="c58a5-103">IConnectionRequestCallback::OnComplete method</span></span>

<span data-ttu-id="c58a5-104">Il metodo **OnComplete** notifica a un'applicazione che una richiesta di connessione o disconnessione pianificata in precedenza al dispositivo MTP/Bluetooth è stata completata</span><span class="sxs-lookup"><span data-stu-id="c58a5-104">The **OnComplete** method notifies an application that a previously scheduled Connect or Disconnect request to the MTP/Bluetooth device has completed</span></span>

## <a name="syntax"></a><span data-ttu-id="c58a5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c58a5-105">Syntax</span></span>


```C++
HRESULT OnComplete(
  [in] HRESULT hrStatus
);
```



## <a name="parameters"></a><span data-ttu-id="c58a5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c58a5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c58a5-107">*hrStatus* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c58a5-107">*hrStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c58a5-108">Stato della richiesta di connessione o disconnessione di un dispositivo specifico.</span><span class="sxs-lookup"><span data-stu-id="c58a5-108">The status of the request to connect or disconnect a given device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c58a5-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c58a5-109">Return value</span></span>

<span data-ttu-id="c58a5-110">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="c58a5-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="c58a5-111">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="c58a5-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="c58a5-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="c58a5-112">Return code</span></span>                                                                          | <span data-ttu-id="c58a5-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c58a5-113">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="c58a5-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c58a5-114"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="c58a5-115">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="c58a5-115">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c58a5-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="c58a5-116">Remarks</span></span>

<span data-ttu-id="c58a5-117">Un'applicazione implementa l'interfaccia [**IConnectionRequestCallback**](iconnectionrequestcallback.md) per ricevere notifiche sulle richieste completate e per annullare richieste in sospeso.</span><span class="sxs-lookup"><span data-stu-id="c58a5-117">An application implements the [**IConnectionRequestCallback**](iconnectionrequestcallback.md) interface to receive notifications about completed requests and to cancel pending requests.</span></span>

<span data-ttu-id="c58a5-118">Dispositivi portatili Windows (WPD) chiama questo metodo per notificare a un'applicazione che una richiesta pianificata in precedenza è stata completata.</span><span class="sxs-lookup"><span data-stu-id="c58a5-118">Windows Portable Devices (WPD) calls this method to notify an application that a previously scheduled request has completed.</span></span> <span data-ttu-id="c58a5-119">Ogni richiesta può essere rilevata e annullata dal callback fornito dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c58a5-119">Each request can be tracked and canceled by its application-supplied callback.</span></span> <span data-ttu-id="c58a5-120">Pertanto, se l'applicazione deve inviare più richieste contemporaneamente usando lo stesso oggetto [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) , a ogni richiesta deve essere passato un oggetto [**IConnectionRequestCallback**](iconnectionrequestcallback.md) univoco come parametro di input ai metodi [**IPortableDeviceConnector:: Connect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-connect) e [**IPortableDeviceConnector::D di connessione**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-disconnect) .</span><span class="sxs-lookup"><span data-stu-id="c58a5-120">Therefore, if the application needs to send multiple requests at the same time using the same [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) object, each request should be passed a unique [**IConnectionRequestCallback**](iconnectionrequestcallback.md) object as the input parameter to the [**IPortableDeviceConnector::Connect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-connect) and [**IPortableDeviceConnector::Disconnect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-disconnect) methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="c58a5-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c58a5-121">Requirements</span></span>



| <span data-ttu-id="c58a5-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c58a5-122">Requirement</span></span> | <span data-ttu-id="c58a5-123">Valore</span><span class="sxs-lookup"><span data-stu-id="c58a5-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c58a5-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c58a5-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c58a5-125">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c58a5-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                             |
| <span data-ttu-id="c58a5-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c58a5-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c58a5-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="c58a5-127">None supported</span></span><br/>                                                                                                                                              |
| <span data-ttu-id="c58a5-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c58a5-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c58a5-129"><dt>Devpkey. h; </dt> <dt>PortableDeviceConnectApi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c58a5-129"><dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt></span></span> </dl> |
| <span data-ttu-id="c58a5-130">IDL</span><span class="sxs-lookup"><span data-stu-id="c58a5-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c58a5-131"><dt>PortableDeviceConnectApi. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c58a5-131"><dt>Portabledeviceconnectapi.idl</dt></span></span> </dl>                                                                |
| <span data-ttu-id="c58a5-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="c58a5-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="c58a5-133"><dt>PortableDeviceGuids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c58a5-133"><dt>PortableDeviceGuids.lib</dt></span></span> </dl>                                                                     |



## <a name="see-also"></a><span data-ttu-id="c58a5-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c58a5-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c58a5-135">**IConnectionRequestCallback**</span><span class="sxs-lookup"><span data-stu-id="c58a5-135">**IConnectionRequestCallback**</span></span>](iconnectionrequestcallback.md)
</dt> </dl>

 

 




