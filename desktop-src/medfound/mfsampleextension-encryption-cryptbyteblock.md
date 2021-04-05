---
description: Specifica la dimensione del blocco di byte crittografato per la crittografia del modello basata su campione.
ms.assetid: 1F370DEC-20B5-456D-BB68-C94E183410F3
title: Attributo MFSampleExtension_Encryption_CryptByteBlock (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 927e08d81cc8066f73b579c8abf419d754fc1713
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049802"
---
# <a name="mfsampleextension_encryption_cryptbyteblock-attribute"></a>\_Attributo CryptByteBlock di crittografia MFSampleExtension \_

Specifica la dimensione del blocco di byte crittografato per la crittografia del modello basata su campione.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Il numero di byte cancellati (non crittografati) nel blocco di mapping di sottocampionamento viene specificato nell'attributo [ \_ \_ SkipByteBlock Encryption MFSampleExtension](mfsampleextension-encryption-skipbyteblock.md) . Se uno di questi attributi non è presente o ha un valore pari a 0, significa che i dati di esempio non sono crittografati. Uno di questi valori deve essere diverso da zero, valori positivi oppure entrambi devono avere un valore pari a zero.

Nei casi in cui l'origine è basata su MP4, il valore viene impostato in base ai valori del \_ blocco default Crypt \_ byte nella \_ casella Track Encryption (' Tenc ') nell'intestazione MP4. Per altre informazioni, vedere [MFSampleExtension \_ Encryption \_ ProtectionScheme](mfsampleextension-encryption-protectionscheme.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1709 \[\]<br/>                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



 

 




