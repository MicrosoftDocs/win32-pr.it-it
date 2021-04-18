---
description: Restituisce un valore booleano che indica se la chiave privata è nell'archivio rimovibile.
ms.assetid: 9371d7cf-65b2-4c0f-a387-195a058d6a8b
title: Metodo PrivateKey. rimovibile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.IsRemovable
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6684d40302746a736701b824685a54faeff5354a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330604"
---
# <a name="privatekeyisremovable-method"></a>Metodo PrivateKey. rimovibile

\[Il metodo **rimovibile** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece la [**Proprietà X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Il metodo **rimovibile** restituisce un valore booleano che indica se la chiave privata è in archivi rimovibili.

## <a name="syntax"></a>Sintassi


```VB
PrivateKey.IsRemovable()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Se true, la chiave privata si trova in una risorsa di archiviazione rimovibile.

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

 

 
