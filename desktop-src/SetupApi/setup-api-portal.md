---
description: Installa driver di dispositivo da programmi con uno script di configurazione e file inf. Scrivere un programma di installazione per la configurazione del dispositivo e l'installazione dei driver. Questa API non è più consigliata per l'installazione di applicazioni software.
ms.assetid: 96a9e472-9b92-4976-9379-dc0c96524963
title: API di installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6101c2673e72095d0cf4ebe59c1cece83449d647
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313277"
---
# <a name="setup-api"></a>API di installazione

## <a name="purpose"></a>Scopo

L'API di installazione di fornisce un set di funzioni che un'applicazione di installazione chiama per eseguire operazioni di installazione.

## <a name="where-applicable"></a>Se applicabile

Queste funzioni di installazione sono disponibili per lo sviluppo di un'applicazione di installazione. Non è più possibile usare l'API di installazione per l'installazione delle applicazioni. Usare invece il [Windows Installer](/windows/desktop/Msi/windows-installer-portal)per lo sviluppo di programmi di installazione dell'applicazione. L'API di installazione continua a essere usata per l'installazione dei driver di dispositivo.

L'API di installazione è destinata allo sviluppo di applicazioni di tipo desktop.

## <a name="developer-audience"></a>Sviluppatori

Uno sviluppatore può usare l'API di installazione se l'applicazione di installazione richiede le funzionalità seguenti:

-   Accodamento di file.
-   Installazione dei file.
-   Gestione degli errori di installazione e della richiesta di supporto.
-   Aggiornamento delle voci del registro di sistema.
-   Registrazione dei file durante l'installazione.
-   Archiviazione dei percorsi di origine usati più di recente.

## <a name="run-time-requirements"></a>Requisiti di runtime

Per informazioni sui sistemi operativi necessari per usare una funzione specifica, vedere la sezione requisiti della documentazione relativa alla funzione.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                 | Descrizione                                                                                 |
|---------------------------------------|---------------------------------------------------------------------------------------------|
| [Overview](overview.md)<br/>   | Informazioni generali sull'API di installazione.<br/>                                             |
| [Riferimento](reference.md)<br/> | Documentazione relativa ai tipi di dati dell'API di installazione, alle strutture, alle funzioni e alle notifiche.<br/> |



 

 

