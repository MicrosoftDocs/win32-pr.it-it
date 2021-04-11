---
title: Uso della procedura guidata plug-in con Visual Studio
description: Uso della procedura guidata plug-in con Visual Studio
ms.assetid: 5d5521b7-5cbc-4259-92b1-a7250853fa2e
keywords:
- Plug-in di Windows Media Player, Visual Studio
- plug-in, Visual Studio
- creazione di plug-in, Visual Studio
- Creazione guidata plug-in di Windows Media Player, Visual Studio
- Visual Studio, creazione guidata plug-in di Windows Media Player
- procedura guidata plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c7f7db9bdc2a99a42f60c2faf38605e50e7dd3e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330711"
---
# <a name="using-the-plug-in-wizard-with-visual-studio"></a>Uso della procedura guidata plug-in con Visual Studio

Dopo aver installato i componenti necessari, è possibile creare rapidamente un plug-in che funge da punto di partenza. La procedura seguente illustra come eseguire questa operazione.

1.  Avviare Microsoft Visual Studio.
2.  Scegliere **nuovo** dal menu **file** , quindi fare clic su **progetto**.
3.  In **Tipi progetto** selezionare **Visual C++ progetti**.
4.  In **modelli** selezionare **creazione guidata plug-in di Windows Media Player**.
5.  Immettere un nome per il progetto.
6.  Immettere un percorso per il progetto. Si tratta della cartella in cui verranno copiati i file di progetto.
7.  Fare clic su **OK** per avviare la procedura guidata.
8.  Selezionare il tipo di plug-in che si desidera creare.
9.  Completare tutte le finestre di dialogo rimanenti della procedura guidata.
10. Usare l'ambiente di sviluppo di Visual Studio per compilare il progetto.
    > [!Note]  
    > In Windows Vista e versioni successive il progetto non viene compilato correttamente a meno che non si esegua Visual Studio con un token di accesso amministratore completo. Fare clic con il pulsante destro del mouse sul nome o sull'icona di Visual Studio e scegliere **Esegui come amministratore**.

     

Prima di provare a compilare il progetto, assicurarsi di configurare l'ambiente di sviluppo in modo che punti alle cartelle denominate include e lib in cui è stato installato il Windows SDK. Il compilatore e il linker dovranno accedere ad alcuni file in queste cartelle.

Se è stata eseguita l'utilità di registrazione di Visual Studio fornita con la Windows SDK, è probabile che l'ambiente di sviluppo sia già stato configurato in modo da puntare al Windows SDK includere le cartelle e lib. In caso contrario, è necessario configurare manualmente l'ambiente di sviluppo.

Per configurare manualmente Visual Studio, seguire questa procedura.

1.  Scegliere **Opzioni** dal menu **Strumenti**.
2.  Fare clic su **progetti e soluzioni** e quindi su **directory di VC + +**.
3.  In **Mostra directory per** fare clic su **Includi file** o **file di libreria**.
4.  Aggiungere le directory per i file necessari.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di un plug-in](building-a-plug-in.md)
</dt> </dl>

 

 




