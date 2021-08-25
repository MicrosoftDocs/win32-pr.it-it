---
description: Il programma di installazione registra gli errori e gli eventi nel proprio log degli errori.
ms.assetid: 244e9afa-2052-469e-aa57-424e03ce5673
title: Registrazione normale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dd1abeb4f110603bcc596cb7981ea65c7d9820d8054adc7533c4f85de2d8bf7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828541"
---
# <a name="normal-logging"></a>Registrazione normale

Il programma di installazione registra gli errori e gli eventi nel proprio log degli errori. Il tipo di registrazione eseguito dal programma di installazione è determinato dall'impostazione della modalità di registrazione. La registrazione è abilitata e la modalità può essere impostata usando i metodi seguenti:

-   La modalità di registrazione di un'installazione avviata dalla riga di comando può essere specificata usando l'opzione /L delle opzioni della riga [di comando](command-line-options.md). Se la modalità di registrazione non viene specificata tramite l'opzione della riga di comando /L , verrà utilizzata la modalità di registrazione predefinita.
-   La modalità di registrazione di un processo di installazione può essere specificata a livello di codice usando la [**funzione MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga) o il [**metodo EnableLog.**](installer-enablelog.md) Se la modalità di registrazione non viene specificata tramite la funzione **MsiEnableLog** o il **metodo EnableLog,** verrà usata la modalità di registrazione predefinita.
-   La modalità di registrazione predefinita di un particolare pacchetto di installazione può essere specificata impostando la [**proprietà MsiLogging**](msilogging.md) nella [tabella Property](property-table.md) del pacchetto. Questa proprietà è disponibile a partire da Windows Installer 4.0.
-   Se la [**proprietà MsiLogging**](msilogging.md) è presente nella tabella [Property](property-table.md), la modalità di registrazione predefinita del pacchetto può essere modificata modificando il valore usando una trasformazione [del database](database-transforms.md). Non è possibile modificare la modalità di registrazione predefinita usando [Patch Packages](patch-packages.md) (un file msp).
-   Se la [**proprietà MsiLogging**](msilogging.md) non è stata impostata, è possibile specificare la modalità di registrazione predefinita per tutti gli utenti del computer usando i [criteri di](logging.md) registrazione.
-   Se è stata impostata la proprietà [**MsiLogging,**](msilogging.md) è possibile specificare la modalità di registrazione predefinita per tutti gli utenti del computer impostando i criteri [DisableLoggingFromPackage](disableloggingfrompackage.md) e [Registrazione.](logging.md)
-   Se la modalità di registrazione non è stata specificata dall'opzione /L, [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga), [**EnableLog**](installer-enablelog.md), [**proprietà MsiLogging**](msilogging.md) o dai criteri di registrazione, la modalità di registrazione predefinita per il pacchetto è la stessa modalità ottenuta impostando la proprietà **MsiLogging** su 'iloggingmo'. [](logging.md)

 

 



