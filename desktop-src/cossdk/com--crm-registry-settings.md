---
description: Sono disponibili diverse impostazioni del registro di sistema per modificare il comportamento di CRM per facilitare la risoluzione dei problemi e lo sviluppo.
ms.assetid: c4e68451-fb8a-45b5-9968-7d5a6418dfe8
title: Impostazioni del registro di sistema COM+ CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac0ea4ec245ab55b73c79660973824fcf33c6c2b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877513"
---
# <a name="com-crm-registry-settings"></a>Impostazioni del registro di sistema COM+ CRM

Sono disponibili diverse impostazioni del registro di sistema per modificare il comportamento di CRM per facilitare la risoluzione dei problemi e lo sviluppo. Tutte queste impostazioni del registro di sistema, elencate e descritte nella tabella seguente, sono facoltative. nessuno è necessario per il normale funzionamento del CRM.

Tutte le impostazioni del registro di sistema CRM si trovano in **HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ COM3 \\ CRM**. Creare la chiave **CRM** sotto la chiave **COM3** se non è già presente.



| Impostazioni del registro di sistema CRM                  | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **VTRACE1**<br/>                 | \_Valore reg DWORD. L'impostazione di questo valore su qualsiasi valore diverso da zero consente di eseguire il debug dei messaggi di traccia su avvisi o errori. Questi messaggi possono essere visualizzati nella finestra di output del debugger. Questo valore deve essere impostato solo per lo sviluppo e non durante la distribuzione normale. Questo valore viene letto quando viene avviata un'applicazione server CRM.<br/>                                                                                                                                                                                                                                                   |
| **IgnoreCompensatorErrors**<br/> | \_Valore reg DWORD. L'impostazione di questo valore su un valore diverso da zero consente all'infrastruttura CRM di ignorare tutti gli errori restituiti dai compensatori CRM. Se il ripristino non riesce a causa di un errore di un compensatore CRM, l'impostazione di questo valore consente il completamento del ripristino. Questo valore viene letto quando viene avviata un'applicazione server CRM.<br/>                                                                                                                                                                                                                                           |
| **CheckpointIntervalInSec**<br/> | \_Valore reg DWORD. Si tratta dell'intervallo di checkpoint in secondi. L'intervallo di checkpoint predefinito è 30 secondi. I checkpoint vengono usati per recuperare spazio dal file di log CRM. L'aumento dell'intervallo di checkpoint può migliorare le prestazioni, ma a scapito di un aumento del tempo di recupero e di un file di log CRM più grande. Questo valore viene letto quando viene avviata un'applicazione server CRM.<br/>                                                                                                                                                                                                  |
| **InitialLogFileSizeInKB**<br/>  | \_Valore reg DWORD. Si tratta delle dimensioni iniziali del file di log CRM, espressa in kilobyte. Le dimensioni predefinite del file di log CRM sono pari a 1024 KB (1 MB). Il file di log CRM si espande automaticamente per soddisfare il carico di transazione imposto, ma se si prevede un carico elevato, potrebbe essere necessario aumentare questo valore. Questo valore viene letto quando viene avviata un'applicazione server COM+ abilitata per CRM, ma se il file di log CRM esiste già per un'applicazione server CRM, questo valore viene ignorato per l'applicazione server.<br/>                                                                               |
| **RecoveryTraceEnabled**<br/>    | \_Valore reg DWORD. L'impostazione di questo valore su qualsiasi valore diverso da zero Abilita una traccia di ripristino. La traccia di ripristino è un file di testo con lo stesso nome del file di log CRM e la seguente estensione aggiuntiva: .recoverytrace.txt. <br/> Questo file si trova nella stessa directory del file di log CRM. La traccia di recupero fornisce una traccia dell'attività CRM durante il ripristino, che può essere usata per la diagnosi dei problemi. Questo valore viene letto quando viene avviata un'applicazione server CRM. Viene tuttavia generato un file di traccia di ripristino univoco per ogni applicazione server CRM.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti Gestione risorse di compensazione COM+](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 




