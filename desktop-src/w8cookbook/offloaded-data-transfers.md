---
title: Trasferimenti dati scaricati
description: Trasferimenti dati scaricati
ms.assetid: 91EBE6D6-2DA7-48DA-AEB7-3FAFCA8341F5
keywords:
- ODX
- copia offload
- Offload
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1057ed27347fefc7ebc6a171eb7273da4341b024
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "106300569"
---
# <a name="offloaded-data-transfers"></a>Trasferimenti dati scaricati

## <a name="platforms"></a>Piattaforme

**Client** -Windows 8  
**Server** : Windows Server 2012  


## <a name="description"></a>Descrizione

Per promuovere lo spostamento dei dati di archiviazione, Microsoft ha sviluppato una nuova tecnologia di trasferimento dei dati (ODX). Invece di usare le operazioni di scrittura con memorizzazione nel buffer e di lettura memorizzate nel buffer, Windows ODX avvia l'operazione di copia con un offload Read e recupera un token che rappresenta i dati dal dispositivo di archiviazione, quindi usa un comando offload Write con il token per richiedere lo spostamento dei dati dal disco di origine al disco di destinazione. Il gestore delle copie dei dispositivi di archiviazione esegue lo spostamento dei dati in base al token. In Windows 8, il responsabile IT e l'amministratore di archiviazione sono in grado di utilizzare la funzionalità Windows ODX per interagire con il dispositivo di archiviazione per spostare file o dati di grandi dimensioni tramite la rete di archiviazione ad alta velocità. Windows ODX ridurrà significativamente il traffico di rete client-server e l'utilizzo della CPU durante i trasferimenti di dati di grandi dimensioni, perché tutto lo spostamento dei dati si trova nella rete di archiviazione back-end. ODX può essere usato per la distribuzione di macchine virtuali, la migrazione massiccia dei dati e il supporto dei dispositivi di archiviazione a più livelli e può ridurre i costi di distribuzione dell'hardware fisico tramite le funzionalità di archiviazione ODX e thin provisioning.

> [!Note]  
> Questa funzionalità funzionerà solo sui dispositivi di archiviazione con implementazione della specifica SPC4 e SBC3.

 

## <a name="functional-details"></a>Dettagli funzionali

-   La funzionalità ODX di Windows è incorporata nel motore di copia del sistema operativo Windows; durante l'enumerazione dell'archiviazione, Windows eseguirà una query sulla funzionalità ODX del dispositivo di archiviazione
-   La copia del dispositivo di archiviazione di origine e della copia di destinazione deve essere gestita nello stesso gestore di copia per il supporto dell'offload di copia
-   Se un'operazione di offload di copia non riesce, il gestore delle copie del dispositivo di archiviazione deve restituire i dati di rilevamento appropriati appropriati per la gestione degli errori delle app
-   Il motore di copia di Windows eseguirà il fallback all'operazione di copia tradizionale se l'operazione di copia dell'offload non riesce

## <a name="using-odx"></a>Uso di ODX

-   L'app per il trasferimento dei dati deve garantire che sia il lun di origine della copia sia il LUN di destinazione della copia siano ODX, prima di chiamare le routine dell'API ODX
-   In Esplora risorse gli utenti possono usare "trascina" o "copia e incolla" per eseguire l'offload della copia
-   Quando il lun di origine e il LUN di destinazione sono montati con la file system, l'app deve chiamare solo FSCTL \_ offload \_ Read e FSCTL \_ offload \_ Write per eseguire il trasferimento dei dati dal LUN di origine al LUN di destinazione
-   Se un'operazione di offload di copia non riesce, il gestore delle copie del dispositivo di archiviazione deve restituire i dati di rilevamento aggiuntivi appropriati per la gestione degli errori delle app
-   Quando il lun di origine o il LUN di destinazione non è montato con il file system e bloccato, l'app deve chiamare l' \_ archiviazione IOCTL \_ gestire \_ \_ \_ gli attributi del set di dati con DeviceDsmAction \_ OffloadRead o DeviceDsmAction \_ OffloadWrite azione per eseguire l'offload della copia
-   Le app per la gestione dell'archiviazione possono usare l' \_ \_ API pass-through SCSI per eseguire trasferimenti di dati con offload quando i LUN di origine e di destinazione non sono montati con alcun file System e bloccato

## <a name="tests"></a>Test

-   Per garantire un'esperienza utente affidabile, verificare la certificazione Windows ODX dell'array di archiviazione
-   Per supportare la funzionalità ODX, il dispositivo di archiviazione deve essere conforme ai requisiti di certificazione per i trasferimenti di dati con offload di Windows (usati per essere logo)
-   Utilizzare il kit di certificazione hardware trasferimenti dati scaricati da Windows per verificare il supporto della funzionalità ODX dei dispositivi di archiviazione

## <a name="resources"></a>Risorse

-   Specifiche T10 XCOPY Lite (11-059r8)
    -   [https://www.t10.org/cgi-bin/ac.pl?t=f&f=spc4r35b.pdf](https://www.t10.org/cgi-bin/ac.pl?t=f&f=spc4r35b.pdf)
    -   [https://www.t10.org/cgi-bin/ac.pl?t=f&f=sbc3r30.pdf](https://www.t10.org/cgi-bin/ac.pl?t=f&f=sbc3r30.pdf)
-   [Servizi dashboard hardware](/windows-hardware/drivers/dashboard/)
-   [\_Struttura pass- \_ through SCSI](/windows-hardware/drivers/ddi/ntddscsi/ns-ntddscsi-_scsi_pass_through)

 

 