---
description: Un nome di dispositivo MS-DOS è una giunzione che punta al percorso di un dispositivo MS-DOS. Queste giunzioni costituiscono lo spazio dei nomi del dispositivo MS-DOS.
ms.assetid: 7d802e9f-dc09-4e3d-b064-e9b57af396e2
title: Definizione di un nome di dispositivo MS-DOS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77331c1d3b3cc7566f118fa19fbb13c84e82af634f1098193bdf3dcb6270ef7d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119638931"
---
# <a name="defining-an-ms-dos-device-name"></a>Definizione di un nome di dispositivo MS-DOS

Un nome di dispositivo MS-DOS è una giunzione che punta al percorso di un dispositivo MS-DOS. Queste giunzioni costituiscono lo spazio dei nomi del dispositivo MS-DOS. Chiamare le [**funzioni DefineDosDevice**](/windows/desktop/api/FileAPI/nf-fileapi-definedosdevicew) [**e SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) per creare e modificare queste giunzioni. [**DeleteVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw) elimina una giunzione creata da **SetVolumeMountPoint** e **DefineDosDevice** elimina le giunzioni create.

Dopo aver definito il nome di un dispositivo MS-DOS, questo rimane visibile a tutti i processi.

-   Tutti i dispositivi MS-DOS vengono identificati da Windows tramite un ID di autenticazione. Un ID di autenticazione è il LUID (identificatore univoco locale) associato a ogni sessione di accesso al momento della creazione.
-   La visibilità di un nome di dispositivo MS-DOS è classificata come globale o locale e viene definita come tale dalla relativa inclusione negli spazi dei nomi Global MS-DOS Device e Local MS-DOS Device. Il contenuto dei dispositivi MS-DOS nello spazio dei nomi Globale è accessibile a tutti gli utenti e il contenuto dei dispositivi MS-DOS nello spazio dei nomi Locale può essere accessibile solo dall'utente il cui token di accesso contiene l'AuthenticationID associato allo spazio dei nomi del dispositivo MS-DOS locale.

Possono esistere più spazi dei nomi del dispositivo MS-DOS locale e un solo spazio dei nomi del dispositivo MS-DOS globale contemporaneamente e in un computer.

Si noti che solo i processi in esecuzione nel contesto LocalSystem possono chiamare [**DefineDosDevice**](/windows/desktop/api/FileAPI/nf-fileapi-definedosdevicew) per creare un dispositivo MS-DOS nello spazio dei nomi del dispositivo MS-DOS globale. Inoltre, lo spazio dei nomi del dispositivo MS-DOS locale corrispondente a un AuthenticationID specifico viene eliminato quando viene rimosso l'ultimo riferimento a tale AuthenticationID.

Quando il codice esegue una query sul nome di un dispositivo MS-DOS esistente chiamando [**QueryDosDevice,**](/windows/desktop/api/FileAPI/nf-fileapi-querydosdevicew)cerca innanzitutto lo spazio dei nomi del dispositivo MS-DOS locale. Se non viene trovato, la funzione cerca lo spazio dei nomi Del dispositivo MS-DOS globale. Quando il codice esegue una query su tutti i nomi di dispositivo MS-DOS esistenti tramite questa funzione, l'elenco di nomi restituiti dipende dal fatto che sia in esecuzione nel contesto LocalSystem. In tal caso, verranno restituiti solo i nomi dei dispositivi MS-DOS inclusi nello spazio dei nomi Global MS-DOS Device. In caso contrario, verrà restituita una concatenazione dei nomi dei dispositivi negli spazi dei nomi Global e Local MS-DOS Device. Se esiste un nome di dispositivo in entrambi gli spazi dei nomi, **QueryDosDevice** restituirà la voce nello spazio dei nomi Local MS-DOS Device. Questo vale anche per l'elenco di tutti i nomi di dispositivo MS-DOS restituiti da [**GetLogicalDrives**](/windows/desktop/api/FileAPI/nf-fileapi-getlogicaldrives) e [**GetLogicalDriveStrings**](/windows/desktop/api/FileAPI/nf-fileapi-getlogicaldrivestringsw).

Si noti che può verificarsi lo scenario seguente:

1.  L'utente A, che non è in esecuzione nel contesto LocalSystem, crea un nome di dispositivo nello spazio dei nomi Local MS-DOS Device corrispondente e tale nome non esiste nello spazio dei nomi Global MS-DOS Device.
2.  L'utente B, che è in esecuzione nel contesto LocalSystem, crea lo stesso nome di dispositivo nello spazio dei nomi Globale del dispositivo MS-DOS.

In questo scenario, l'utente A non avrà accesso al nome del dispositivo nello spazio dei nomi Del dispositivo MS-DOS globale finché non rimuove o rinomina il nome del dispositivo nello spazio dei nomi del dispositivo MS-DOS locale. Per ridurre la probabilità che questo scenario si verifichi, le lettere di unità MS-DOS devono essere allocate nello spazio dei nomi Globale del dispositivo MS-DOS a partire da C: e terminando con Z:. Questa sequenza deve essere inversa per l'allocazione di lettere di unità MS-DOS nello spazio dei nomi Del dispositivo MS-DOS locale.

Se non si esegue all'interno del contesto LocalSystem, [**DefineDosDevice**](/windows/desktop/api/FileAPI/nf-fileapi-definedosdevicew) non consentirà di definire un nome di dispositivo nello spazio dei nomi Del dispositivo MS-DOS locale se il nome del dispositivo esiste già negli spazi dei nomi del dispositivo MS-DOS locale o globale. Chiamare [**QueryDosDevice**](/windows/desktop/api/FileAPI/nf-fileapi-querydosdevicew) prima di chiamare **DefineDosDevice** per determinare se il nome del dispositivo che si intende definire esiste negli spazi dei nomi del dispositivo MS-DOS.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Denominazione di file, percorsi e spazi dei nomi](naming-a-file.md)
</dt> </dl>

 

 



