---
title: Estensioni del dispositivo per la creazione di report sul contenuto acquisito
description: Estensioni del dispositivo per la creazione di report sul contenuto acquisito
ms.assetid: 597d872e-9105-4edb-afa3-9f4407de0f73
keywords:
- Windows Media Player,estensioni del dispositivo
- Windows Media Player,estensioni
- Windows Media Player,creazione di report sul contenuto acquisito
- estensioni del dispositivo, creazione di report sul contenuto acquisito
- estensioni, creazione di report sul contenuto acquisito
- creazione di report sul contenuto acquisito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3389f5b35cedc853d66e6f450836195497628972ea6ae15642d75155d8b83b6c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902061"
---
# <a name="device-extensions-for-reporting-acquired-content"></a>Estensioni del dispositivo per la creazione di report sul contenuto acquisito

Windows Media Player 11 introduce una nuova funzionalità che consente ai dispositivi portatili di notificare al lettore il contenuto aggiunto al dispositivo dopo l'ultima sincronizzazione. Windows Media Player 11 può usare queste informazioni per copiare il contenuto appena acquisito dal dispositivo al computer dell'utente. I produttori di dispositivi devono tenere presente i requisiti seguenti per il supporto di questa funzionalità:

-   Questa funzionalità è supportata solo per i dispositivi abilitati per MTP.
-   Questa funzionalità funziona solo con i dispositivi che hanno una relazione con Windows Media Player.
-   I dispositivi devono segnalare solo il contenuto creato o scaricato dal dispositivo. Sono incluse le foto scattate dal dispositivo. registrazioni vocali create dal dispositivo; registrazioni di messaggi vocali; download da una scheda di archiviazione; e download da Internet. Il contenuto archiviato nel dispositivo in seguito alla sincronizzazione con un altro dispositivo o a una relazione diversa non deve essere segnalato.

Il file di intestazione denominato wmpdevices.h, installato come parte di Windows Media Player SDK, definisce le strutture e le costanti necessarie per supportare Windows Media Player estensioni del dispositivo.

Perché un dispositivo sia riconosciuto come supporto per la creazione di report del contenuto acquisito tramite il set di estensioni del dispositivo MTP Windows Media Player, deve includere le informazioni seguenti nel set di dati DeviceInfo. Per altre informazioni su questo set di dati, vedere la sezione 4.6.1 della specifica MTP.



| Campo del set di dati          | Ordine dei campi | Tipo di dati  | Valore                       |
|------------------------|-------------|------------|-----------------------------|
| VendorExtensionID      | 2           | **UINT32** | 0x00000006                  |
| VendorExtensionVersion | 3           | **UINT16** | 0x0064 (100)                |
| VendorExtensionDesc    | 4           | **Stringa** | "microsoft.com/WMPPD: 11.0" |



 

La tabella seguente fornisce informazioni dettagliate sull'operazione MTP per la creazione di report sul contenuto acquisito.



| Elemento                  | Descrizione                                                                                                                                                                                                                     |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Codice operazione        | 0x9202                                                                                                                                                                                                                          |
| Parametro dell'operazione 1 | ID transazione fornito dal dispositivo durante la sessione precedente. Questo valore è zero per la prima sessione.                                                                                                                |
| Parametro dell'operazione 2 | Indice iniziale. Questo valore è sempre zero alla prima chiamata di una sessione. Nelle chiamate successive all'interno della stessa sessione di sincronizzazione, questo valore aumenta del conteggio degli elementi restituiti dai dati di risposta precedenti. |
| Parametro dell'operazione 3 | 0x10000. Questa costante, definita in wmpdevices.h, è il numero massimo di PUOID che possono essere restituiti nella risposta. Si noti che il valore di questa costante può essere modificato nelle versioni future di questo file di intestazione.              |
| Parametro dell'operazione 4 | 0                                                                                                                                                                                                                               |
| Parametro dell'operazione 5 | 0                                                                                                                                                                                                                               |
| Dati                  | Il dispositivo restituisce una matrice MTP contenente i PUOID acquisiti. La matrice inizia con un **valore DWORD** che indica il conteggio degli elementi nella matrice, seguito dalla matrice di elementi.                               |
| Direzione dei dati        | R->I                                                                                                                                                                                                                         |
| Opzioni del codice di risposta | **MTP \_ RESPONSE \_ OK** (0x2001) o codice di risposta di errore valido.                                                                                                                                                                    |
| Parametro di risposta 1  | ID della transazione corrente.                                                                                                                                                                                                     |
| Parametro di risposta 2  | Numero di PUOID che rimangono da recuperare dalle richieste future.                                                                                                                                                            |
| Parametro di risposta 3  | **DWORD contenente** informazioni sullo stato. Lo stato è indicato in modo bit per bit. Per informazioni sui flag da usare, vedere Note.                                                                                              |
| Parametro di risposta 4  | 0                                                                                                                                                                                                                               |
| Parametro di risposta 5  | 0                                                                                                                                                                                                                               |



 

## <a name="remarks"></a>Commenti

Lo stato viene indicato tramite il parametro di risposta 3 in modo bit per bit usando il flag seguente.



| Flag                                              | valore | Descrizione                                                                                                                                                                                                                             |
|---------------------------------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **WMP \_ MDRT \_ \_ CONTRASSEGNA GLI ELEMENTI ACQUISITI \_ NON \_ SEGNALATI** | 0x1   | Il dispositivo contiene alcuni elementi acquisiti che non possono essere restituiti nell'elenco di PUOIDS. Si noti che questo flag non è ridondante con il parametro di risposta 2. Impostare questo flag solo quando sono presenti elementi richiesti che il dispositivo non può restituire. |



 

I bit da 1 a 31 sono riservati per un uso futuro. Questi bit devono essere impostati su zero.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Windows Media Player**](windows-media-player.md)
</dt> </dl>

 

 




