---
description: Imposta o recupera l'algoritmo utilizzato per la firma, l'inviluppo e la crittografia delle operazioni. Si tratta della proprietà predefinita.
ms.assetid: e1144a9c-a352-4f73-a91c-ea66f3d61608
title: Proprietà Algorithm.Name
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Algorithm.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 35ff147d8db7fb409787fa938a951dfc0a2320e3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324598"
---
# <a name="algorithmname-property"></a>Proprietà Algorithm.Name

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista, Windows XP. Usare invece la [**classe AlgorithmIdentifier**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La proprietà **Name** imposta o recupera l'algoritmo utilizzato per la firma, l'inviluppo e la crittografia delle operazioni. Si tratta della proprietà predefinita.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
Algorithm.Name As CAPICOM_ENCRYPTION_ALGORITHM
```



## <a name="property-value"></a>Valore proprietà

Valore dell'enumerazione dell' [**\_ \_ algoritmo di crittografia CAPICOM**](capicom-encryption-algorithm.md) che specifica quale algoritmo utilizzare. Nella tabella seguente sono illustrati i possibili valori.



| Valore                                                                                                                                                                                                                       | Significato                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_RC2"></span><span id="capicom_encryption_algorithm_rc2"></span><dl> <dt>**Algoritmo di crittografia capicol \_ \_ \_ RC2**</dt> </dl>    | Usare la crittografia RC2.<br/>        |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_RC4"></span><span id="capicom_encryption_algorithm_rc4"></span><dl> <dt>**\_Algoritmo di crittografia CAPICOM \_ \_ RC4**</dt> </dl>    | Usare la crittografia RC4.<br/>        |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_DES"></span><span id="capicom_encryption_algorithm_des"></span><dl> <dt>**\_algoritmo di crittografia CAPICOM \_ \_ des**</dt> </dl>    | Usare la crittografia DES.<br/>        |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_3DES"></span><span id="capicom_encryption_algorithm_3des"></span><dl> <dt>**Algoritmo di crittografia capicol \_ \_ \_ 3DES**</dt> </dl> | Usare la crittografia Triple DES.<br/> |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_AES"></span><span id="capicom_encryption_algorithm_aes"></span><dl> <dt>**algoritmo di crittografia capicol \_ \_ \_ AES**</dt> </dl>    | Usare l'algoritmo AES.<br/>     |



 

## <a name="remarks"></a>Commenti

Quando il valore di questa proprietà viene reimpostato, direttamente o indirettamente, viene reimpostato l'intero stato dell'oggetto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
