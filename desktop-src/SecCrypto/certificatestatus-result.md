---
description: La proprietà Result recupera un valore che indica se il certificato è valido. Si tratta della proprietà predefinita.
ms.assetid: b1edfbde-9d54-4e9c-ba9b-33e4c354c23f
title: Proprietà CertificateStatus. Result
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.Result
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: df13e9a9fb0454d30ce855b3d272fa521e96e0f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324139"
---
# <a name="certificatestatusresult-property"></a>Proprietà CertificateStatus. Result

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**struttura X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La proprietà **result** recupera un valore che indica se il certificato è valido. Si tratta della proprietà predefinita.

## <a name="syntax"></a>Sintassi


```VB
CertificateStatus.Result As Boolean
```



## <a name="property-value"></a>Valore proprietà

Se **true**, il certificato è valido. La validità del certificato viene controllata usando l'impostazione corrente della proprietà [**CheckFlag**](certificatestatus-checkflag.md) e le diverse impostazioni dei criteri.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
