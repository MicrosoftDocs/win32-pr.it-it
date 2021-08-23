---
description: Specifica le dimensioni del blocco di byte crittografato per la crittografia basata su modelli basati su campioni.
ms.assetid: 1F370DEC-20B5-456D-BB68-C94E183410F3
title: MFSampleExtension_Encryption_CryptByteBlock attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85da01a8b69fa22604cc10df54aa474ec117256ebee0630e490e25d9888484d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119603201"
---
# <a name="mfsampleextension_encryption_cryptbyteblock-attribute"></a>Attributo \_ \_ CryptByteBlock di crittografia MFSampleExtension

Specifica le dimensioni del blocco di byte crittografato per la crittografia basata su modelli basati su campioni.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Il numero di byte non crittografati non crittografati nel blocco di mapping di sottocampionamento viene specificato nell'attributo [ \_ \_ SkipByteBlock della crittografia MFSampleExtension.](mfsampleextension-encryption-skipbyteblock.md) Se uno di questi attributi non è presente o ha un valore pari a 0, significa che i dati di esempio non sono crittografati. Entrambi questi valori devono essere diversi da zero, positivi o entrambi devono avere un valore pari a zero.

Nei casi in cui l'origine è basata su MP4, il valore viene impostato in base ai valori del blocco di byte di crittografia predefinito all'interno della casella di crittografia della traccia \_ \_ \_ ('tenc') nell'intestazione MP4. Per altre informazioni, vedere [MFSampleExtension \_ Encryption \_ ProtectionScheme.](mfsampleextension-encryption-protectionscheme.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1709 \[\]<br/>                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



 

 




