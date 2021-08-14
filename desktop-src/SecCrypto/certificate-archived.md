---
description: Imposta o recupera un valore booleano che indica se il certificato è archiviato.
ms.assetid: a6526b0e-e76b-4f03-a6ba-9e380e362364
title: Certificate.Archived - proprietà
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
ms.openlocfilehash: d2e3ab848caa24cb77a8cb45e992eeac7365af0de743fa148b07b484239fa658
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771950"
---
# <a name="certificatearchived-property"></a>Certificate.Archived - proprietà

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe X509Certificate2**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) nello spazio dei [**nomi System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

La **proprietà Archived** imposta o recupera un valore booleano che indica se il certificato è archiviato.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
Certificate.Archived As Boolean
```



## <a name="property-value"></a>Valore proprietà

Valore booleano che indica se il certificato è archiviato. Se **true,** il certificato viene archiviato. Si noti che la modifica del valore **da false** **a true** consente di archiviare il certificato.

## <a name="remarks"></a>Commenti

Questa proprietà genera CAPICOM \_ E NOT ALLOWED quando viene generato uno script da \_ \_ un'applicazione basata sul Web.

> [!Note]  
> Un certificato archiviato non è visibile nell'interfaccia utente di gestione dei certificati. Inoltre, i certificati archiviati non verranno inclusi nel metodo [**Store.Open**](store-open.md) a meno che non venga specificato CAPICOM \_ STORE OPEN INCLUDE \_ \_ \_ ARCHIVED.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
