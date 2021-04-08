---
description: Gli autori dei pacchetti di installazione possono specificare che il programma di installazione copia i file condivisi (dll comunemente condivise) di un'applicazione nella cartella di tale applicazione anziché in un percorso condiviso.
ms.assetid: eb5f7088-30e0-4644-813a-c93e6f56ccbf
title: Componenti isolati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f29f614dfd819e093c5729a9a97a076247d281d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750119"
---
# <a name="isolated-components"></a>Componenti isolati

Gli autori dei pacchetti di installazione possono specificare che il programma di installazione copia i file condivisi (dll comunemente condivise) di un'applicazione nella cartella di tale applicazione anziché in un percorso condiviso. Questo set di file privato (dll) viene quindi usato solo dall'applicazione. L'isolamento dell'applicazione insieme ai componenti condivisi in questo modo presenta i vantaggi seguenti:

-   L'applicazione usa sempre le versioni dei file condivisi con cui è stata distribuita.
-   L'installazione dell'applicazione non sovrascrive altre versioni dei file condivisi da altre applicazioni.
-   Le installazioni successive di altre applicazioni che utilizzano versioni diverse dei file condivisi non possono sovrascrivere i file utilizzati da questa applicazione.

Poiché l'implementazione corrente di COM mantiene un unico percorso completo nel registro di sistema per ogni coppia CLSID/contesto, impone a tutte le applicazioni di usare la stessa versione di una DLL condivisa. Per consentire a un'applicazione di memorizzare una copia privata di un server COM, il caricatore di sistema in Windows 2000 verifica la presenza di una. File locale nella cartella dell'applicazione. Se il caricatore di sistema rileva un oggetto. Il file locale modifica la logica di ricerca per preferire le dll che si trovano nella stessa cartella dell'applicazione.

Quando Windows Installer esegue l' [azione IsolateComponents](isolatecomponents-action.md) , copiano i file del componente (in genere una DLL condivisa) specificata nella \_ colonna condivisa Component della [tabella IsolatedComponent](isolatedcomponent-table.md) nella stessa cartella del componente, in genere un file con estensione exe, specificato nella \_ colonna applicazione componente. Il programma di installazione crea un file in questa directory, con una lunghezza pari a zero byte, con il nome di file breve del file di chiave per l' \_ applicazione componente (in genere il nome è lo stesso dell'applicazione con estensione exe) accodato con. Locale. Il programma di installazione usa la registrazione per il componente nel percorso condiviso e non scrive le informazioni di registrazione per la copia del componente nel percorso privato.

Per altre informazioni, vedere:

-   [Installazione di componenti isolati](installation-of-isolated-components.md)
-   [Reinstallazione dei componenti isolati](reinstallation-of-isolated-components.md)
-   [Rimozione di componenti isolati](removal-of-isolated-components.md)
-   [Utilizzo di componenti isolati](using-isolated-components.md)

 

 



