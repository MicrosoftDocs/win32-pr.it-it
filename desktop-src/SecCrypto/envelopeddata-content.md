---
description: Imposta o Recupera il contenuto di testo non crittografato di un messaggio da racchiudere. Si tratta della proprietà predefinita.
ms.assetid: 7927321f-fbda-45e0-9b9f-c10ecd3a98b1
title: Proprietà EnvelopedData. Content
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData.Content
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ce87dba503d8e8eec2dc21a9024c1071b3255f3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327898"
---
# <a name="envelopeddatacontent-property"></a>Proprietà EnvelopedData. Content

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe EnvelopedCms**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La proprietà **Content** imposta o Recupera il contenuto di testo non crittografato di un messaggio da racchiudere. Si tratta della proprietà predefinita.

## <a name="syntax"></a>Sintassi


```VB
EnvelopedData.Content As String
```



## <a name="property-value"></a>Valore proprietà

Contenuto di testo non crittografato di un messaggio da racchiudere.

## <a name="remarks"></a>Commenti

L'impostazione di questa proprietà deve essere eseguita prima che venga chiamato il metodo [**Encrypt**](envelopeddata-encrypt.md) . Quando il valore di questa proprietà viene reimpostato, direttamente o indirettamente, viene reimpostato l'intero [*stato*](../secgloss/s-gly.md) dell'oggetto e qualsiasi contenuto crittografato nell'oggetto viene perso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EnvelopedData**](envelopeddata.md)
</dt> </dl>

 

 
