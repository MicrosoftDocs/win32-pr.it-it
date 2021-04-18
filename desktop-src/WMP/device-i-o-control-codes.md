---
title: Codici di controllo di I/O del dispositivo
description: Codici di controllo di I/O del dispositivo
ms.assetid: 46a5d166-ca8d-42df-9455-145332437153
keywords:
- Media Player di Windows, codici di controllo di I/O del dispositivo
- Media Player di Windows, codici di controllo
- Gestione dispositivi Windows Media
- codici di controllo di I/O del dispositivo
- codici di controllo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69c00e235ce0f0e68e98f4f0e37221eac0903682
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298570"
---
# <a name="device-io-control-codes"></a>Codici di controllo di I/O del dispositivo

Windows Media Player 10 o versioni successive definisce Windows Media Gestione dispositivi I codici di controllo di I/O del dispositivo. La tabella seguente contiene i codici di controllo e le relative descrizioni.



| Codice di controllo di I/O                      | Valore      | Descrizione                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ \_ \_ round trip dei metadati IOCTL WMP \_** | 0x31504d57 | Gestisce il trasferimento delle informazioni sulle modifiche apportate ai valori dei metadati. Vedere [estensioni del dispositivo per il trasferimento di metadati accelerati](device-extensions-for-accelerated-metadata-transfer.md).                                                                                                                                                                          |
| **il \_ dispositivo IOCTL WMP \_ \_ può \_ sincronizzare**     | 0x32504d57 | Indica se un dispositivo portatile supporta la sincronizzazione automatica. Windows Media Player 10 o versioni successive non fornisce buffer di input. Il buffer di output deve restituire un valore **DWORD** . Il valore 1 indica che il dispositivo supporta la sincronizzazione. Il valore 0 indica che il dispositivo non supporta la sincronizzazione automatica.<br/> Per ulteriori informazioni, vedere la sezione Osservazioni.<br/> |



 

## <a name="remarks"></a>Commenti

Questi codici di controllo sono definiti in wmpdevices. h.

Se il dispositivo non supporta il **dispositivo \_ IOCTL \_ WMP \_ può \_ sincronizzare**, Windows Media Player 10 o versioni successive presuppone che il dispositivo supporti la sincronizzazione automatica. Si noti che, anche se questo valore può impedire la sincronizzazione automatica, sono disponibili criteri aggiuntivi per determinare se il dispositivo supporta la sincronizzazione automatica.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Estensioni del dispositivo per il trasferimento di metadati accelerati**](device-extensions-for-accelerated-metadata-transfer.md)
</dt> <dt>

[**Windows Media Player**](windows-media-player.md)
</dt> </dl>

 

 





