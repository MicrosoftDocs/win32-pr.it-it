---
description: Recupera uno o più oggetti IPortableDeviceConnector successivi nella sequenza di enumerazione.
ms.assetid: 5aed563a-5ecc-49c0-8a0c-622405453896
title: 'Metodo IEnumPortableDeviceConnectors:: Next (Devpkey. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPortableDeviceConnectors.Next
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: 709e938c28f9bf09e34d918eea7be3029c7a11e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317852"
---
# <a name="ienumportabledeviceconnectorsnext-method"></a><span data-ttu-id="dbae0-103">IEnumPortableDeviceConnectors:: Next (metodo)</span><span class="sxs-lookup"><span data-stu-id="dbae0-103">IEnumPortableDeviceConnectors::Next method</span></span>

<span data-ttu-id="dbae0-104">Il metodo **successivo** recupera i successivi uno o più oggetti [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) nella sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="dbae0-104">The **Next** method retrieves the next one or more [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) objects in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbae0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dbae0-105">Syntax</span></span>


```C++
HRESULT Next(
  [in]      UINT32                   cRequested,
  [out]     IPortableDeviceConnector **pConnectors,
  [in, out] UINT32                   *pcFetched
);
```



## <a name="parameters"></a><span data-ttu-id="dbae0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="dbae0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbae0-107">*cRequested* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dbae0-107">*cRequested* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbae0-108">Numero di dispositivi richiesti.</span><span class="sxs-lookup"><span data-stu-id="dbae0-108">The number of requested devices.</span></span> <span data-ttu-id="dbae0-109">Questo valore indica anche il numero di elementi nella matrice allocata dal chiamante specificata dal parametro *pConnectors* .</span><span class="sxs-lookup"><span data-stu-id="dbae0-109">This value also indicates the number of elements in the caller-allocated array specified by the *pConnectors* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="dbae0-110">*pConnectors* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="dbae0-110">*pConnectors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dbae0-111">Matrice di puntatori [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) , ognuno dei quali specifica un dispositivo Bluetooth MTP abbinato.</span><span class="sxs-lookup"><span data-stu-id="dbae0-111">An array of [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) pointers, each specifying a paired MTP Bluetooth device.</span></span> <span data-ttu-id="dbae0-112">Il chiamante deve allocare una matrice di puntatori **IPortableDeviceConnector** , con la lunghezza della matrice specificata dal parametro *cRequested* .</span><span class="sxs-lookup"><span data-stu-id="dbae0-112">The caller must allocate an array of **IPortableDeviceConnector** pointers, with the array length specified by the *cRequested* parameter.</span></span> <span data-ttu-id="dbae0-113">In esito positivo, il chiamante deve liberare sia la matrice che i puntatori restituiti.</span><span class="sxs-lookup"><span data-stu-id="dbae0-113">On successful return, the caller must free both the array and the returned pointers.</span></span> <span data-ttu-id="dbae0-114">Le interfacce **IPortableDeviceConnector** vengono liberate chiamando il metodo **IUnknown:: Release** .</span><span class="sxs-lookup"><span data-stu-id="dbae0-114">The **IPortableDeviceConnector** interfaces are freed by calling the **IUnknown::Release** method.</span></span>

</dd> <dt>

<span data-ttu-id="dbae0-115">*pcFetched* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="dbae0-115">*pcFetched* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="dbae0-116">Numero di interfacce [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) effettivamente recuperate.</span><span class="sxs-lookup"><span data-stu-id="dbae0-116">The number of [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) interfaces that are actually retrieved.</span></span> <span data-ttu-id="dbae0-117">Se non vengono recuperate interfacce **IPortableDeviceConnector** e il valore restituito è **S \_ false**, non sono disponibili altre interfacce **IPortableDeviceConnector** da enumerare.</span><span class="sxs-lookup"><span data-stu-id="dbae0-117">If no **IPortableDeviceConnector** interfaces are retrieved and the return value is **S\_FALSE**, there are no more **IPortableDeviceConnector** interfaces to enumerate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbae0-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dbae0-118">Return value</span></span>

