---
description: Recupera un oggetto OID che identifica l'oggetto Template.
ms.assetid: bdd9d401-e9c4-4307-9817-7dcb55c539f8
title: Template.OID - proprietà
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
ms.openlocfilehash: ecfc56210d5fa81f6e7623b2c471cf0df1b5f091f7dab6c797b56f6af8d2496e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118897386"
---
# <a name="templateoid-property"></a>Template.OID - proprietà

\[La **proprietà OID** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Usare invece la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) nello spazio dei nomi [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chiamando il costruttore che accetta un OID come parametro e quindi usare l'OID per il modello di certificato per recuperare il modello di estensione del certificato.\]

La **proprietà OID** recupera un [**oggetto OID**](oid.md) che identifica l'oggetto Template. [](template.md)

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
Template.OID As OID
```



## <a name="property-value"></a>Valore proprietà

Oggetto [**OID**](oid.md) che identifica [**l'oggetto**](template.md) Template.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Modello**](template.md)
</dt> </dl>

 

 
