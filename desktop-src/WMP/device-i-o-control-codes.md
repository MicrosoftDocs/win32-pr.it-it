---
title: Codici di controllo di I/O del dispositivo
description: Codici di controllo di I/O del dispositivo
ms.assetid: 46a5d166-ca8d-42df-9455-145332437153
keywords:
- Windows Media Player, codici di controllo I/O del dispositivo
- Windows Media Player,codici di controllo
- Windows Gestione dispositivi multimediali
- codici di controllo di I/O del dispositivo
- codici di controllo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63d610b396125cf190764b53106ca6535a214e2c8166f4e69de884c113fd77ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117935850"
---
# <a name="device-io-control-codes"></a>Codici di controllo di I/O del dispositivo

Windows Media Player 10 o versioni successive definisce Windows di controllo I/O del dispositivo di Gestione dispositivi multimediali. La tabella seguente contiene i codici di controllo e le relative descrizioni.



| Codice di controllo I/O                      | Valore      | Descrizione                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ROUND TRIP DEI \_ METADATI WMP IOCTL \_ \_ \_** | 0x31504d57 | Gestisce il trasferimento di informazioni sulle modifiche apportate ai valori dei metadati. Vedere [Estensioni del dispositivo per il trasferimento accelerato dei metadati.](device-extensions-for-accelerated-metadata-transfer.md)                                                                                                                                                                          |
| **IL DISPOSITIVO IOCTL \_ WMP \_ PUÒ ESEGUIRE LA \_ \_ SINCRONIZZAZIONE**     | 0x32504d57 | Indica se un dispositivo portatile supporta la sincronizzazione automatica. Windows Media Player 10 o versione successiva non fornisce alcun buffer di input. Il buffer di output deve restituire un **valore DWORD.** Il valore 1 indica che il dispositivo supporta la sincronizzazione. Il valore 0 indica che il dispositivo non supporta la sincronizzazione automatica.<br/> Per ulteriori informazioni, vedere la sezione Osservazioni.<br/> |



 

## <a name="remarks"></a>Commenti

Questi codici di controllo sono definiti in wmpdevices.h.

Se il dispositivo non supporta **IOCTL \_ WMP \_ DEVICE CAN \_ \_ SYNC,** Windows Media Player 10 o versione successiva presuppone che il dispositivo supporti la sincronizzazione automatica. Si noti che anche se questo valore può non consentire la sincronizzazione automatica, esistono criteri aggiuntivi usati per determinare se il dispositivo supporta la sincronizzazione automatica.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Estensioni del dispositivo per il trasferimento accelerato dei metadati**](device-extensions-for-accelerated-metadata-transfer.md)
</dt> <dt>

[**Windows Media Player**](windows-media-player.md)
</dt> </dl>

 

 





