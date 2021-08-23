---
description: Specifica le dimensioni del blocco di byte non crittografate per la crittografia basata su modelli basati su campioni.
ms.assetid: F65112FA-B380-45F8-A1FC-3408FE6E49E2
title: MFSampleExtension_Encryption_SkipByteBlock attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c674a7f7762f97a1978bd827795733d01b1dea3053898c5ecd30308373449b17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119603131"
---
# <a name="mfsampleextension_encryption_skipbyteblock-attribute"></a>Attributo \_ SkipByteBlock della crittografia MFSampleExtension \_

Specifica le dimensioni del blocco di byte non crittografate per la crittografia basata su modelli basati su campioni.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Il numero di byte crittografati nel blocco di mapping subsample viene specificato nell'attributo [MFSampleExtension \_ Encryption \_ CryptByteBlock.](mfsampleextension-encryption-cryptbyteblock.md) Se uno di questi attributi non è presente o ha un valore pari a 0, significa che i dati di esempio non sono crittografati. Entrambi questi valori devono essere diversi da zero, positivi o entrambi devono avere un valore pari a zero.

Nei casi in cui l'origine è basata su MP4, il valore viene impostato in base ai valori del blocco di byte skip predefinito all'interno della casella di crittografia della traccia \_ \_ \_ ('tenc') nell'intestazione MP4. Per altre informazioni, vedere [MFSampleExtension \_ Encryption \_ ProtectionScheme.](mfsampleextension-encryption-protectionscheme.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1709 \[\]<br/>                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



 

 




