---
description: La sezione install di un file INF definisce i passaggi della procedura di installazione.
ms.assetid: 24d40dc6-ac09-4cf8-9229-f81da2925576
title: Esempio di sezione di installazione INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39c8162dbf06b87faf8a1ce432c361a28befca0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315325"
---
# <a name="inf-install-section-example"></a>Esempio di sezione di installazione INF

La sezione **Install** di un file inf definisce i passaggi della procedura di installazione. Ogni riga di una sezione di **installazione** è costituita da due parti. A sinistra del segno di uguale (=) è la chiave. Sul lato destro è disponibile un elenco di uno o più titoli di sezione. La chiave specifica il tipo di sezioni elencate a destra. Per una descrizione del formato di questa sezione, vedere le sezioni e le direttive dei file INF del Microsoft Windows 2000 Driver Development Kit.

Di seguito è riportato un esempio di una sezione di **installazione** .

``` syntax
[MyInstallSection]
Copyfiles=DataFiles, ProgramFiles
Delfiles=OldFiles
UpdateInis=NewIniInfo
AddReg=NewRegistryInfo, MoreNewRegistryInfo
DelReg=OldRegistryInfo, MoreOldRegistryInfo
```

In questo esempio la chiave **CopyFiles** è impostata sui valori "DataFiles" e "ProgramFiles". Vengono specificate due sezioni **copia file** nel file inf che contengono i nomi dei file di origine utilizzati per la copia delle operazioni. La destinazione per i file copiati verrebbe specificata in una sezione **DestinationDirs** nel file inf.

Alla chiave **delfiles** viene assegnato il valore "OldFiles". Viene specificata una sezione **Delete Files** che contiene informazioni rilevanti per le operazioni di eliminazione di file.

La chiave **UpdateInis** specifica le sezioni del **file ini di aggiornamento** contenenti informazioni sull'aggiornamento delle voci nel file ini.

Le chiavi **AddReg** e **DelReg** specificano le sezioni **Add Registry** ed **Delete** Registry contenenti informazioni sull'aggiunta o l'eliminazione di informazioni del registro di sistema.

 

 



