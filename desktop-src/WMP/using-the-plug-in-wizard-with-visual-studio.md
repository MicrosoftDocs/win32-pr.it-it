---
title: Uso della Creazione guidata plug-in con Visual Studio
description: Uso della Creazione guidata plug-in con Visual Studio
ms.assetid: 5d5521b7-5cbc-4259-92b1-a7250853fa2e
keywords:
- Windows Media Player plug-in, Visual Studio
- plug-in, Visual Studio
- compilazione di plug-in, Visual Studio
- Windows Media Player Creazione guidata plug-in, Visual Studio
- Visual Studio,Windows Media Player creazione guidata plug-in
- Procedura guidata plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1534d084d2c57d3546427db59274d1bd135bc66e8bf396906ff7776cae9a370f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134334"
---
# <a name="using-the-plug-in-wizard-with-visual-studio"></a>Uso della Creazione guidata plug-in con Visual Studio

Dopo aver installato i componenti necessari, è possibile creare rapidamente un plug-in che fungerà da punto di partenza. Verrà illustrata la procedura seguente.

1.  Avviare Microsoft Visual Studio.
2.  Scegliere **Nuovo** dal menu File **e quindi** fare clic su **Project**.
3.  In **Project tipi** selezionare **Visual C++ progetti**.
4.  In **Modelli** selezionare Windows Media Player **creazione guidata plug-in.**
5.  Immettere un nome per il progetto.
6.  Immettere un percorso per il progetto. Si tratta della cartella in cui verranno copiati i file di progetto.
7.  Fare **clic su OK** per avviare la procedura guidata.
8.  Selezionare il tipo di plug-in che si vuole creare.
9.  Completare tutte le finestre di dialogo rimanenti della procedura guidata.
10. Usare l Visual Studio di sviluppo per compilare il progetto.
    > [!Note]  
    > In Windows Vista e versioni successive, il progetto verrà compilato correttamente solo se si esegue Visual Studio con un token di accesso amministratore completo. Fare clic con il pulsante destro Visual Studio nome o sull'icona e scegliere **Esegui come amministratore.**

     

Prima di provare a compilare il progetto, assicurarsi di configurare l'ambiente di sviluppo in modo che punti alle cartelle denominate Include e Lib in cui è stato installato Windows SDK. Il compilatore e il linker dovranno accedere ad alcuni dei file in queste cartelle.

Se è stata eseguita l'utilità Visual Studio Registration fornita con Windows SDK, è probabile che l'ambiente di sviluppo sia già stato configurato in modo da puntare alle cartelle Include e Lib di Windows SDK. In caso contrario, è necessario configurare manualmente l'ambiente di sviluppo.

Per configurare manualmente Visual Studio, seguire questa procedura.

1.  Scegliere **Opzioni** dal menu **Strumenti**.
2.  Fare **clic su Progetti e soluzioni** e quindi su VC++ **directory**.
3.  In **Mostra directory per fare** clic su Includi file **o** File **di libreria**.
4.  Aggiungere le directory per i file necessari.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Compilazione di un plug-in](building-a-plug-in.md)
</dt> </dl>

 

 




