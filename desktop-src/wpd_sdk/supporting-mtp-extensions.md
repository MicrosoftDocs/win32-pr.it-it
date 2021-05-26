---
description: Supporto delle estensioni MTP
ms.assetid: 9e5f3da6-346a-4eca-bc85-2755c569986d
title: Supporto delle estensioni MTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 898df3f1347af2ccc42a796b480156b6603b13ec
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423731"
---
# <a name="supporting-mtp-extensions"></a>Supporto delle estensioni MTP

## <a name="media-transfer-protocol"></a>Media Transfer Protocol

Il protocollo MTP (Media Transfer Protocol) è un'estensione del protocollo PTP (Picture Transfer Protocol). Di conseguenza, tutta la semantica del protocollo PTP è valida in MTP.

MTP comunica usando comandi e risposte tra due parti, l'iniziatore e il risponditore. I ruoli dei dispositivi coinvolti sono molto chiaramente definiti. Il PC è in genere l'iniziatore e il dispositivo è sempre il risponditore. Un dispositivo non PC può anche essere un iniziatore (ad esempio, un mazzo di auto o una scatola Microsoft X). Un dispositivo non può mai assumere entrambi i ruoli contemporaneamente.

L'iniziatore avvia la comunicazione inviando un comando al risponditore. Il risponditore elabora il comando e restituisce una risposta appropriata. Al comando potrebbe essere associata una fase dati. In questo caso, la direzione del flusso di dati deve essere nota in anticipo e accettata sia dall'iniziatore che dal risponditore. Tenere presente che non esiste un'intestazione descrittiva che indica i flussi di dati per i nuovi comandi.

Il risponditore può avviare la comunicazione indipendentemente dall'iniziatore. Ad esempio, il risponditore può inviare eventi all'iniziatore. Tuttavia, non è possibile inviare dati insieme all'evento . Se sono presenti dati che devono essere letti come parte dell'evento, l'iniziatore deve inviare un comando MTP e il dispositivo può quindi inviare dati in risposta al comando.

Per una descrizione completa di MTP, vedere la specifica [MTP](https://www.usb.org/sites/default/files/MTPv1_1.zip).

## <a name="sending-mtp-commands"></a>Invio di comandi MTP

Le applicazioni possono inviare comandi MTP a un dispositivo richiamando il [**metodo IPortableDevice::SendCommand.**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand) Il comando inviato dipende dal fatto che sia presente una fase dati e dal fatto che tutti i dati che accompagnano vengono letti o scritti nel dispositivo. Nella tabella seguente vengono descritti i tre possibili comandi di estensione MTP.

Tenere presente che questi comandi sono specifici di MTP. e sono pertanto implementati solo dal driver di classe MTP WPD.



| Comando  | Descrizione  |
|--------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**TRASFERIMENTO DEI DATI \_ DI FINE DEL COMANDO \_ WPD MTP \_ EXT \_ \_ \_**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-end-data-transfer)                                      | Emetta un comando MTP che segnala la conclusione di un'operazione di lettura o scrittura dei dati.              |
| [**COMANDO WPD \_ \_ MTP \_ EXT \_ EXECUTE COMMAND WITHOUT DATA \_ \_ \_ \_ PHASE**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-without-data-phase)  | Consente di eseguire un comando MTP senza una fase dati corrispondente.                                         |
| [**COMANDO WPD \_ \_ MTP \_ EXT \_ EXECUTE CON DATI DA \_ \_ \_ \_ \_ SCRIVERE**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-write) | Viene eseguito un comando MTP seguito dai dati che accompagnano, che verranno scritti nel dispositivo. |
| [**COMANDO WPD \_ \_ MTP \_ EXT \_ EXECUTE CON DATI DA \_ \_ \_ \_ \_ LEGGERE**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-read)   | Consente di eseguire un comando MTP seguito dai dati correlati, che vengono letti dal dispositivo.       |
| [**COMANDO WPD \_ \_ MTP \_ EXT \_ LETTURA \_ DATI**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-read-data)                                                       | Invia un comando MTP che invia i dati dal dispositivo al PC.                                  |
| [**WPD \_ COMMAND \_ MTP \_ EXT \_ WRITE \_ DATA**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-write-data)                                                     | Invia un comando MTP che invia dati al dispositivo dal PC.                                  |



 

Indipendentemente dalla fase, è necessario specificare **WPD \_ PROPERTY \_ MTP \_ EXT \_ OPERATION \_ CODE** e **WPD \_ PROPERTY \_ MTP \_ EXT OPERATION \_ \_ PARAMS.**

Se il driver MTP è stato in grado di inviare il comando al dispositivo, i valori restituiti conterranno sempre **WPD \_ PROPERTY \_ MTP \_ EXT \_ RESPONSE \_ CODE**. Se il codice di risposta indica l'esito positivo e se la semantica del comando consente i parametri di risposta, saranno disponibili anche **WPD \_ PROPERTY \_ MTP \_ EXT \_ RESPONSE \_ PARAMS.**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida per programmatori**](programming-guide.md)
</dt> </dl>

 

 
