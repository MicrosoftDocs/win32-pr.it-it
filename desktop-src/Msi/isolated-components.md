---
description: Gli autori dei pacchetti di installazione possono specificare che il programma di installazione copia i file condivisi (DLL comunemente condivise) di un'applicazione nella cartella dell'applicazione anziché in un percorso condiviso.
ms.assetid: eb5f7088-30e0-4644-813a-c93e6f56ccbf
title: Componenti isolati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08095e72862a94474b7096950ac5ed3b331e806456e72982ee9d7374ab9511b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013179"
---
# <a name="isolated-components"></a>Componenti isolati

Gli autori dei pacchetti di installazione possono specificare che il programma di installazione copia i file condivisi (DLL comunemente condivise) di un'applicazione nella cartella dell'applicazione anziché in un percorso condiviso. Questo set privato di file (DLL) viene quindi usato solo dall'applicazione. L'isolamento dell'applicazione con i relativi componenti condivisi in questo modo presenta i vantaggi seguenti:

-   L'applicazione usa sempre le versioni dei file condivisi con cui è stata distribuita.
-   L'installazione dell'applicazione non sovrascrive altre versioni dei file condivisi da altre applicazioni.
-   Le installazioni successive di altre applicazioni che usano versioni diverse dei file condivisi non possono sovrascrivere i file usati dall'applicazione.

Poiché l'implementazione corrente di COM mantiene un singolo percorso completo nel Registro di sistema per ogni coppia CLSID/contesto, impone a tutte le applicazioni di usare la stessa versione di una DLL condivisa. Per consentire a un'applicazione di mantenere una copia privata di un server COM, il caricatore di sistema in Windows 2000 verifica la presenza di . File LOCAL nella cartella dell'applicazione. Se il caricatore di sistema rileva un oggetto . LOCAL, modifica la logica di ricerca per preferire le DLL che si trovano nella stessa cartella dell'applicazione.

Quando Windows Installer esegue l'azione [IsolateComponents,](isolatecomponents-action.md) copiano i file del componente (in genere una DLL condivisa) specificati nella colonna Componente condiviso della tabella IsolatedComponent nella stessa cartella del componente (in genere un file .exe) specificato nella colonna Applicazione \_ [](isolatedcomponent-table.md) \_ componente. Il programma di installazione crea un file in questa directory di lunghezza pari a zero byte, con il nome file breve del file di chiave per l'applicazione componente (in genere il nome è lo stesso del .exe dell'applicazione) aggiunto con \_ . Locale. Il programma di installazione usa la registrazione per il componente nel percorso condiviso e non scrive informazioni di registrazione per la copia del componente nella posizione privata.

Per altre informazioni, vedere:

-   [Installazione di componenti isolati](installation-of-isolated-components.md)
-   [Reinstallazione dei componenti isolati](reinstallation-of-isolated-components.md)
-   [Rimozione di componenti isolati](removal-of-isolated-components.md)
-   [Uso di componenti isolati](using-isolated-components.md)

 

 