<span data-ttu-id="dbae0-119">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="dbae0-119">The method returns an **HRESULT**.</span></span> <span data-ttu-id="dbae0-120">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="dbae0-120">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="dbae0-121">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="dbae0-121">Return code</span></span>                                                                             | <span data-ttu-id="dbae0-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dbae0-122">Description</span></span>                                                      |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="dbae0-123"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="dbae0-123"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="dbae0-124">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="dbae0-124">The method succeeded.</span></span><br/>                                 |
| <dl> <span data-ttu-id="dbae0-125"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="dbae0-125"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="dbae0-126">Non sono disponibili altri dispositivi Bluetooth MTP da enumerare.</span><span class="sxs-lookup"><span data-stu-id="dbae0-126">There are no more MTP Bluetooth devices to enumerate.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="dbae0-127">Esempio</span><span class="sxs-lookup"><span data-stu-id="dbae0-127">Examples</span></span>

<span data-ttu-id="dbae0-128">Nell'esempio seguente viene illustrato l'utilizzo di questo metodo per enumerare i dispositivi MTP/Bluetooth abbinati e per inviare una richiesta di connessione asincrona a ognuno di essi.</span><span class="sxs-lookup"><span data-stu-id="dbae0-128">The following example demonstrates the use of this method to enumerate paired MTP/Bluetooth devices, and to send an asynchronous connection request to each.</span></span>


```C++
IEnumPortableDeviceConnectors* pEnum = NULL;
    HRESULT hrEnum = S_OK;
 HRESULT hr = CoCreateInstance(CLSID_EnumBthMtpConnectors, NULL, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pEnum));
    if (SUCCEEDED(hr))
{
  while (S_OK == hrEnum)
    {
       UINT32  uFetched        = 0;
       LPWSTR  wszDevicePnPID  = NULL;
       IPortableDeviceConnector* pDevice = NULL;
       hrEnum = pEnum->Next(1, &spDevice, &uFetched);
       if (hrEnum == S_OK && uFetched == 1)
        {
          // Send an asynchronous connect request.  
          hr = pDevice ->Connect(NULL);
          // Release the device when done
          pDevice->Release();
          pDevice = NULL;
        }
     }  // while S_OK == hrEnum
  // Release the enumerator when done
    if (pEnum)
    {
     pEnum->Release();
     pEnum = NULL;
   }
    }
       
```



## <a name="requirements"></a><span data-ttu-id="dbae0-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dbae0-129">Requirements</span></span>



| <span data-ttu-id="dbae0-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbae0-130">Requirement</span></span> | <span data-ttu-id="dbae0-131">Valore</span><span class="sxs-lookup"><span data-stu-id="dbae0-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbae0-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dbae0-132">Minimum supported client</span></span><br/> | <span data-ttu-id="dbae0-133">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="dbae0-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                             |
| <span data-ttu-id="dbae0-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dbae0-134">Minimum supported server</span></span><br/> | <span data-ttu-id="dbae0-135">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="dbae0-135">None supported</span></span><br/>                                                                                                                                              |
| <span data-ttu-id="dbae0-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dbae0-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="dbae0-137"><dt>Devpkey. h; </dt> <dt>PortableDeviceConnectApi. h</dt></span><span class="sxs-lookup"><span data-stu-id="dbae0-137"><dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt></span></span> </dl> |
| <span data-ttu-id="dbae0-138">IDL</span><span class="sxs-lookup"><span data-stu-id="dbae0-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dbae0-139"><dt>PortableDeviceConnectApi. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dbae0-139"><dt>Portabledeviceconnectapi.idl</dt></span></span> </dl>                                                                |
| <span data-ttu-id="dbae0-140">Libreria</span><span class="sxs-lookup"><span data-stu-id="dbae0-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="dbae0-141"><dt>PortableDeviceGuids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dbae0-141"><dt>PortableDeviceGuids.lib</dt></span></span> </dl>                                                                     |



## <a name="see-also"></a><span data-ttu-id="dbae0-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dbae0-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbae0-143">**IEnumPortableDeviceConnectors**</span><span class="sxs-lookup"><span data-stu-id="dbae0-143">**IEnumPortableDeviceConnectors**</span></span>](ienumportabledeviceconnectors.md)
</dt> </dl>

 

 




