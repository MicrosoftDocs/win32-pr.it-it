---
title: Voce del Registro di sistema Autorizzazioni
description: Voce del Registro di sistema Autorizzazioni
ms.assetid: 01d55d2d-fe29-4006-a34b-9fbc730f9cbc
keywords:
- Windows Media Player,estensioni di file
- Windows Media Player,autorizzazioni
- Windows Media Player,registro
- registro, estensioni di file
- registro, autorizzazioni
- registro, impostazioni per Windows Media Player
- Impostazioni del Registro di sistema dell'estensione di file
- autorizzazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec5feaae3ebf55359f664e40df26b52912d727446ad715cd552d92cc1d090ad0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117747738"
---
# <a name="permissions-registry-entry"></a>Voce del Registro di sistema Autorizzazioni

Quando Windows Media Player rileva un'estensione di file personalizzata, cerca una sottochiave del Registro di sistema corrispondente all'estensione. La sottochiave è descritta in [Registro estensioni file Impostazioni](file-name-extension-registry-settings.md). Una delle voci del Registro di sistema che possono essere visualizzate nella sottochiave dell'estensione è **la voce** Autorizzazioni.

La **voce** Autorizzazioni specifica le azioni che Windows Media Player eseguire sui file con estensione personalizzata. La **voce Autorizzazioni** ha il formato seguente.



| Nome        | Type           | valore                                                                  |
|-------------|----------------|------------------------------------------------------------------------|
| Autorizzazioni | **REG \_ DWORD** | Set di flag, ognuno dei quali concede l'autorizzazione per un'azione specifica. |



 

Il valore della **voce Autorizzazioni** è UN **OR** bit per bit di uno o più dei flag seguenti.



| Flag (valore decimale) | Descrizione                                                                                                                                                                                                                                                                   |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1                    | Autorizzazione per la riproduzione. È possibile riprodurre i file con l'estensione di file registrata.                                                                                                                                                                                       |
| 2                    | Autorizzazione per l'eliminazione della cartella. I file con l'estensione di file registrata verranno inclusi nella playlist creata quando l'utente trascina una cartella contenente i file e la rilascia nell'interfaccia utente di Player.                                                      |
| 4                    | Autorizzazione per il CD multimediale. I file con l'estensione di file registrata verranno inclusi nella playlist creata quando un CD contenente i file viene inserito nell'unità CD-ROM.                                                                                           |
| 8                    | Autorizzazione per la libreria. I file con l'estensione di file registrata possono essere aggiunti alla libreria. Obbligatorio per i plug-in di conversione.                                                                                                                                    |
| 16                   | Autorizzazione per il flusso HTML. I file con l'estensione di file registrata verranno inseriti nella cache Internet Explorer quando vengono recapitati da un flusso Web.                                                                                                            |
| 128                  | Autorizzazione per la transcoding. I file con l'estensione di file registrata possono essere transcodificati Windows formato multimediale in determinate condizioni. Vedere [IWMPTranscodePolicy::allowTranscode](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmptranscodepolicy-allowtranscode). Richiede Windows Media Player 10 o versione successiva. |



 

Quando l'utente tenta di riprodurre un file multimediale con un'estensione di file personalizzata, Windows Media Player cerca una sottochiave del Registro di sistema corrispondente all'estensione. Se non viene trovata alcuna corrispondenza, il lettore visualizza all'utente una finestra di dialogo di avviso che richiede all'utente l'autorizzazione per tentare di riprodurre il file. Se si creano file multimediali digitali con estensioni di file personalizzate, è possibile impedire la visualizzazione di questo avviso nel computer dell'utente registrando l'estensione del nome file e specificando una **voce Autorizzazioni.**

La **voce Autorizzazioni** (ad eccezione del valore del flag 128) è supportata da Windows Media Player serie 9 e successive. Il valore del flag 128 è supportato da Windows Media Player 10 e versioni successive.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**File Name Extension Registry Impostazioni**](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




