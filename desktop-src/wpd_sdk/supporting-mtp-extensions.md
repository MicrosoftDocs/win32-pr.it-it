---
description: Supporto delle estensioni MTP
ms.assetid: 9e5f3da6-346a-4eca-bc85-2755c569986d
title: Supporto delle estensioni MTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f26a6a5a585167984ec944528bb74a6746e42ac4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884169"
---
# <a name="supporting-mtp-extensions"></a>Supporto delle estensioni MTP

## <a name="media-transfer-protocol"></a>Protocollo di trasferimento multimediale

Il protocollo MTP (Media Transfer Protocol) è un'estensione del protocollo PTP (Picture Transfer Protocol). Di conseguenza, tutte le semantiche del protocollo PTP sono valide in MTP.

MTP comunica con i comandi e le risposte tra due parti, l'iniziatore e il risponditore. I ruoli dei dispositivi interessati sono ben definiti. Il PC è in genere l'initiator e il dispositivo è sempre il risponditore. Un dispositivo non PC può anche essere un iniziatore (ad esempio, un car deck o un Microsoft X-box). Un dispositivo non può mai assumere entrambi i ruoli nello stesso momento.

L'initiator avvia la comunicazione inviando un comando al risponditore. Il risponditore elabora il comando e restituisce una risposta appropriata. Potrebbe essere presente una fase di dati associata al comando. In tal caso, la direzione del flusso di dati deve essere nota in anticipo e accettata sia dall'initiator che dal risponditore. Tenere presente che non è presente un'intestazione descrittiva che indica i flussi di dati per i nuovi comandi.

Il risponditore può avviare la comunicazione indipendentemente dall'initiator. Ad esempio, il risponditore può inviare eventi all'initiator. Tuttavia, non è possibile inviare dati insieme all'evento. Se sono presenti dati che devono essere letti come parte dell'evento, l'iniziatore deve inviare un comando MTP e il dispositivo può inviare i dati in risposta al comando.

Per una descrizione completa di MTP, vedere la [specifica MTP](https://www.usb.org/sites/default/files/MTPv1_1.zip).

## <a name="sending-mtp-commands"></a>Invio di comandi MTP

Le applicazioni possono inviare comandi MTP a un dispositivo richiamando il metodo [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand) . Il comando inviato dipende dalla presenza o meno di una fase di dati e dall'eventuale lettura o scrittura di dati associati nel dispositivo. Nella tabella seguente vengono descritti i tre possibili comandi dell'estensione MTP.

Tenere presente che questi comandi sono specifici per MTP; e sono pertanto implementati solo dal driver della classe MTP WPD.



|                                                                                                                                      |                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| Comando                                                                                                                              | Descrizione                                                                                       |
| [**\_comando WPD \_ MTP \_ ext \_ End \_ data \_ Transfer**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-end-data-transfer)                                      | Rilascia un comando MTP che segnala la conclusione di un'operazione di lettura o scrittura dei dati.              |
| [**\_comando WPD \_ comando \_ MTP \_ ext \_ Execute \_ senza \_ \_ fase dati**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-without-data-phase)  | Rilascia un comando MTP senza una fase di dati corrispondente.                                         |
| [**comando \_ WPD \_ MTP \_ ext \_ Execute \_ \_ con \_ dati \_ da \_ scrivere**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-write) | Rilascia un comando MTP seguito da dati associati, che verranno scritti nel dispositivo. |
| [**comando \_ WPD \_ MTP \_ ext \_ Execute \_ \_ con \_ dati \_ da \_ leggere**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-read)   | Rilascia un comando MTP seguito da dati associati, che vengono letti dal dispositivo.       |
| [**\_comando WPD \_ MTP \_ ext \_ Read \_ Data**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-read-data)                                                       | Rilascia un comando MTP che invia i dati dal dispositivo al PC.                                  |
| [**\_comando WPD \_ MTP \_ ext \_ scrivere \_ dati**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-write-data)                                                     | Rilascia un comando MTP che invia i dati al dispositivo dal PC.                                  |



 

Indipendentemente dalla fase, è necessario specificare la **Proprietà WPD del \_ \_ \_ \_ \_ codice operativo MTP EXT** e la **\_ Proprietà WPD \_ MTP \_ ext \_ Operation \_ params** .

Se il driver MTP è stato in grado di inviare il comando al dispositivo, i valori restituiti conterranno sempre il **\_ \_ codice di \_ \_ risposta \_ MTP EXT della proprietà WPD**. Se il codice di risposta indica l'esito positivo e se la semantica del comando consente i parametri di risposta, saranno disponibili anche i **\_ param della proprietà WPD MTP della \_ \_ \_ risposta \_** .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida per programmatori**](programming-guide.md)
</dt> </dl>

 

 
