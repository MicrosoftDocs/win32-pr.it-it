---
title: Voce del registro di sistema FormatCode
description: Voce del registro di sistema FormatCode
ms.assetid: cc444eaa-6898-48ab-9573-9e7d5e25d6db
keywords:
- Media Player di Windows, voci del registro di sistema FormatCode
- Windows Media Player, estensioni di file
- Windows Media Player, registro di sistema
- Registro di sistema, estensioni di file
- Registro di sistema, voci FormatCode
- Registro di sistema, impostazioni per Windows Media Player
- impostazioni del registro di sistema estensione del nome file
- Voci del registro di sistema FormatCode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2318d32e9d7a08a2ae23b24e7acd2674b9eecb2
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104223406"
---
# <a name="formatcode-registry-entry"></a>Voce del registro di sistema FormatCode

Quando Windows Media Player rileva un'estensione del nome di file personalizzata, Cerca una sottochiave del registro di sistema corrispondente all'estensione. La sottochiave è descritta in [impostazioni del registro di sistema estensione del nome file](file-name-extension-registry-settings.md). Una delle voci del registro di sistema che possono essere visualizzate sotto la sottochiave dell'estensione è la voce **FormatCode** .

La voce del registro di sistema **FormatCode** specifica il codice di formato MTP (Media Transport Protocol) per i file con estensione personalizzata. La voce del registro di sistema **FormatCode** ha il formato seguente.



| Nome       | Type           | valore                                                             |
|------------|----------------|-------------------------------------------------------------------|
| FormatCode | **REG \_ DWORD** | Intero positivo a 16 bit che identifica il formato del file. |



 

Quando l'utente tenta di copiare un file multimediale digitale con estensione di file personalizzata in un dispositivo portatile, Windows Media Player Cerca nel registro di sistema di trovare un codice di formato associato all'estensione del nome file personalizzata. Se Windows Media Player trova un codice di formato, USA MTP per determinare se il dispositivo supporta il formato di file personalizzato. Se il dispositivo supporta il formato, il file multimediale viene copiato nel dispositivo senza essere transcodificato.

Un dispositivo che supporta MTP può fornire Media Player Windows con un set di dati DeviceInfo, che contiene, tra le altre cose, un elenco di codici di formato supportati dal dispositivo.

Se è in corso lo sviluppo di un formato di file personalizzato, è possibile richiedere un codice di formato da Microsoft. Per informazioni su come richiedere un codice di formato, vedere Microsoft Media Transport Protocol Porting Kit, disponibile nel [centro per sviluppatori Microsoft Windows Media](https://msdn.microsoft.com/windowsmedia/default.aspx).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Impostazioni del registro di sistema estensione del nome file**](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




