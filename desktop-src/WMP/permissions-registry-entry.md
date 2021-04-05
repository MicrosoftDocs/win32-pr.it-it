---
title: Voce del registro di sistema autorizzazioni
description: Voce del registro di sistema autorizzazioni
ms.assetid: 01d55d2d-fe29-4006-a34b-9fbc730f9cbc
keywords:
- Windows Media Player, estensioni di file
- Windows Media Player, autorizzazioni
- Windows Media Player, registro di sistema
- Registro di sistema, estensioni di file
- Registro di sistema, autorizzazioni
- Registro di sistema, impostazioni per Windows Media Player
- impostazioni del registro di sistema estensione del nome file
- autorizzazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aec86b4facec4babed4afed04ca342903670dbb
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046284"
---
# <a name="permissions-registry-entry"></a>Voce del registro di sistema autorizzazioni

Quando Windows Media Player rileva un'estensione del nome di file personalizzata, Cerca una sottochiave del registro di sistema corrispondente all'estensione. La sottochiave è descritta in [impostazioni del registro di sistema estensione del nome file](file-name-extension-registry-settings.md). Una delle voci del registro di sistema che possono essere visualizzate sotto la sottochiave dell'estensione è la voce **autorizzazioni** .

La voce **autorizzazioni** specifica le azioni che Windows Media Player può eseguire sui file con estensione personalizzata. La voce **autorizzazioni** ha il formato seguente.



| Nome        | Type           | valore                                                                  |
|-------------|----------------|------------------------------------------------------------------------|
| Autorizzazioni | **REG \_ DWORD** | Set di flag, ciascuno dei quali concede l'autorizzazione per un'azione specifica. |



 

Il valore della voce delle **autorizzazioni** è un **or** bit per bit di uno o più dei flag seguenti.



| Flag (valore decimale) | Descrizione                                                                                                                                                                                                                                                                   |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1                    | Autorizzazione per la riproduzione. È possibile riprodurre i file con l'estensione di file registrato.                                                                                                                                                                                       |
| 2                    | Autorizzazione per l'eliminazione della cartella. I file con estensione registrata verranno inclusi nella playlist creata quando l'utente trascina una cartella che contiene i file e la rilascia sull'interfaccia utente del lettore.                                                      |
| 4                    | Autorizzazione per il CD multimediale. I file con l'estensione di file registrata verranno inclusi nella playlist creata quando un CD contenente i file viene inserito nell'unità CD-ROM.                                                                                           |
| 8                    | Autorizzazione per la libreria. I file con l'estensione di file registrata possono essere aggiunti alla libreria. Obbligatorio per i plug-in di conversione.                                                                                                                                    |
| 16                   | Autorizzazione per lo streaming HTML. I file con l'estensione del nome file registrato verranno inseriti nella cache di Internet Explorer quando vengono recapitati da un flusso Web.                                                                                                            |
| 128                  | Autorizzazione per la transcodifica. I file con l'estensione del nome file registrato possono essere trascodificati in formato Windows Media in determinate condizioni. Vedere [IWMPTranscodePolicy:: allowTranscode](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmptranscodepolicy-allowtranscode). Richiede Windows Media Player 10 o versione successiva. |



 

Quando l'utente tenta di riprodurre un file multimediale con estensione di file personalizzata, Windows Media Player ricerca una sottochiave del registro di sistema corrispondente all'estensione. Se non viene trovata alcuna corrispondenza, il lettore Visualizza all'utente una finestra di dialogo di avviso che richiede all'utente l'autorizzazione per tentare di riprodurre il file. Se si creano file multimediali digitali con estensioni di file personalizzate, è possibile impedire che questo avviso venga visualizzato nel computer dell'utente registrando l'estensione del nome file e specificando una voce di **autorizzazione** .

La voce relativa alle **autorizzazioni** (ad eccezione del valore del flag 128) è supportata dalla serie Windows Media Player 9 e versioni successive. Il valore del flag 128 è supportato da Windows Media Player 10 e versioni successive.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Impostazioni del registro di sistema estensione del nome file**](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




