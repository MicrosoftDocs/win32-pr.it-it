---
description: Imposta o recupera il contenuto di testo non crittografato di un messaggio da inviare in busta. Si tratta della proprietà predefinita.
ms.assetid: 7927321f-fbda-45e0-9b9f-c10ecd3a98b1
title: EnvelopedData.Content - proprietà
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
ms.openlocfilehash: 4115b55b7f9542c5a31c9abd3bcbbaec5256be4283675becac2f011ec76c8cbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117766072"
---
# <a name="envelopeddatacontent-property"></a>EnvelopedData.Content - proprietà

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe EnvelopedCms**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System.Security.Cryptography.Pkcs.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

La **proprietà Content** imposta o recupera il contenuto in testo non crittografato di un messaggio da inviare in busta. Si tratta della proprietà predefinita.

## <a name="syntax"></a>Sintassi


```VB
EnvelopedData.Content As String
```



## <a name="property-value"></a>Valore proprietà

Contenuto di testo non crittografato di un messaggio da inviare in busta.

## <a name="remarks"></a>Commenti

L'impostazione di questa proprietà deve essere eseguita prima [**della chiamata del**](envelopeddata-encrypt.md) metodo Encrypt. Quando il valore di questa proprietà viene reimpostato, [](../secgloss/s-gly.md) direttamente o indirettamente, l'intero stato dell'oggetto viene reimpostato e qualsiasi contenuto crittografato nell'oggetto viene perso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EnvelopedData**](envelopeddata.md)
</dt> </dl>

 

 
