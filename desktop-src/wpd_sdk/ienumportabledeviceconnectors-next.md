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
# <a name="ienumportabledeviceconnectorsnext-method"></a>IEnumPortableDeviceConnectors:: Next (metodo)

Il metodo **successivo** recupera i successivi uno o più oggetti [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) nella sequenza di enumerazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Next(
  [in]      UINT32                   cRequested,
  [out]     IPortableDeviceConnector **pConnectors,
  [in, out] UINT32                   *pcFetched
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*cRequested* \[ in\]
</dt> <dd>

Numero di dispositivi richiesti. Questo valore indica anche il numero di elementi nella matrice allocata dal chiamante specificata dal parametro *pConnectors* .

</dd> <dt>

*pConnectors* \[ out\]
</dt> <dd>

Matrice di puntatori [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) , ognuno dei quali specifica un dispositivo Bluetooth MTP abbinato. Il chiamante deve allocare una matrice di puntatori **IPortableDeviceConnector** , con la lunghezza della matrice specificata dal parametro *cRequested* . In esito positivo, il chiamante deve liberare sia la matrice che i puntatori restituiti. Le interfacce **IPortableDeviceConnector** vengono liberate chiamando il metodo **IUnknown:: Release** .

</dd> <dt>

*pcFetched* \[ in uscita\]
</dt> <dd>

Numero di interfacce [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) effettivamente recuperate. Se non vengono recuperate interfacce **IPortableDeviceConnector** e il valore restituito è **S \_ false**, non sono disponibili altre interfacce **IPortableDeviceConnector** da enumerare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                             | Descrizione                                                      |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>    | Il metodo è riuscito.<br/>                                 |
| <dl> <dt>**S \_ false**</dt> </dl> | Non sono disponibili altri dispositivi Bluetooth MTP da enumerare.<br/> |



 

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato l'utilizzo di questo metodo per enumerare i dispositivi MTP/Bluetooth abbinati e per inviare una richiesta di connessione asincrona a ognuno di essi.


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



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                                                                                             |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                                                                              |
| Intestazione<br/>                   | <dl> <dt>Devpkey. h; </dt> <dt>PortableDeviceConnectApi. h</dt> </dl> |
| IDL<br/>                      | <dl> <dt>PortableDeviceConnectApi. idl</dt> </dl>                                                                |
| Libreria<br/>                  | <dl> <dt>PortableDeviceGuids. lib</dt> </dl>                                                                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IEnumPortableDeviceConnectors**](ienumportabledeviceconnectors.md)
</dt> </dl>

 

 




