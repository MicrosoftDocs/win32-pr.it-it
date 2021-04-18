---
description: Compila una catena di verifica del certificato da un certificato finale al certificato radice attendibile e restituisce un valore booleano che indica la validità complessiva della catena.
ms.assetid: 878f09ba-d79b-4f14-b4f6-ecb54771f56f
title: 'Metodo IChain2:: Build'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Chain.Build
- IChain2.Build
- IChain.Build
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 66ad51d94fdbd361a34e25b4b76289139abb87f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323968"
---
# <a name="ichain2build-method"></a>Metodo IChain2:: Build

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Il metodo di **compilazione** compila una catena di verifica del certificato da un certificato finale al [*certificato radice*](../secgloss/r-gly.md) attendibile e restituisce un valore booleano che indica la validità complessiva della catena.

## <a name="syntax"></a>Sintassi


```VB
Chain.Build( _
  ByVal Certificate _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Certificato* \[ di in\]
</dt> <dd>

Oggetto [**certificato**](certificate.md) che rappresenta il certificato finale sul quale deve essere compilata la catena di verifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Valore booleano che indica la validità complessiva della catena. La validità complessiva si basa sui criteri di verifica della validità sul posto.

## <a name="remarks"></a>Commenti

La catena viene compilata usando la proprietà [**CertificateStatus. CheckFlag**](certificatestatus-checkflag.md) , nonché i criteri di applicazione e di certificato specificati da un oggetto [**CertificateStatus**](certificatestatus.md) . La raccolta restituita è ordinata; il primo certificato della raccolta, **Certificates. Item**(1), è il certificato finale della catena. L'ultimo certificato della raccolta, **Certificates. Item**(**Certificates. Count**), è il [*certificato radice*](../secgloss/r-gly.md) della catena. **Certificates. Item**(0) rappresenta l'intera catena.

Ogni volta che viene chiamato il metodo **chain. Build** , lo [*stato*](../secgloss/s-gly.md) dell'oggetto [**Chain**](chain.md) viene reimpostato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetti Cryptography**](cryptography-objects.md)
</dt> <dt>

[**Catena**](chain.md)
</dt> </dl>

 

 
