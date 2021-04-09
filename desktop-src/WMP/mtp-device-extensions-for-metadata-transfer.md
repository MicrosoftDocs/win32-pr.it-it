---
title: Estensioni del dispositivo MTP per il trasferimento dei metadati
description: Estensioni del dispositivo MTP per il trasferimento dei metadati
ms.assetid: 9cf68373-e84f-4568-a9da-16ddee0fc4e9
keywords:
- Windows Media Player, estensioni del dispositivo MTP
- Windows Media Player, estensioni del dispositivo
- Windows Media Player, estensioni
- Media Player di Windows, metadati
- Windows Media Player, Media Transfer Protocol (MTP)
- Protocollo MTP (Media Transfer Protocol)
- MTP (Media Transfer Protocol)
- metadati, estensioni del dispositivo MTP
- metadati, estensioni del dispositivo
- metadati, estensioni
- estensioni del dispositivo, trasferimento di metadati
- estensioni, trasferimento di metadati
- Estensioni del dispositivo MTP per il trasferimento dei metadati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f64ff16fd97f135d7f8c902af823b967079408fb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044038"
---
# <a name="mtp-device-extensions-for-metadata-transfer"></a>Estensioni del dispositivo MTP per il trasferimento dei metadati

Il protocollo MTP (Media Transfer Protocol) è un protocollo progettato per i dispositivi multimediali portatili. Lo scopo principale di questo protocollo è fornire un protocollo comune per lo scambio di dati tra un computer e un dispositivo multimediale portatile. Ciò include la ricezione e l'invio di oggetti multimediali e l'enumerazione del contenuto e delle funzionalità del dispositivo.

MTP usa identificatori di oggetti univoci (PUOIDs) permanenti per identificare in modo univoco gli elementi multimediali digitali (e altri oggetti) archiviati in un dispositivo. Quando si scambiano informazioni sulle modifiche apportate in un dispositivo che supporta MTP, il dispositivo e Windows Media Player usano PUOIDs per identificare quali oggetti sono stati modificati.

Il file di intestazione denominato wmpdevices. h, che viene installato come parte di Windows Media Player SDK, definisce le strutture e le costanti necessarie per supportare le estensioni del dispositivo Windows Media Player.

Affinché un dispositivo venga riconosciuto come supporto per il trasferimento dei metadati tramite il set di estensioni del dispositivo Windows Media Player MTP, deve includere le seguenti informazioni nel set di dati DeviceInfo. Per ulteriori informazioni su questo set di dati, vedere la sezione 4.6.1 della specifica MTP.



| Campo del set di dati          | Ordine campi | Tipo di dati  | Valore                       |
|------------------------|-------------|------------|-----------------------------|
| VendorExtensionID      | 2           | **UINT32** | 0x00000006                  |
| VendorExtensionVersion | 3           | **UINT16** | 0x0064 (100)                |
| VendorExtensionDesc    | 4           | **Stringa** | "microsoft.com/WMPPD: 10,0" |



 

La tabella seguente fornisce informazioni dettagliate sull'operazione MTP per il trasferimento di metadati accelerati.



| Elemento                  | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Codice operativo        | 0x9201                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Parametro dell'operazione 1 | ID transazione fornito dal dispositivo durante la sessione precedente. Questo valore è zero per la prima sessione.                                                                                                                                                                                                                                                                                                                                                                                       |
| Parametro dell'operazione 2 | Indice iniziale. Questo valore è sempre zero nella prima chiamata di una sessione. Nelle chiamate successive all'interno della stessa sessione di sincronizzazione, questo valore aumenta in base alla somma del conteggio degli elementi modificati e degli elementi eliminati dai dati di risposta precedenti.                                                                                                                                                                                                                                             |
| Parametro dell'operazione 3 | 0x10000. Questa costante, definita in wmpdevices. h, è il numero massimo di PUOIDs che possono essere restituiti nella risposta. Si noti che il valore di questa costante può essere modificato nelle versioni future di questo file di intestazione.                                                                                                                                                                                                                                                                                     |
| Parametro dell'operazione 4 | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Parametro dell'operazione 5 | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Data                  | Il dispositivo restituisce due matrici MTP contigue che contengono PUOIDs. Ogni array MTP inizia con un valore **DWORD** che indica il numero di elementi nella matrice, seguito dalla matrice di elementi. La prima matrice MTP contiene l'elenco di PUOIDs che sono stati aggiunti o modificati. Il secondo array MTP contiene l'elenco di PUOIDs che sono stati eliminati dal dispositivo portatile. Si noti che la somma del numero di PUOID nelle due matrici non deve superare il valore passato nel parametro operation 3.<br/> |
| Direzione dati        | R->I                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Opzioni del codice di risposta | **MTP \_ RISPOSTA \_ OK** (0x2001) o codice di risposta di errore valido.                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Parametro di risposta 1  | ID della transazione corrente del dispositivo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Parametro di risposta 2  | Numero di PUOIDs che rimangono per essere recuperate dalle richieste future.                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Parametro di risposta 3  | **DWORD** che contiene informazioni sullo stato. Lo stato è indicato in modalità bit per bit. Per informazioni sui flag da usare, vedere la sezione Osservazioni.                                                                                                                                                                                                                                                                                                                                                                     |
| Parametro di risposta 4  | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Parametro di risposta 5  | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="remarks"></a>Commenti

Lo stato è indicato dal parametro di risposta 3 in modalità bit per bit usando i flag seguenti.



| Flag                                             | valore | Descrizione                                                                                                                                                                                                                          |
|--------------------------------------------------|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MDRT i flag di WMP non \_ \_ \_ segnalati \_ \_ elementi eliminati** | 0x1   | Gli elementi sono stati eliminati prima che venisse segnalato il primo nome del percorso dell'oggetto. Questo indica spesso che il dispositivo è stato riformattato.                                                                                                           |
| **MDRT i flag di WMP non \_ \_ \_ segnalati \_ \_ elementi aggiunti**   | 0x2   | Il dispositivo contiene alcuni elementi aggiunti che non possono essere restituiti nell'elenco di PUOIDS. Si noti che questo flag non è ridondante con il parametro di risposta 2. Impostare questo flag solo quando sono presenti elementi richiesti che il dispositivo non può restituire. |



 

I bit da 2 a 31 sono riservati per un uso futuro. Questi bit devono essere impostati su zero.

Windows Media Player invia il comando MTP a un dispositivo all'inizio di una sessione di sincronizzazione prima del trasferimento dei file multimediali. Il dispositivo deve restituire la risposta il più rapidamente possibile per evitare ritardi nell'operazione di sincronizzazione.

Windows Media Player richiederà i valori per gli attributi elencati in [informazioni sui metadati](about-the-metadata.md) per ogni POUID modificato restituito nella risposta. Windows Media Player potrebbe inviare i valori aggiornati per questi attributi al dispositivo nei comandi successivi.

I file segnalati come rimossi dal dispositivo possono essere copiati di nuovo nel dispositivo se le impostazioni dell'utente lo richiedono.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Estensioni del dispositivo per il trasferimento di metadati accelerati**](device-extensions-for-accelerated-metadata-transfer.md)
</dt> </dl>

 

 





