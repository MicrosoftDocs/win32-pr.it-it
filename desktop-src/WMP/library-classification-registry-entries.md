---
title: Voci del Registro di sistema di classificazione delle librerie
description: Voci del Registro di sistema di classificazione delle librerie
ms.assetid: 3ef7d384-503f-4b8f-9f4b-e0ef3c56616b
keywords:
- Windows Media Player,library
- Windows Media Player,classificazione delle voci del Registro di sistema
- Windows Media Player,estensioni di file
- Windows Media Player,registro
- registro, estensioni di file
- registro, voci di classificazione delle librerie
- registro, impostazioni per Windows Media Player
- Impostazioni del Registro di sistema dell'estensione di file
- library, voci del Registro di sistema di classificazione
- libreria, registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51cb263732dc8071d603c5acd62db25fc8ee887c35b28d109d961a63aba80d6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118575131"
---
# <a name="library-classification-registry-entries"></a>Voci del Registro di sistema di classificazione delle librerie

Quando Windows Media Player rileva un file multimediale con un'estensione di file personalizzata, non sa se il file deve essere classificato come audio, video o altro tipo. Per impostazione predefinita, Windows Media Player inserisce tali file nella parte Altri supporti della libreria.

Se i file multimediali digitali hanno un formato personalizzato, è possibile fornire Windows Media Player con informazioni sulla posizione in cui devono essere visualizzati i file nella libreria del lettore inserendo due voci nel Registro di sistema nel computer dell'utente.

Una voce viene riportata nella sottochiave seguente.

**HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ MediaPlayer \\ MLS \\ Extensions**

Il formato della voce del Registro di sistema è il seguente.



| Nome                                                  | Tipo di dati   | Valore                                      |
|-------------------------------------------------------|-------------|--------------------------------------------|
| Estensione di file senza il separatore punto (.) | **REG \_ SZ** | Stringa che specifica il percorso di una libreria |



 

L'altra voce del Registro di sistema viene riportata nella sottochiave seguente creata.

**HKEY \_ CLASSES \_ \\ ROOT** *customExtension*

dove *customExtension è* l'estensione del nome file incluso il separatore punto (.).

Il formato della voce del Registro di sistema è il seguente.



| Nome          | Tipo di dati   | Valore                                      |
|---------------|-------------|--------------------------------------------|
| PerceivedType | **REG \_ SZ** | Stringa che specifica il percorso di una libreria |



 

Entrambe le voci del Registro di sistema devono avere lo stesso valore. I valori possibili sono specificati nella tabella seguente.



| Valore | Descrizione                                                                      |
|-------|----------------------------------------------------------------------------------|
| Audio | I file con l'estensione personalizzata vengono visualizzati nella parte relativa alla musica della libreria. |
| Video | I file con l'estensione personalizzata vengono visualizzati nella parte video della libreria. |



 

Ad esempio, le voci del Registro di sistema seguenti specificano che i file con estensione xyz verranno visualizzati nella parte musica della libreria:


```C++

HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\MLS\Extensions
    xyz     REG_SZ     audio

HKEY_CLASSES_ROOT\.xyz
    PerceivedType     REG_SZ     audio

```



Si noti che qualsiasi codice che tenta di scrivere nel Registro di sistema nel computer dell'utente può scrivere nel sottoalbero HKEY LOCAL MACHINE solo se l'utente corrente dispone di \_ \_ privilegi amministrativi.

Le voci del Registro di sistema di classificazione delle librerie sono supportate dalle versioni seguenti Windows Media Player.

-   Windows Media Player serie 9 con hotfix 823275
-   Windows Media Player 10 e versioni successive

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**File Name Extension Registry Impostazioni**](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




