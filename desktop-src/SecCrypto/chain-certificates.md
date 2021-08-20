---
description: La proprietà Certificates recupera una raccolta Certificates che rappresenta i certificati nella catena. Questa è la proprietà predefinita.
ms.assetid: c3e6953f-35e5-469a-a1aa-e3a4ebe21ac3
title: Proprietà IChain2::Certificates
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChain2.Certificates
- IChain2.get_Certificates
- IChain.Certificates
- IChain.get_Certificates
- Chain.Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 16fb08d020dcd59ed7caf22a0e93f4a4866b58642f12d0c131f3f0368bd3e7e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769652"
---
# <a name="ichain2certificates-property"></a>Proprietà IChain2::Certificates

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) nello spazio dei [**nomi System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

La **proprietà Certificates** recupera una raccolta [**Certificates**](certificates.md) che rappresenta i certificati nella catena. Questa è la proprietà predefinita.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
Chain.Certificates As Certificates
```



## <a name="property-value"></a>Valore proprietà

Raccolta [**certificates**](certificates.md) utilizzata per recuperare informazioni su ogni certificato nella catena. Il primo certificato nella raccolta restituita, **Certificates.Item**(1), è il certificato finale della catena. L'ultimo certificato nella **raccolta, Certificates.Item**(**Certificates.Count**), è il [*certificato radice*](../secgloss/r-gly.md) della catena.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
