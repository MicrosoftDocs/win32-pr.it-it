---
description: Rimuove un singolo oggetto certificato dalla raccolta.
ms.assetid: dff82825-1a7d-4c1a-94e2-7f9d1281ecf2
title: 'Metodo ICertificates2:: Remove'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Remove
- ICertificates2.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6a2f9336a420f1d014e178f67cae02cf85f0fd44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331906"
---
# <a name="icertificates2remove-method"></a>Metodo ICertificates2:: Remove

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe X509Certificate2Collection**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Il metodo **Remove** rimuove un singolo oggetto [**Certificate**](certificate.md) dalla raccolta. Questo metodo è stato introdotto in capicol 2,0.

## <a name="syntax"></a>Sintassi


```VB
Certificates.Remove( _
  ByVal Index _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Indice* \[ di in\]
</dt> <dd>

Valore di indice per l'oggetto [**certificato**](certificate.md) da rimuovere. Questo parametro può essere uno dei seguenti tipi possibili.



| Type                                                                                                                                                                                                                                                              | Significato                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Long"></span><span id="long"></span><span id="LONG"></span><dl> * * * * <dt>Long * *</dt> * *<dt></dt> </dl>                                                | L'oggetto [**certificato**](certificate.md) in corrispondenza dell'indice specificato nella raccolta viene rimosso.<br/>                                                                                                          |
| <span id="String"></span><span id="string"></span><span id="STRING"></span><dl> * * * * <dt>Stringa * *</dt> * *<dt></dt> </dl>                                        | Il primo oggetto [**certificato**](certificate.md) della raccolta che corrisponde all'identificazione personale [*SHA-1*](../secgloss/s-gly.md) contenuto nella stringa specificata viene rimosso.<br/> |
| <span id="Certificate"></span><span id="certificate"></span><span id="CERTIFICATE"></span><dl> <dt>**[**Certificato**](certificate.md)**</dt> di <dt></dt> </dl> | Il primo oggetto [**certificato**](certificate.md) della raccolta che corrisponde all'oggetto **certificato** specificato viene rimosso.<br/>                                                                           |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
