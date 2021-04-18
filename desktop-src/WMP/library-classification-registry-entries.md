---
title: Voci del registro di sistema di classificazione delle librerie
description: Voci del registro di sistema di classificazione delle librerie
ms.assetid: 3ef7d384-503f-4b8f-9f4b-e0ef3c56616b
keywords:
- Windows Media Player, libreria
- Media Player di Windows, voci del registro di sistema di classificazione
- Windows Media Player, estensioni di file
- Windows Media Player, registro di sistema
- Registro di sistema, estensioni di file
- Registro di sistema, voci di classificazione delle librerie
- Registro di sistema, impostazioni per Windows Media Player
- impostazioni del registro di sistema estensione del nome file
- raccolta, voci del registro di sistema di classificazione
- libreria, registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e48ea1aacdd1e4c553a7e83bfdd711ff331c0878
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298557"
---
# <a name="library-classification-registry-entries"></a>Voci del registro di sistema di classificazione delle librerie

Quando Windows Media Player rileva un file multimediale con un'estensione di file personalizzata, non sa se il file deve essere classificato come audio, video o un altro tipo. Per impostazione predefinita, Windows Media Player inserisce tali file nell'altra parte relativa ai supporti della libreria.

Se i file multimediali digitali hanno un formato personalizzato, è possibile specificare Windows Media Player con le informazioni sulla posizione in cui i file devono essere visualizzati nella libreria del lettore inserendo due voci nel registro di sistema nel computer dell'utente.

Una voce viene inserita nella sottochiave seguente.

**HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ MediaPlayer \\ MLS \\ Extensions**

La voce del registro di sistema ha il formato seguente.



| Nome                                                  | Tipo di dati   | Valore                                      |
|-------------------------------------------------------|-------------|--------------------------------------------|
| Estensione del nome file senza il separatore punto (.) | **REG \_ SZ** | Stringa che specifica un percorso di libreria |



 

L'altra voce del registro di sistema passa alla sottochiave seguente che è stata creata.

**HKEY \_ CustomExtension \_ radice \\ classi** 

dove *customExtension* è l'estensione del nome di file, incluso il separatore del punto (.).

La voce del registro di sistema ha il formato seguente.



| Nome          | Tipo di dati   | Valore                                      |
|---------------|-------------|--------------------------------------------|
| PerceivedType | **REG \_ SZ** | Stringa che specifica un percorso di libreria |



 

Entrambe le voci del registro di sistema devono avere lo stesso valore. Nella tabella seguente sono riportati i valori possibili.



| Valore | Descrizione                                                                      |
|-------|----------------------------------------------------------------------------------|
| Audio | I file con estensione personalizzata vengono visualizzati nella parte musicale della libreria. |
| Video | I file con estensione personalizzata vengono visualizzati nella parte video della libreria. |



 

Ad esempio, le voci del registro di sistema seguenti specificano che i file con estensione xyz verranno visualizzati nella parte musicale della libreria:


```C++

HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\MLS\Extensions
    xyz     REG_SZ     audio

HKEY_CLASSES_ROOT\.xyz
    PerceivedType     REG_SZ     audio

```



Si noti che il codice che tenta di scrivere nel registro di sistema nel computer dell'utente può scrivere nel \_ sottoalbero del computer locale HKEY \_ solo se l'utente corrente dispone di privilegi amministrativi.

Le voci del registro di sistema di classificazione delle librerie sono supportate dalle seguenti versioni di Windows Media Player.

-   Windows Media Player 9 serie con hotfix 823275
-   Windows Media Player 10 e versioni successive

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Impostazioni del registro di sistema estensione del nome file**](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




