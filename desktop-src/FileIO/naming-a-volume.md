---
description: Un'etichetta è un nome descrittivo assegnato a un volume, in genere da un utente finale, per renderlo più semplice da riconoscere. Un volume può avere un'etichetta, una lettera di unità, entrambi o nessuno. Per impostare l'etichetta per un volume, utilizzare la funzione SetVolumeLabel.
ms.assetid: f640f42d-a703-4e2e-a6d3-09cbe989cd11
title: Denominazione di un volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6435b6b5c7283cf2fb9a98951698f79646dfdffa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883958"
---
# <a name="naming-a-volume"></a>Denominazione di un volume

Un'etichetta è un nome descrittivo assegnato a un volume, in genere da un utente finale, per renderlo più semplice da riconoscere. Un volume può avere un'etichetta, una lettera di unità, entrambi o nessuno. Per impostare l'etichetta per un volume, utilizzare la funzione [**SetVolumeLabel**](/windows/desktop/api/WinBase/nf-winbase-setvolumelabela) .

Molti fattori possono rendere difficile l'identificazione di volumi specifici usando solo lettere ed etichette di unità. Uno è che non è necessario che un volume disponga di una lettera di unità o di un'etichetta. Un altro è che due volumi diversi possono avere la stessa etichetta, rendendoli indistinguibili ad eccezione della lettera di unità. Un terzo fattore è che le assegnazioni di lettere di unità possono cambiare man seconda che i volumi vengono aggiunti e rimossi dal computer.

Per risolvere questo problema, il sistema operativo utilizza i *percorsi GUID del volume* per identificare i volumi. Si tratta di stringhe di questo tipo:

"\\\\?\\ Volume {*GUID*} \\ "

dove *GUID* è un identificatore univoco globale (Guid) che identifica il volume.

Un percorso GUID volume viene talvolta definito *nome del volume univoco*, poiché un percorso GUID del volume può riferirsi solo a un volume. Tuttavia, questo termine è fuorviante, perché un volume può avere più di un percorso GUID del volume.

Il \\ \\ prefisso "? \\ " Disabilita l'analisi del percorso e non è considerato parte del percorso. Per ulteriori informazioni sul prefisso " \\ \\ ? \\ ", vedere [denominazione di un file o di una directory](naming-a-file.md).

È necessario specificare percorsi completi quando si utilizzano i percorsi GUID del volume con il \\ \\ prefisso "? \\ ".

Una *cartella montata* è un'associazione tra una cartella in un volume e un altro volume, in modo che il percorso della cartella possa essere usato per accedere al volume. Se ad esempio si usa la funzione [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) per creare una cartella montata che associa il volume "d: \\ " alla cartella "C: \\ mountd \\ ", è possibile usare il percorso ("d: \\ " o "C: \\ mountd \\ ") per accedere al volume "d: \\ ".

Un *punto di montaggio del volume* è qualsiasi percorso in modalità utente che può essere usato per accedere a un volume. Sono disponibili tre tipi di punti di montaggio del volume:

-   Lettera di unità, ad esempio, "C: \\ ".
-   Un percorso GUID volume, ad esempio, " \\ \\ ? \\ Volume {26a21bda-a627-11D7-9931-806e6f6e6963} \\ ".
-   Una cartella montata, ad esempio, "C: \\ mountd \\ ".

Tutte le funzioni del volume e della cartella montata che accettano un percorso GUID del volume come parametro di input richiedono la barra rovesciata finale. Tutte le funzioni del volume e della cartella montata che restituiscono un percorso GUID del volume forniscono la barra rovesciata finale, ma questo non è il caso della funzione [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) . È possibile aprire un volume chiamando **CreateFile** e omettere la barra rovesciata finale dal nome del volume specificato. **CreateFile** elabora un percorso GUID del volume con una barra rovesciata accodata come directory radice del volume.

Il sistema operativo assegna un percorso GUID del volume a un volume quando il volume viene installato per la prima volta e quando il volume è formattato. Le funzioni volume e cartella montata utilizzano i percorsi GUID del volume per accedere ai volumi. Per ottenere il percorso GUID del volume per un volume, usare la funzione [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) .

Le lunghezze del percorso possono costituire un problema quando viene creata una cartella montata che associa un volume che dispone di un albero di directory Deep con una directory in un altro volume. Questo perché il percorso del volume viene concatenato al percorso della directory. Il **\_ percorso massimo** costante definito a livello globale definisce il numero massimo di caratteri consentiti per un percorso. Per ulteriori informazioni sul **\_ percorso massimo**, vedere [denominazione di un file o di una directory](naming-a-file.md). È possibile evitare questo vincolo eseguendo una delle operazioni seguenti:

-   Fare riferimento ai volumi in base ai relativi percorsi GUID volume.
-   Utilizzare le versioni Unicode (W) delle funzioni file che supportano il \\ \\ prefisso? \\ .

 

 



