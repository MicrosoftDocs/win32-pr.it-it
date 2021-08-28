---
description: Restituisce un oggetto BasicConstraints che rappresenta l'estensione dei vincoli di base del certificato.
ms.assetid: cc4e566a-5f68-4e28-9397-39f22a71e45b
title: Metodo ICertificate2::BasicConstraints
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.BasicConstraints
- ICertificate2.BasicConstraints
- ICertificate.BasicConstraints
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 8958a942a8c56dfe39c8a96bcf3f80cefcb7978feac186a80432cbe8f03b5c4b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127151"
---
# <a name="icertificate2basicconstraints-method"></a>Metodo ICertificate2::BasicConstraints

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe X509Certificate2**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) nello spazio dei nomi [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Il **metodo BasicConstraints** restituisce un [**oggetto BasicConstraints**](basicconstraints.md) che rappresenta l'estensione dei vincoli di base del certificato.

## <a name="syntax"></a>Sintassi


```VB
Certificate.BasicConstraints()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Oggetto [**BasicConstraints**](basicconstraints.md) che rappresenta l'estensione dei vincoli di base del certificato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
