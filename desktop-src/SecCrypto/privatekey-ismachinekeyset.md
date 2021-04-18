---
description: Restituisce un valore booleano che indica se la chiave privata appartiene a un set di chiavi del computer.
ms.assetid: ea13ba68-30ae-4aa4-b490-29fd4542c621
title: PrivateKey. IsMachineKeyset, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.IsMachineKeyset
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2a42e3f932b8294d9671b7901437151d9fbbe5a8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333776"
---
# <a name="privatekeyismachinekeyset-method"></a>PrivateKey. IsMachineKeyset, metodo

\[Il metodo **IsMachineKeyset** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece la [**Proprietà X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Il metodo **IsMachineKeyset** restituisce un valore booleano che indica se la chiave privata appartiene a un set di chiavi del computer.

## <a name="syntax"></a>Sintassi


```VB
PrivateKey.IsMachineKeyset()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Se true, la chiave privata appartiene a un set di chiavi del computer.

## <a name="remarks"></a>Commenti

Il valore restituito di questo metodo dipende dal provider del [*servizio di crittografia*](../secgloss/c-gly.md) (CSP) utilizzato. Questo metodo restituirà un valore attendibile se viene utilizzato un CSP Microsoft. Se CSP non è un CSP Microsoft, il valore restituito non può essere considerato accurato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PrivateKey**](privatekey.md)
</dt> </dl>

 

 
