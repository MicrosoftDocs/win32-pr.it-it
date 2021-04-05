---
description: Installa l'oggetto ActiveX specificato.
ms.assetid: c5d460d8-0df4-437a-a59e-707bf868a339
title: 'Metodo IeAxiSystemInstaller:: InitializeSystemInstaller'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiSystemInstaller.InitializeSystemInstaller
api_type:
- COM
api_location: ''
ms.openlocfilehash: 874bee80e23051d5dfdd22e259395293ae532619
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884457"
---
# <a name="ieaxisysteminstallerinitializesysteminstaller-method"></a>Metodo IeAxiSystemInstaller:: InitializeSystemInstaller

Il metodo **InitializeSystemInstaller** installa l'oggetto ActiveX specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT InitializeSystemInstaller(
  [in]  BSTR     bstrUrl,
  [in]  DWORD    dwClientPID,
  [in]  IUnknown *pCallback,
  [out] BSTR     *pbstrNonce
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrURL* \[ in\]
</dt> <dd>

URL dell'oggetto ActiveX da installare.

</dd> <dt>

*dwClientPID* \[ in\]
</dt> <dd>

ID processo del processo chiamante.

</dd> <dt>

*pCallback* \[ in\]
</dt> <dd>

Puntatore a un'istanza dell'interfaccia [**IeAxiServiceCallback**](ieaxiservicecallback.md) che verifica se l'oggetto ActiveX può essere installato.

</dd> <dt>

*pbstrNonce* \[ out\]
</dt> <dd>

Contesto che può essere utilizzato per condividere le informazioni sullo stato nelle chiamate ad altri metodi utilizzati per verificare e scaricare l'oggetto ActiveX.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il metodo restituisce S \_ OK.

Se il metodo ha esito negativo, restituisce un valore **HRESULT** che indica l'errore. Per un elenco di codici di errore comuni, vedere [valori HRESULT comuni](/windows/desktop/SecCrypto/common-hresult-values).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[ desktop apps\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                 |
| IID<br/>                      | IID \_ IeAxiSystemInstaller è definito come a50ea6f8-4764-4299-B309-022b2a8b4d8d<br/>                   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IeAxiSystemInstaller**](ieaxisysteminstaller.md)
</dt> </dl>

 

