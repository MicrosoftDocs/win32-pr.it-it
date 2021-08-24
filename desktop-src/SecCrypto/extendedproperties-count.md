---
description: Recupera il numero di oggetti ExtendedProperty nella raccolta.
ms.assetid: 50bc8485-7285-4704-80db-c2e0d68e8cb0
title: ExtendedProperties.Count - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c34aa63da5276c573d5c3f260d5d7a5956045813695991756ede6c9f69be29ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119007269"
---
# <a name="extendedpropertiescount-property"></a>ExtendedProperties.Count - proprietà

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece Platform Invocation Services (PInvoke) per chiamare la funzione API Win32 [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) e ottenere le proprietà. Per informazioni su PInvoke, vedere [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx). Possono essere utili anche .NET e [CryptoAPI tramite P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) parte 1 e .NET e [CryptoAPI tramite P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) parte 2 delle sottosezioni dell'estensione della crittografia .NET con CAPICOM e [P/Invoke.](/previous-versions/ms867087(v=msdn.10))\]

La **proprietà Count** recupera il numero di oggetti [**ExtendedProperty**](extendedproperty.md) nella raccolta.

## <a name="syntax"></a>Sintassi


```VB
ExtendedProperties.Count As Long
```



## <a name="property-value"></a>Valore proprietà

Numero di [**oggetti ExtendedProperty**](extendedproperty.md) nella raccolta.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
