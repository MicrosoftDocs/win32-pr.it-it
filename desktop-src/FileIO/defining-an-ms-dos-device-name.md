---
description: Il nome di un dispositivo MS-DOS è un collegamento che punta al percorso di un dispositivo MS-DOS. Queste giunzioni costituiscono lo spazio dei nomi del dispositivo MS-DOS.
ms.assetid: 7d802e9f-dc09-4e3d-b064-e9b57af396e2
title: Definizione di un nome di dispositivo MS-DOS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ed89e1d9938e320ecce3ff0b35b8ae0792fe219
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310031"
---
# <a name="defining-an-ms-dos-device-name"></a>Definizione di un nome di dispositivo MS-DOS

Il nome di un dispositivo MS-DOS è un collegamento che punta al percorso di un dispositivo MS-DOS. Queste giunzioni costituiscono lo spazio dei nomi del dispositivo MS-DOS. Chiamare le funzioni [**DefineDosDevice**](/windows/desktop/api/FileAPI/nf-fileapi-definedosdevicew) e [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) per creare e modificare tali giunzioni. [**DeleteVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw) Elimina una giunzione creata da **SetVolumeMountPoint** e **DefineDosDevice** Elimina le giunzioni che crea.

Una volta definito, il nome del dispositivo MS-DOS rimane visibile a tutti i processi.

-   Tutti i dispositivi MS-DOS sono identificati da Windows tramite un ID di autenticazione. Un ID di autenticazione è l'identificatore univoco locale (LUID) associato a ogni sessione di accesso al momento della creazione.
-   La visibilità di un nome di dispositivo MS-DOS è stata categorizzata come globale o locale e viene definita in base alla relativa inclusione nel dispositivo MS-DOS globale e negli spazi dei nomi del dispositivo MS-DOS locale. Il contenuto dei dispositivi MS-DOS nello spazio dei nomi globale è accessibile a tutti gli utenti e il contenuto dei dispositivi MS-DOS nello spazio dei nomi locale è accessibile solo all'utente il cui token di accesso contiene il AuthenticationID associato allo spazio dei nomi del dispositivo MS-DOS locale.

Più spazi dei nomi del dispositivo MS-DOS locale e un solo spazio dei nomi del dispositivo MS-DOS globale possono esistere in una sola volta e in un computer.

Si noti che solo i processi in esecuzione nel contesto LocalSystem possono chiamare [**DefineDosDevice**](/windows/desktop/api/FileAPI/nf-fileapi-definedosdevicew) per creare un dispositivo MS-DOS nello spazio dei nomi del dispositivo MS-DOS globale. Inoltre, lo spazio dei nomi del dispositivo MS-DOS locale corrispondente a un AuthenticationID specifico viene eliminato quando viene rimosso l'ultimo riferimento a tale AuthenticationID.

Quando il codice esegue una query su un nome di dispositivo MS-DOS esistente chiamando [**QueryDosDevice**](/windows/desktop/api/FileAPI/nf-fileapi-querydosdevicew), cerca innanzitutto nello spazio dei nomi del dispositivo MS-DOS locale. Se non viene trovato, la funzione effettuerà la ricerca nello spazio dei nomi del dispositivo MS-DOS globale. Quando il codice esegue una query su tutti i nomi di dispositivo MS-DOS esistenti tramite questa funzione, l'elenco di nomi restituiti dipende dal fatto che sia in esecuzione nel contesto LocalSystem. In tal caso, verranno restituiti solo i nomi di dispositivo MS-DOS inclusi nello spazio dei nomi del dispositivo MS-DOS globale. In caso contrario, verrà restituita una concatenazione dei nomi di dispositivo negli spazi dei nomi del dispositivo MS-DOS globale e locale. Se il nome di un dispositivo è presente in entrambi gli spazi dei nomi, **QueryDosDevice** restituirà la voce nello spazio dei nomi del dispositivo MS-DOS locale. Questo vale anche per l'elenco di tutti i nomi di dispositivo MS-DOS restituiti da [**GetLogicalDrives**](/windows/desktop/api/FileAPI/nf-fileapi-getlogicaldrives) e [**GetLogicalDriveStrings**](/windows/desktop/api/FileAPI/nf-fileapi-getlogicaldrivestringsw).

Si noti che è possibile che si verifichi lo scenario seguente:

1.  L'utente A, che non è in esecuzione all'interno del contesto LocalSystem, crea il nome di un dispositivo nello spazio dei nomi del dispositivo MS-DOS locale corrispondente e tale nome non esiste nello spazio dei nomi del dispositivo MS-DOS globale.
2.  L'utente B, che viene eseguito all'interno del contesto LocalSystem, crea lo stesso nome di dispositivo nello spazio dei nomi del dispositivo MS-DOS globale.

In questo scenario, l'utente A non potrà accedere al nome del dispositivo nello spazio dei nomi del dispositivo MS-DOS globale fino a quando non rimuove o Rinomina il nome del dispositivo nello spazio dei nomi del dispositivo MS-DOS locale. Per ridurre la probabilità che si verifichi questo scenario, le lettere di unità MS-DOS devono essere allocate nello spazio dei nomi del dispositivo MS-DOS globale che inizia con C: e termina con E z:. Questa sequenza deve essere invertita per l'allocazione delle lettere di unità MS-DOS nello spazio dei nomi del dispositivo MS-DOS locale.

Se non è in esecuzione nel contesto LocalSystem, [**DefineDosDevice**](/windows/desktop/api/FileAPI/nf-fileapi-definedosdevicew) non consentirà di definire un nome dispositivo nello spazio dei nomi del dispositivo MS-DOS locale se il nome del dispositivo esiste già negli spazi dei nomi del dispositivo MS-DOS locale o globale. Chiamare [**QueryDosDevice**](/windows/desktop/api/FileAPI/nf-fileapi-querydosdevicew) prima di chiamare **DefineDosDevice** per determinare se il nome del dispositivo che si intende definire esiste negli spazi dei nomi del dispositivo MS-DOS.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Denominazione di file, percorsi e spazi dei nomi](naming-a-file.md)
</dt> </dl>

 

 



