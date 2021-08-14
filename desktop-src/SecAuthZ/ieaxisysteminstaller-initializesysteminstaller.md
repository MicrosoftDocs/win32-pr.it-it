---
description: Installa l'oggetto ActiveX specificato.
ms.assetid: c5d460d8-0df4-437a-a59e-707bf868a339
title: Metodo IeAxiSystemInstaller::InitializeSystemInstaller
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
ms.openlocfilehash: 9619557395ede0510e04378a03f2ded32fa7a9c829c8c6f40acdaf58b8e0fda2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119414651"
---
# <a name="ieaxisysteminstallerinitializesysteminstaller-method"></a>Metodo IeAxiSystemInstaller::InitializeSystemInstaller

Il **metodo InitializeSystemInstaller** installa l'oggetto ActiveX specificato.

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

*bstrUrl* \[ Pollici\]
</dt> <dd>

URL dell'oggetto ActiveX da installare.

</dd> <dt>

*dwClientPID* \[ Pollici\]
</dt> <dd>

ID del processo chiamante.

</dd> <dt>

*pCallback* \[ Pollici\]
</dt> <dd>

Puntatore a un'istanza [**dell'interfaccia IeAxiServiceCallback**](ieaxiservicecallback.md) che verifica se l'oggetto ActiveX può essere installato.

</dd> <dt>

*pbstrNonce* \[ Cambio\]
</dt> <dd>

Contesto che può essere usato per condividere le informazioni sullo stato nelle chiamate ad altri metodi usati per verificare e scaricare l ActiveX o object.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il metodo restituisce S \_ OK.

Se il metodo ha esito negativo, restituisce un **valore HRESULT** che indica l'errore. Per un elenco dei codici di errore comuni, vedere [Valori HRESULT comuni](/windows/desktop/SecCrypto/common-hresult-values).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista Business, Windows Vista Enterprise, Windows solo app desktop di Vista Ultimate \[\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                 |
| IID<br/>                      | \_IeAxiSystemInstaller IID è definito come a50ea6f8-4764-4299-b309-022b2a8b4d8d<br/>                   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IeAxiSystemInstaller**](ieaxisysteminstaller.md)
</dt> </dl>

 

