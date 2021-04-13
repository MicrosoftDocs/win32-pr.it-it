---
description: Il programma di installazione registra errori ed eventi nel proprio log degli errori.
ms.assetid: 244e9afa-2052-469e-aa57-424e03ce5673
title: Registrazione normale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0846305ef53c596fbd6f117eaf76b0715a94c313
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528170"
---
# <a name="normal-logging"></a>Registrazione normale

Il programma di installazione registra errori ed eventi nel proprio log degli errori. Il tipo di registrazione eseguito dal programma di installazione è determinato dall'impostazione della modalità di registrazione. La registrazione è abilitata e la modalità può essere impostata usando i metodi seguenti:

-   È possibile specificare la modalità di registrazione di un'installazione avviata dalla riga di comando usando l'opzione/L delle [Opzioni della riga di comando](command-line-options.md). Se la modalità di registrazione non viene specificata tramite l'opzione della riga di comando/L, verrà utilizzata la modalità di registrazione predefinita.
-   La modalità di registrazione di un processo di installazione può essere specificata a livello di codice tramite la funzione [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga) o il metodo [**EnableLog**](installer-enablelog.md) . Se la modalità di registrazione non viene specificata tramite la funzione **MsiEnableLog** o il metodo **EnableLog** , verrà utilizzata la modalità di registrazione predefinita.
-   È possibile specificare la modalità di registrazione predefinita di un particolare pacchetto di installazione impostando la proprietà [**MsiLogging**](msilogging.md) nella [tabella delle proprietà](property-table.md) del pacchetto. Questa proprietà è disponibile a partire da Windows Installer 4,0.
-   Se la proprietà [**MsiLogging**](msilogging.md) è presente nella [tabella delle proprietà](property-table.md), è possibile modificare la modalità di registrazione predefinita del pacchetto modificando il valore utilizzando una trasformazione del [database](database-transforms.md). La modalità di registrazione predefinita non può essere modificata usando i [pacchetti di patch](patch-packages.md) (un file con estensione msp).
-   Se la proprietà [**MsiLogging**](msilogging.md) non è stata impostata, è possibile specificare la modalità di registrazione predefinita per tutti gli utenti del computer utilizzando i criteri di [registrazione](logging.md) .
-   Se è stata impostata la proprietà [**MsiLogging**](msilogging.md) , è possibile specificare la modalità di registrazione predefinita per tutti gli utenti del computer impostando il criterio [DisableLoggingFromPackage](disableloggingfrompackage.md) e i criteri di [registrazione](logging.md) .
-   Se la modalità di registrazione non è stata specificata mediante l'opzione/L, [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga), [**EnableLog**](installer-enablelog.md), la proprietà [**MsiLogging**](msilogging.md) o i criteri di [registrazione](logging.md) , la modalità di registrazione predefinita per il pacchetto è la stessa, ottenuta impostando la proprietà **MsiLogging** su' iwearmo '.

 

 



