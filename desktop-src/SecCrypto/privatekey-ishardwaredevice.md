---
description: Restituisce un valore booleano che indica se la chiave privata è archiviata in un dispositivo hardware.
ms.assetid: 9a06f598-55cd-441b-a85f-8bec299f8245
title: Metodo PrivateKey.IsHardwareDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.IsHardwareDevice
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6a030fddd811048ee3054c3280a3299470ac3978994d0599285b4f75bedfc3cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117978268"
---
# <a name="privatekeyishardwaredevice-method"></a>Metodo PrivateKey.IsHardwareDevice

\[Il **metodo IsHardwareDevice** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Usare invece la [**proprietà X509Certificate2.PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) nello spazio dei nomi [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Il **metodo IsHardwareDevice** restituisce un valore booleano che indica se la chiave privata è archiviata in un dispositivo hardware.

## <a name="syntax"></a>Sintassi


```VB
PrivateKey.IsHardwareDevice()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Se true, la chiave privata viene archiviata in un dispositivo hardware.

## <a name="remarks"></a>Commenti

Il valore restituito di questo metodo dipende dal provider del servizio di [*crittografia*](../secgloss/c-gly.md) (CSP) usato. Questo metodo restituirà un valore attendibile se viene usato microsoft CSP. Se CSP non è microsoft CSP, il valore restituito non può essere considerato attendibile per essere accurato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PrivateKey**](privatekey.md)
</dt> </dl>

 

 
