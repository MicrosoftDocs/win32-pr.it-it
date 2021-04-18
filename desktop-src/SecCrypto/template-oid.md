---
description: Recupera un oggetto OID che identifica l'oggetto modello.
ms.assetid: bdd9d401-e9c4-4307-9817-7dcb55c539f8
title: Proprietà Template. OID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4a8599ac999c7d6a3e3403d94ff2c6daf0eba48b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330599"
---
# <a name="templateoid-property"></a>Proprietà Template. OID

\[La proprietà **OID** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chiamando il costruttore che accetta un OID come parametro e quindi usare OID per il modello di certificato per recuperare il modello di estensione del certificato.\]

La proprietà **OID** recupera un oggetto [**OID**](oid.md) che identifica l'oggetto [**modello**](template.md) .

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
Template.OID As OID
```



## <a name="property-value"></a>Valore proprietà

Oggetto [**OID**](oid.md) che identifica l'oggetto [**modello**](template.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Modello**](template.md)
</dt> </dl>

 

 
