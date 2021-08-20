---
title: Uso della Creazione guidata plug-in di Online Store con Visual Studio
description: Uso della Creazione guidata plug-in di Online Store con Visual Studio
ms.assetid: 0bf670cd-897d-4cd6-ae95-ae16b2dacc96
keywords:
- Windows Media Player negozi online, plug-in
- negozi online, plug-in
- tipo 1 negozi online, plug-in
- Windows Media Player negozi online, creazione guidata plug-in
- negozi online, creazione guidata plug-in
- tipo 1 negozi online, procedura guidata plug-in
- Windows Media Player negozi online, Visual Studio
- negozi online, Visual Studio
- Tipo 1 di negozi online, Visual Studio
- plug-in, Windows Media Player online store
- plug-in, negozi online
- plug-in, tipo 1 negozi online
- plug-in, Visual Studio
- plug-in, creazione guidata plug-in
- Windows Media Player plug-in, tipo 1 negozi online
- Windows Media Player plug-in, negozi online
- Windows Media Player plug-in, Windows Media Player online store
- Windows Media Player plug-in, Visual Studio
- Windows Media Player plug-in, procedura guidata plug-in
- Visual Studio,Windows Media Player Online Stores Wizard
- Creazione guidata plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd53a1b83f817e4cfcc7dede80361f56f46ea41da8730f4396330c12af05c73a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118830682"
---
# <a name="using-the-online-store-plug-in-wizard-with-visual-studio"></a>Uso della Creazione guidata plug-in di Online Store con Visual Studio

Dopo aver installato i componenti necessari, è possibile creare rapidamente un plug-in che fungerà da punto di partenza. La procedura seguente ti guiderà:

1.  Avviare Microsoft Visual Studio.
2.  Scegliere **Nuovo** dal menu File e **quindi** fare clic **su Project**.
3.  In **Project tipi fare** clic su Visual C++ **Progetti**.
4.  In **Modelli** fare clic su **Windows Media Player Guidata negozi online**.
5.  Immettere un nome per il progetto.
6.  Immettere un percorso per il progetto. Si tratta della cartella in cui verranno copiati i file di progetto.
7.  Fare **clic su OK** per avviare la procedura guidata.
8.  Selezionare **Tipo 1 (integrazione completa)** e fare clic su **Avanti.**
9.  Immettere un nome descrittivo e un distributore di contenuti. Fare clic su **Fine**.
10. Usare l'Visual Studio di sviluppo per compilare il progetto.
    > [!Note]  
    > In Windows Vista e versioni successive, il progetto non verrà compilato correttamente a meno che non si ese Visual Studio con un token di accesso amministratore completo. Fare clic con il pulsante destro Visual Studio nome o sull'icona e scegliere **Esegui come amministratore**.

     

Prima di provare a compilare il progetto, assicurarsi di configurare l'ambiente di sviluppo in modo che punti alle cartelle denominate Include e Lib in cui è stato installato Windows SDK. Il compilatore e il linker dovranno accedere ad alcuni dei file in queste cartelle.

Se è stata eseguita l'utilità Visual Studio Registration fornita con Windows SDK, è probabile che l'ambiente di sviluppo sia già stato configurato per puntare alle cartelle include e lib di Windows SDK. In caso contrario, è necessario configurare manualmente l'ambiente di sviluppo.

Per configurare manualmente Visual Studio, seguire questa procedura.

1.  Scegliere **Opzioni** dal menu Strumenti.
2.  Fare **clic su Progetti e soluzioni** e quindi su VC++ **directory**.
3.  In **Mostra directory per** fare clic su Includi **file** o File **di libreria**.
4.  Aggiungere le directory per i file necessari.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Compilazione del plug-in per uno Store online di tipo 1](building-the-plug-in-for-a-type-1-online-store.md)
</dt> </dl>

 

 




