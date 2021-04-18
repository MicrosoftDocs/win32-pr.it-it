---
title: Metodo IDeviceAccessPolicyCheck DeviceInterfaceClassAccessCheckWithCallingThread
description: Questa API determinerà se il token per il contesto corrente ha accesso alla classe di interfaccia del dispositivo specificata. IID 7D276FF2-CE90-4275-A2A8-9A48B10D3E0B.
ms.assetid: D7BFE1F3-4876-4BAB-A32D-46DB533140BB
keywords:
- API broker Access Device Method DeviceInterfaceClassAccessCheckWithCallingThread
- API gestore di accesso ai dispositivi del metodo DeviceInterfaceClassAccessCheckWithCallingThread, interfaccia IDeviceAccessPolicyCheck
- API del broker di accesso ai dispositivi dell'interfaccia IDeviceAccessPolicyCheck, metodo DeviceInterfaceClassAccessCheckWithCallingThread
topic_type:
- apiref
api_name:
- IDeviceAccessPolicyCheck.DeviceInterfaceClassAccessCheckWithCallingThread
api_type:
- COM
ms.topic: article
ms.date: 02/11/2020
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 44eb44a83175cf8f735abfeb8cfec4de83f46bd2
ms.sourcegitcommit: 01a4383738056cf3de4f45f36d98ef73d4dc694d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/11/2020
ms.locfileid: "106299369"
---
# <a name="ideviceaccesspolicycheckdeviceinterfaceclassaccesscheckwithcallingthread-method"></a><span data-ttu-id="1cc2b-107">IDeviceAccessPolicyCheck::D Metodo eviceInterfaceClassAccessCheckWithCallingThread</span><span class="sxs-lookup"><span data-stu-id="1cc2b-107">IDeviceAccessPolicyCheck::DeviceInterfaceClassAccessCheckWithCallingThread method</span></span>

> [!Important]  
> <span data-ttu-id="1cc2b-108">Queste interfacce non sono supportate e non devono essere usate.</span><span class="sxs-lookup"><span data-stu-id="1cc2b-108">These interfaces are not supported and should not be used.</span></span> <span data-ttu-id="1cc2b-109">Usare invece le API nella Guida di riferimento per la [programmazione di API di accesso ai dispositivi](device-access-api-c---programming-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="1cc2b-109">Use the APIs in the [Device Access API C++ Programming Reference](device-access-api-c---programming-reference.md) instead.</span></span>

<span data-ttu-id="1cc2b-110">Questa API determinerà se il token per il contesto corrente ha accesso alla classe di interfaccia del dispositivo specificata.</span><span class="sxs-lookup"><span data-stu-id="1cc2b-110">This API will determine if the token for the current context has access to the device interface class specified.</span></span> <span data-ttu-id="1cc2b-111">IID = 7D276FF2-CE90-4275-A2A8-9A48B10D3E0B.</span><span class="sxs-lookup"><span data-stu-id="1cc2b-111">IID = 7D276FF2-CE90-4275-A2A8-9A48B10D3E0B.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cc2b-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1cc2b-112">Syntax</span></span>

```C++
HRESULT DeviceInterfaceClassAccessCheckWithCallingThread(
  [in] PCWSTR pszDeviceInterfaceClassGuid,
  [in] DWORD  dwClientThreadId
);
```

## <a name="parameters"></a><span data-ttu-id="1cc2b-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="1cc2b-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cc2b-114">*pszDeviceInterfaceClassGuid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1cc2b-114">*pszDeviceInterfaceClassGuid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cc2b-115">GUID della classe dell'interfaccia del dispositivo per cui è necessario controllare l'accesso.</span><span class="sxs-lookup"><span data-stu-id="1cc2b-115">Device interface class GUID for which access should be checked.</span></span>

</dd> <dt>

<span data-ttu-id="1cc2b-116">*dwClientThreadId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1cc2b-116">*dwClientThreadId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cc2b-117">ID thread del client in cui deve essere visualizzata un'interfaccia utente associata, se necessario.</span><span class="sxs-lookup"><span data-stu-id="1cc2b-117">Client thread ID where any associated UI should be shown if necessary.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cc2b-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1cc2b-118">Return value</span></span>

<span data-ttu-id="1cc2b-119">Se questa funzione ha esito positivo, restituisce S_OK.</span><span class="sxs-lookup"><span data-stu-id="1cc2b-119">If this function succeeds, it returns S_OK.</span></span> <span data-ttu-id="1cc2b-120">In caso contrario, restituisce un codice di errore HRESULT.</span><span class="sxs-lookup"><span data-stu-id="1cc2b-120">Otherwise, it returns an HRESULT error code.</span></span>
