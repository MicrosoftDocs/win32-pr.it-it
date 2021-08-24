---
title: Estensioni del dispositivo MTP per il trasferimento dei metadati
description: Estensioni del dispositivo MTP per il trasferimento dei metadati
ms.assetid: 9cf68373-e84f-4568-a9da-16ddee0fc4e9
keywords:
- Windows Media Player,estensioni del dispositivo MTP
- Windows Media Player,estensioni del dispositivo
- Windows Media Player,estensioni
- Windows Media Player, metadati
- Windows Media Player,Media Transfer Protocol (MTP)
- Media Transfer Protocol (MTP)
- MTP (Media Transfer Protocol)
- metadati, estensioni del dispositivo MTP
- metadati, estensioni del dispositivo
- metadati, estensioni
- estensioni del dispositivo, trasferimento di metadati
- estensioni, trasferimento di metadati
- Estensioni del dispositivo MTP per il trasferimento dei metadati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c56f633d7cd4ca44a90d311c1e4c1c2e6d213e1d2ad1a43b802e4795a59a7d47
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119572441"
---
# <a name="mtp-device-extensions-for-metadata-transfer"></a>Estensioni del dispositivo MTP per il trasferimento dei metadati

Media Transfer Protocol (MTP) è un protocollo progettato per dispositivi multimediali portatili. Lo scopo principale di questo protocollo è fornire un protocollo comune per lo scambio di dati tra un computer e un dispositivo multimediale portatile. Ciò include la ricezione e l'invio di oggetti multimediali e l'enumerazione del contenuto e delle funzionalità del dispositivo.

MTP usa identificatori di oggetto univoci persistenti (PUOID) per identificare in modo univoco gli elementi multimediali digitali (e altri oggetti) archiviati in un dispositivo. Quando si scambiano informazioni sulle modifiche che si sono verificate in un dispositivo che supporta MTP, il dispositivo e il Windows Media Player usano i puoid per identificare quali oggetti sono stati modificati.

Il file di intestazione denominato wmpdevices.h, installato come parte di Windows Media Player SDK, definisce le strutture e le costanti necessarie per supportare Windows Media Player estensioni del dispositivo.

Perché un dispositivo sia riconosciuto come trasferimento di metadati di supporto tramite il set di estensioni del dispositivo Windows Media Player MTP, deve includere le informazioni seguenti nel set di dati DeviceInfo. Per altre informazioni su questo set di dati, vedere la sezione 4.6.1 della specifica MTP.



| Campo del set di dati          | Ordine dei campi | Tipo di dati  | Valore                       |
|------------------------|-------------|------------|-----------------------------|
| VendorExtensionID      | 2           | **UINT32** | 0x00000006                  |
| VendorExtensionVersion | 3           | **UINT16** | 0x0064 (100)                |
| VendorExtensionDesc    | 4           | **Stringa** | "microsoft.com/WMPPD: 10.0" |



 

La tabella seguente fornisce informazioni dettagliate sull'operazione MTP per il trasferimento accelerato dei metadati.



| Elemento                  | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Codice operazione        | 0x9201                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Parametro dell'operazione 1 | ID della transazione fornito dal dispositivo durante la sessione precedente. Questo valore è zero per la prima sessione.                                                                                                                                                                                                                                                                                                                                                                                       |
| Parametro dell'operazione 2 | Indice iniziale. Questo valore è sempre zero alla prima chiamata di una sessione. Nelle chiamate successive all'interno della stessa sessione di sincronizzazione, questo valore aumenta della somma del conteggio degli elementi modificati e eliminati dai dati di risposta precedenti.                                                                                                                                                                                                                                             |
| Parametro dell'operazione 3 | 0x10000. Questa costante, definita in wmpdevices.h, è il numero massimo di PUOID che possono essere restituiti nella risposta. Si noti che il valore di questa costante può essere modificato nelle versioni future di questo file di intestazione.                                                                                                                                                                                                                                                                                     |
| Parametro dell'operazione 4 | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Parametro dell'operazione 5 | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Dati                  | Il dispositivo restituisce due matrici MTP contigue contenenti ID. Ogni matrice MTP inizia con **un valore DWORD** che indica il conteggio degli elementi nella matrice, seguito dalla matrice di elementi . La prima matrice MTP contiene l'elenco dei PUOID aggiunti o modificati. La seconda matrice MTP contiene l'elenco dei PUOID che sono stati eliminati dal dispositivo portatile. Si noti che la somma del conteggio DELLE UNITÀ DI ARCHIVIAZIONE nelle due matrici non deve superare il valore passato nel parametro dell'operazione 3.<br/> |
| Direzione dei dati        | R->I                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Opzioni del codice di risposta | **MTP \_ RESPONSE \_ OK** (0x2001) o codice di risposta di errore valido.                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Parametro di risposta 1  | ID della transazione corrente del dispositivo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Parametro di risposta 2  | Numero di PUOID che rimangono da recuperare dalle richieste future.                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Parametro di risposta 3  | **DWORD contenente** informazioni sullo stato. Lo stato è indicato bit per bit. Per informazioni sui flag da usare, vedere La sezione Osservazioni.                                                                                                                                                                                                                                                                                                                                                                     |
| Parametro di risposta 4  | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Parametro di risposta 5  | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="remarks"></a>Commenti

Lo stato viene indicato tramite il parametro di risposta 3 in modo bit per bit usando i flag seguenti.



| Flag                                             | valore | Descrizione                                                                                                                                                                                                                          |
|--------------------------------------------------|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **WMP \_ MDRT \_ FLAGS \_ UNREPORTED \_ DELETED \_ ITEMS** | 0x1   | Gli elementi sono stati eliminati prima che venga segnalato il nome del primo percorso dell'oggetto. Questo spesso indica che il dispositivo è stato riformattato.                                                                                                           |
| **WMP \_ MDRT \_ FLAGS \_ UNREPORTED \_ ADDED \_ ITEMS**   | 0x2   | Il dispositivo contiene alcuni elementi aggiunti che non possono essere restituiti nell'elenco di PUOIDS. Si noti che questo flag non è ridondante con il parametro di risposta 2. Impostare questo flag solo quando sono presenti elementi richiesti che il dispositivo non può restituire. |



 

I bit da 2 a 31 sono riservati per un uso futuro. Questi bit devono essere impostati su zero.

Windows Media Player invia il comando MTP a un dispositivo all'inizio di una sessione di sincronizzazione prima del trasferimento dei file multimediali. Il dispositivo deve restituire la risposta il più rapidamente possibile per evitare ritardi nell'operazione di sincronizzazione.

Windows Media Player richiederà valori per gli attributi elencati in [Informazioni](about-the-metadata.md) sui metadati per ogni POUID modificato restituito nella risposta. Windows Media Player inviare i valori aggiornati per questi attributi al dispositivo nei comandi successivi.

I file segnalati come rimossi dal dispositivo possono essere copiati nuovamente nel dispositivo se le impostazioni dell'utente lo richiedono.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Estensioni del dispositivo per il trasferimento accelerato dei metadati**](device-extensions-for-accelerated-metadata-transfer.md)
</dt> </dl>

 

 





