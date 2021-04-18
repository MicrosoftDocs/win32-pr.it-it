---
title: Uso della procedura guidata plug-in di Store online con Visual Studio
description: Uso della procedura guidata plug-in di Store online con Visual Studio
ms.assetid: 0bf670cd-897d-4cd6-ae95-ae16b2dacc96
keywords:
- Windows Media Player Online Stores, plug-in
- archivi online, plug-in
- digitare 1 negozi online, plug-in
- Windows Media Player Online Stores, creazione guidata plug-in
- negozi online, creazione guidata plug-in
- digitare 1 archivi online, creazione guidata plug-in
- Windows Media Player Online Stores, Visual Studio
- negozi online, Visual Studio
- digitare 1 negozi online, Visual Studio
- plug-in, archivi Windows Media Player online
- plug-in, archivi online
- plug-in, digitare 1 negozi online
- plug-in, Visual Studio
- plug-in, creazione guidata plug-in
- Plug-in di Windows Media Player, digitare 1 negozi online
- Plug-in di Windows Media Player, archivi online
- Plug-in di Windows Media Player, archivi Windows Media Player online
- Plug-in di Windows Media Player, Visual Studio
- Plug-in di Windows Media Player, creazione guidata plug-in
- Visual Studio, procedura guidata per gli archivi online di Windows Media Player
- procedura guidata plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0c9aadbb9cef4b44cb421bf8a4737cc408c5220
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297793"
---
# <a name="using-the-online-store-plug-in-wizard-with-visual-studio"></a>Uso della procedura guidata plug-in di Store online con Visual Studio

Dopo aver installato i componenti necessari, è possibile creare rapidamente un plug-in che funge da punto di partenza. La procedura seguente consentirà di:

1.  Avviare Microsoft Visual Studio.
2.  Scegliere **nuovo** dal menu **file** , quindi fare clic su **progetto**.
3.  In **Tipi progetto** fare clic su **progetti Visual C++**.
4.  In **modelli** fare clic su **creazione guidata di Windows Media Player Online Stores**.
5.  Immettere un nome per il progetto.
6.  Immettere un percorso per il progetto. Si tratta della cartella in cui verranno copiati i file di progetto.
7.  Fare clic su **OK** per avviare la procedura guidata.
8.  Selezionare il **tipo 1 (integrazione completa)** e fare clic su **Avanti**.
9.  Immettere un nome descrittivo e un server di distribuzione del contenuto. Fare clic su **Fine**.
10. Usare l'ambiente di sviluppo di Visual Studio per compilare il progetto.
    > [!Note]  
    > In Windows Vista e versioni successive il progetto non viene compilato correttamente a meno che non si esegua Visual Studio con un token di accesso amministratore completo. Fare clic con il pulsante destro del mouse sul nome o sull'icona di Visual Studio e scegliere **Esegui come amministratore**.

     

Prima di provare a compilare il progetto, assicurarsi di configurare l'ambiente di sviluppo in modo che punti alle cartelle denominate include e lib in cui è stato installato il Windows SDK. Il compilatore e il linker dovranno accedere ad alcuni file in queste cartelle.

Se è stata eseguita l'utilità di registrazione di Visual Studio fornita con la Windows SDK, è probabile che l'ambiente di sviluppo sia già stato configurato in modo da puntare al Windows SDK includere le cartelle e lib. In caso contrario, è necessario configurare manualmente l'ambiente di sviluppo.

Per configurare manualmente Visual Studio, seguire questa procedura.

1.  Scegliere Opzioni dal menu **strumenti** .
2.  Fare clic su **progetti e soluzioni** e quindi su **directory di VC + +**.
3.  In **Mostra directory per** fare clic su **Includi file** o **file di libreria**.
4.  Aggiungere le directory per i file necessari.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione del plug-in per un negozio online di tipo 1](building-the-plug-in-for-a-type-1-online-store.md)
</dt> </dl>

 

 




