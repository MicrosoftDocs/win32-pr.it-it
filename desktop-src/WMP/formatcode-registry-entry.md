---
title: Voce del Registro di sistema FormatCode
description: Voce del Registro di sistema FormatCode
ms.assetid: cc444eaa-6898-48ab-9573-9e7d5e25d6db
keywords:
- Windows Media Player,Voci del Registro di sistema FormatCode
- Windows Media Player,estensioni di file
- Windows Media Player,Registro di sistema
- Registro di sistema, estensioni di file
- registro, voci FormatCode
- Registro di sistema, impostazioni per Windows Media Player
- Impostazioni del Registro di sistema dell'estensione del nome file
- Voci del Registro di sistema FormatCode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbb2bed5cd9a77a9fd58b9b3bb7b57044afe78f6b1655bef420032afdf80d5e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117934703"
---
# <a name="formatcode-registry-entry"></a>Voce del Registro di sistema FormatCode

Quando Windows Media Player rileva un'estensione di file personalizzata, cerca una sottochiave del Registro di sistema corrispondente all'estensione. La sottochiave è descritta in [File Name Extension Registry Impostazioni](file-name-extension-registry-settings.md). Una delle voci del Registro di sistema che possono essere visualizzate nella sottochiave dell'estensione è **la voce FormatCode.**

La voce del Registro di sistema **FormatCode** specifica il codice di formato MTP (Media Transport Protocol) per i file con estensione personalizzata. La voce del Registro di sistema **FormatCode** ha il formato seguente.



| Nome       | Type           | valore                                                             |
|------------|----------------|-------------------------------------------------------------------|
| FormatCode | **REG \_ DWORD** | Intero positivo a 16 bit che identifica il formato del file. |



 

Quando l'utente tenta di copiare un file multimediale digitale con un'estensione di file personalizzata in un dispositivo portatile, Windows Media Player cerca nel Registro di sistema un codice di formato associato all'estensione di file personalizzata. Se Windows Media Player trova un codice di formato, usa MTP per determinare se il dispositivo supporta il formato di file personalizzato. Se il dispositivo supporta il formato, il file multimediale viene copiato nel dispositivo senza essere transcodificato.

Un dispositivo che supporta MTP può fornire Windows Media Player un set di dati DeviceInfo, che contiene, tra le altre cose, un elenco di codici di formato supportati dal dispositivo.

Se si sta sviluppando un formato di file personalizzato, è possibile richiedere un codice di formato da Microsoft. Per informazioni su come richiedere un codice di formato, vedere Microsoft Media Transport Protocol Porting Kit, disponibile in [Microsoft Windows Media Developer Center.](https://msdn.microsoft.com/windowsmedia/default.aspx)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**File Name Extension Registry Impostazioni**](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




