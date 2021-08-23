---
description: La proprietà Item recupera un oggetto ExtendedProperty dalla raccolta. Si tratta della proprietà predefinita.
ms.assetid: add819e1-6330-483a-8a76-3b7fb8d3f110
title: ExtendedProperties.Item - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 088756fe1e4bb3d5b019c141740917185c117416e8f30b871586b7197c62aa1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119007259"
---
# <a name="extendedpropertiesitem-property"></a>ExtendedProperties.Item - proprietà

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece Platform Invocation Services (PInvoke) per chiamare la funzione api Win32 [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) e ottenere le proprietà. Per informazioni su PInvoke, vedere [Esercitazione su Platform Invoke.](https://msdn.microsoft.com/library/aa288468.aspx) Possono essere utili anche .NET e [CryptoAPI tramite P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) parte 1 e .NET e [CryptoAPI tramite P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) parte 2 delle sottosezioni estensione della crittografia .NET con CAPICOM e [P/Invoke.](/previous-versions/ms867087(v=msdn.10))\]

La **proprietà Item** recupera un oggetto [**ExtendedProperty**](extendedproperty.md) dalla raccolta. Si tratta della proprietà predefinita.

## <a name="syntax"></a>Sintassi


```VB
ExtendedProperties.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a>Valore proprietà

Oggetto [**ExtendedProperty**](extendedproperty.md) che rappresenta la proprietà estesa indicizzata della raccolta.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
