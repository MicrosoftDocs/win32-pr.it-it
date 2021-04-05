---
title: Estensioni dispositivo per preferenze oggetto playlist
description: Estensioni dispositivo per preferenze oggetto playlist
ms.assetid: 33b3dd18-fda2-4bf9-a893-5d77cdde6b80
keywords:
- Windows Media Player, estensioni del dispositivo
- Windows Media Player, estensioni
- Windows Media Player, preferenze oggetto playlist
- estensioni del dispositivo, preferenze oggetto playlist
- estensioni, preferenze oggetto playlist
- Oggetto playlist
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fd9c6301e33307fc49e50b8aa9042752e020e32
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712733"
---
# <a name="device-extensions-for-playlist-object-preferences"></a>Estensioni dispositivo per preferenze oggetto playlist

Nell'ambito del processo di sincronizzazione, Windows Media Player 10 o versioni successive copia gli oggetti playlist nei dispositivi portatili abilitati per MTP. Windows Media Player 11 introduce nuove funzionalità che consentono ai dispositivi portatili di limitare i tipi di oggetti Playlist copiati. (Windows Media Player Sincronizza sempre il contenuto della playlist come specificato dalle regole di sincronizzazione. Questa funzionalità ha effetto solo sulla sincronizzazione degli oggetti playlist. Windows Media Player copia tre tipi di oggetti playlist dal computer al dispositivo:

-   **Playlist ordinarie.** Si tratta di playlist che sono visibili nella funzionalità della **libreria** di Windows Media Player. Sono incluse le playlist create dall'utente, le playlist aggiunte alla libreria da negozi online e le playlist di esempio installate con il lettore. Windows Media Player copia solo queste playlist nel dispositivo quando l'utente le seleziona per la sincronizzazione.
-   **Playlist di sincronizzazione azionaria.** Si tratta di playlist speciali installate con Windows Media Player e usate solo per la sincronizzazione. Queste playlist sono visibili solo nell'installazione guidata del dispositivo Windows Media Player.
-   **Playlist create in modo implicito.** Queste playlist vengono create quando l'utente trascina e rilascia una cartella di categoria, ad esempio **Artist** o **album**, nel riquadro in cui sono elencati gli elementi da sincronizzare.

Il file di intestazione denominato wmpdevices. h, che è stato aggiornato per questa versione, definisce le strutture e le costanti necessarie per supportare le estensioni del dispositivo Windows Media Player.

Affinché un dispositivo venga riconosciuto come supporto per le preferenze degli oggetti playlist tramite il set di estensioni del dispositivo Windows Media Player MTP, deve includere le informazioni seguenti nel set di dati DeviceInfo. Per ulteriori informazioni su questo set di dati, vedere la sezione 4.6.1 della specifica MTP.



| Campo del set di dati          | Ordine campi | Tipo di dati  | Valore                       |
|------------------------|-------------|------------|-----------------------------|
| VendorExtensionID      | 2           | **UINT32** | 0x00000006                  |
| VendorExtensionVersion | 3           | **UINT16** | 0x0064 (100)                |
| VendorExtensionDesc    | 4           | **Stringa** | "microsoft.com/WMPPD: 11,0" |



 

La tabella seguente fornisce informazioni dettagliate sull'operazione MTP per le preferenze dell'oggetto playlist.



| Elemento                  | Descrizione                                                                                                                                                                                                                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Codice operativo        | 0x9203                                                                                                                                                                                                                                                                                          |
| Parametro dell'operazione 1 | 0                                                                                                                                                                                                                                                                                               |
| Parametro dell'operazione 2 | 0                                                                                                                                                                                                                                                                                               |
| Parametro dell'operazione 3 | 0                                                                                                                                                                                                                                                                                               |
| Parametro dell'operazione 4 | 0                                                                                                                                                                                                                                                                                               |
| Parametro dell'operazione 5 | 0                                                                                                                                                                                                                                                                                               |
| Data                  | Il dispositivo restituisce un valore nel parametro di risposta 1 per indicare la preferenza di sincronizzazione dell'oggetto playlist.                                                                                                                                                                                      |
| Direzione dati        | R->I                                                                                                                                                                                                                                                                                         |
| Opzioni del codice di risposta | \_Risposta MTP \_ OK (0x2001) o codice di risposta di errore valido.                                                                                                                                                                                                                                        |
| Parametro di risposta 1  | 0 o 1. Il valore 0 indica che Windows Media Player deve sincronizzare solo gli oggetti della playlist ordinaria. Il valore 1 indica che Windows Media Player deve sincronizzare gli oggetti della playlist ordinaria, le azioni e gli oggetti della playlist di sincronizzazione creati in modo implicito, che è il comportamento predefinito. |
| Parametro di risposta 2  | 0                                                                                                                                                                                                                                                                                               |
| Parametro di risposta 3  | 0                                                                                                                                                                                                                                                                                               |
| Parametro di risposta 4  | 0                                                                                                                                                                                                                                                                                               |
| Parametro di risposta 5  | 0                                                                                                                                                                                                                                                                                               |



 

## <a name="remarks"></a>Commenti

L'implementazione di questa funzionalità è facoltativa per i dispositivi portatili. Windows Media Player sincronizza gli oggetti della playlist ordinaria, gli oggetti playlist della sincronizzazione azionaria e gli oggetti playlist creati in modo implicito per impostazione predefinita.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Windows Media Player**](windows-media-player.md)
</dt> </dl>

 

 




