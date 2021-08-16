---
title: Estensioni del dispositivo per le preferenze degli oggetti playlist
description: Estensioni del dispositivo per le preferenze degli oggetti playlist
ms.assetid: 33b3dd18-fda2-4bf9-a893-5d77cdde6b80
keywords:
- Windows Media Player,estensioni del dispositivo
- Windows Media Player,estensioni
- Windows Media Player,Preferenze degli oggetti playlist
- estensioni del dispositivo,preferenze degli oggetti playlist
- estensioni,preferenze degli oggetti playlist
- Oggetto Playlist
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f2acb01de41b753a85fee1c69e0bf015c687da04f50a10531ee5c67b0a13cc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118340920"
---
# <a name="device-extensions-for-playlist-object-preferences"></a>Estensioni del dispositivo per le preferenze degli oggetti playlist

Come parte del processo di sincronizzazione, Windows Media Player 10 o versioni successive copia gli oggetti playlist nei dispositivi portatili abilitati per MTP. Windows Media Player 11 introduce una nuova funzionalità che consente ai dispositivi portatili di limitare i tipi di oggetti playlist copiati. (Windows Media Player sempre il contenuto della playlist come specificato dalle regole di sincronizzazione. Questa funzionalità influisce solo sulla sincronizzazione degli oggetti playlist. Windows Media Player copia tre tipi di oggetti playlist dal computer al dispositivo:

-   **Playlist ordinarie.** Si tratta di playlist visibili nella **funzionalità Libreria** di Windows Media Player. Sono incluse le playlist create dall'utente, le playlist aggiunte alla libreria dai negozi online e le playlist di esempio installate con Player. Windows Media Player copia solo queste playlist nel dispositivo quando l'utente le ha selezionate per la sincronizzazione.
-   **Playlist di sincronizzazione stock.** Si tratta di playlist speciali installate con Windows Media Player e usate solo per la sincronizzazione. Queste playlist sono visibili solo nel Windows Media Player dispositivo Installazione guidata.
-   **Playlist create in modo implicito.** Queste playlist vengono create quando l'utente trascina e rilascia una cartella di categorie, ad esempio **Artista** o **Album,** nel riquadro in cui sono elencati gli elementi da sincronizzare.

Il file di intestazione denominato wmpdevices.h, aggiornato per questa versione, definisce le strutture e le costanti necessarie per supportare Windows Media Player estensioni del dispositivo.

Perché un dispositivo sia riconosciuto come preferenze dell'oggetto playlist di supporto tramite il set di estensioni del dispositivo MTP Windows Media Player, deve includere le informazioni seguenti nel set di dati DeviceInfo. Per altre informazioni su questo set di dati, vedere la sezione 4.6.1 della specifica MTP.



| Campo del set di dati          | Ordine dei campi | Tipo di dati  | Valore                       |
|------------------------|-------------|------------|-----------------------------|
| VendorExtensionID      | 2           | **UINT32** | 0x00000006                  |
| VendorExtensionVersion | 3           | **UINT16** | 0x0064 (100)                |
| VendorExtensionDesc    | 4           | **Stringa** | "microsoft.com/WMPPD: 11.0" |



 

La tabella seguente fornisce informazioni dettagliate sull'operazione MTP per le preferenze degli oggetti playlist.



| Elemento                  | Descrizione                                                                                                                                                                                                                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Codice operazione        | 0x9203                                                                                                                                                                                                                                                                                          |
| Parametro dell'operazione 1 | 0                                                                                                                                                                                                                                                                                               |
| Parametro dell'operazione 2 | 0                                                                                                                                                                                                                                                                                               |
| Parametro dell'operazione 3 | 0                                                                                                                                                                                                                                                                                               |
| Parametro dell'operazione 4 | 0                                                                                                                                                                                                                                                                                               |
| Parametro dell'operazione 5 | 0                                                                                                                                                                                                                                                                                               |
| Dati                  | Il dispositivo restituisce un valore nel parametro di risposta 1 per indicare la preferenza di sincronizzazione dell'oggetto playlist.                                                                                                                                                                                      |
| Direzione dei dati        | R->I                                                                                                                                                                                                                                                                                         |
| Opzioni del codice di risposta | MTP \_ RESPONSE \_ OK (0x2001) o codice di risposta di errore valido.                                                                                                                                                                                                                                        |
| Parametro di risposta 1  | 0 o 1. Il valore 0 indica che Windows Media Player sincronizzare solo gli oggetti playlist ordinari. Il valore 1 indica che tale Windows Media Player sincronizzare gli oggetti playlist ordinari, gli oggetti predefiniti e gli oggetti playlist di sincronizzazione creati in modo implicito, ovvero il comportamento predefinito. |
| Parametro di risposta 2  | 0                                                                                                                                                                                                                                                                                               |
| Parametro di risposta 3  | 0                                                                                                                                                                                                                                                                                               |
| Parametro di risposta 4  | 0                                                                                                                                                                                                                                                                                               |
| Parametro di risposta 5  | 0                                                                                                                                                                                                                                                                                               |



 

## <a name="remarks"></a>Commenti

L'implementazione di questa funzionalità è facoltativa per i dispositivi portatili. Windows Media Player sincronizza gli oggetti playlist ordinari, gli oggetti playlist di sincronizzazione stock e gli oggetti playlist creati in modo implicito per impostazione predefinita.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Windows Media Player**](windows-media-player.md)
</dt> </dl>

 

 




