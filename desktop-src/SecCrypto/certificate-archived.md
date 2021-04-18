---
description: Imposta o recupera un valore booleano che indica se il certificato è archiviato.
ms.assetid: a6526b0e-e76b-4f03-a6ba-9e380e362364
title: Proprietà Certificate. Archived
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Archived
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e1d8cdea3e43bbe10ee87f8f4aa605740a15e6ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333781"
---
# <a name="certificatearchived-property"></a>Proprietà Certificate. Archived

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe X509Certificate2**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La proprietà **archiviata** imposta o recupera un valore booleano che indica se il certificato è archiviato.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
Certificate.Archived As Boolean
```



## <a name="property-value"></a>Valore proprietà

Valore booleano che indica se il certificato è archiviato. Se **true**, il certificato viene archiviato. Si noti che la modifica del valore da **false** a **true** archivia il certificato.

## <a name="remarks"></a>Commenti

Questa proprietà genera CAPICOM \_ E \_ non \_ è consentita quando viene inserito nello script da un'applicazione basata sul Web.

> [!Note]  
> Un certificato archiviato non è visibile nell'interfaccia utente di gestione certificati. I certificati archiviati, inoltre, non verranno inclusi nel metodo [**Store. Open**](store-open.md) , a meno che non \_ \_ \_ \_ sia specificato Archived Store.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
