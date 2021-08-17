---
description: Compila una catena di verifica del certificato da un certificato finale al certificato radice attendibile e restituisce un valore booleano che indica la validità complessiva della catena.
ms.assetid: 878f09ba-d79b-4f14-b4f6-ecb54771f56f
title: Metodo IChain2::Build
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
ms.openlocfilehash: 5001fe6855a02ad487b16b56d01eb83d28c25c8ef5ba52e6249c9de1bd2fc8a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769750"
---
# <a name="ichain2build-method"></a>Metodo IChain2::Build

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) nello spazio dei nomi [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Il **metodo Build** compila una catena di verifica [](../secgloss/r-gly.md) del certificato da un certificato finale al certificato radice attendibile e restituisce un valore booleano che indica la validità complessiva della catena.

## <a name="syntax"></a>Sintassi


```VB
Chain.Build( _
  ByVal Certificate _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Certificato* \[ Pollici\]
</dt> <dd>

Oggetto [**Certificate**](certificate.md) che rappresenta il certificato finale su cui deve essere compilata la catena di verifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Valore booleano che indica la validità complessiva della catena. La validità complessiva si basa sui criteri di controllo di validità in atto.

## <a name="remarks"></a>Commenti

La catena viene compilata usando la [**proprietà CertificateStatus.CheckFlag,**](certificatestatus-checkflag.md) nonché i criteri di applicazione e certificato specificati da [**un oggetto CertificateStatus.**](certificatestatus.md) La raccolta restituita è ordinata. il primo certificato nella **raccolta, Certificates.Item**(1), è il certificato finale della catena. L'ultimo certificato nella **raccolta, Certificates.Item**(**Certificates.Count**), è il [*certificato radice*](../secgloss/r-gly.md) della catena. **Certificates.Item**(0) rappresenta l'intera catena.

Ogni volta che viene chiamato il **metodo Chain.Build,** lo [*stato*](../secgloss/s-gly.md) dell'oggetto [**Chain**](chain.md) viene reimpostato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetti di crittografia**](cryptography-objects.md)
</dt> <dt>

[**Catena**](chain.md)
</dt> </dl>

 

 
