---
description: Gli amministratori possono controllare la quantità di dati che ciascun utente può archiviare in un volume file system NTFS.
ms.assetid: 42efbd5b-6455-4319-a76e-cdb666fc36b8
title: Gestione delle quote disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5231d7683f0af40e7006193be8d5ff9390e21b65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317771"
---
# <a name="managing-disk-quotas"></a>Gestione delle quote disco

Il file system NTFS supporta le *quote disco* che consentono agli amministratori di controllare la quantità di dati che ciascun utente può archiviare in un volume file system NTFS. Gli amministratori possono facoltativamente configurare il sistema per la registrazione di un evento quando gli utenti sono vicini alla propria quota e per negare ulteriore spazio su disco agli utenti che superano la quota. Gli amministratori possono inoltre generare report e utilizzare Monitoraggio eventi per tenere traccia dei problemi di quota.

È possibile determinare se un file system supporta le quote disco chiamando la funzione [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) ed esaminando il flag di bit **\_ \_ quote volume file** .

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                   | Descrizione                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [Amministrazione a livello di utente di quote disco](user-level-administration-of-disk-quotas.md)<br/>     | Come ottenere maggiore spazio libero su disco dopo il superamento della quota di quote.<br/>                                                                  |
| [Amministrazione a livello di sistema di quote disco](system-level-administration-of-disk-quotas.md)<br/> | L'amministratore di sistema può impostare le quote per utenti specifici in un volume. L'amministratore può inoltre impostare le quote predefinite per il volume.<br/> |
| [Limiti della quota del disco](disk-quota-limits.md)<br/>                                                   | Descrive due tipi di limiti di quota del disco e il modo in cui vengono misurati i limiti delle quote del disco<br/>                                                      |
| [Interfacce di quota disco](disk-quota-interfaces.md)<br/>                                           | Interfacce utilizzate con le quote disco.<br/>                                                                                                     |



 

 

 




