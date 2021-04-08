---
description: Specifica la dimensione del blocco di byte cancellata (non crittografata) per la crittografia dei modelli basata sul campione.
ms.assetid: F65112FA-B380-45F8-A1FC-3408FE6E49E2
title: Attributo MFSampleExtension_Encryption_SkipByteBlock (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18003c03df7e65314846d34cb1d1093f5b2507a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880614"
---
# <a name="mfsampleextension_encryption_skipbyteblock-attribute"></a>\_Attributo SkipByteBlock di crittografia MFSampleExtension \_

Specifica la dimensione del blocco di byte cancellata (non crittografata) per la crittografia dei modelli basata sul campione.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Il numero di byte crittografati nel blocco di mapping di sottocampionamento viene specificato nell'attributo [ \_ \_ CryptByteBlock Encryption MFSampleExtension](mfsampleextension-encryption-cryptbyteblock.md) . Se uno di questi attributi non è presente o ha un valore pari a 0, significa che i dati di esempio non sono crittografati. Uno di questi valori deve essere diverso da zero, valori positivi oppure entrambi devono avere un valore pari a zero.

Nei casi in cui l'origine è basata su MP4, il valore viene impostato in base ai valori del \_ blocco default Skip \_ byte nella \_ casella Track Encryption ("Tenc") nell'intestazione MP4. Per altre informazioni, vedere [MFSampleExtension \_ Encryption \_ ProtectionScheme](mfsampleextension-encryption-protectionscheme.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1709 \[\]<br/>                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



 

 




