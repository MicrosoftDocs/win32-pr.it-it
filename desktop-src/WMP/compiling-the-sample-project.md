---
title: Compilazione del progetto di esempio
description: Compilazione del progetto di esempio
ms.assetid: c605042e-ec45-44c7-afca-42a874882eab
keywords:
- Windows Media Player Online Stores, compilazione di progetti di esempio
- negozi online, compilazione di progetti di esempio
- digitare 2 archivi online, compilazione di progetti di esempio
- Windows Media Player Online Stores, progetti di esempio
- negozi online, progetti di esempio
- digitare 2 archivi online, progetti di esempio
- Windows Media Player Online Stores, creazione guidata progetto
- negozi online, creazione guidata progetto
- digitare 2 archivi online, creazione guidata progetto
- plug-in, creazione guidata progetto
- Plug-in di Windows Media Player, creazione guidata progetto
- compilazione di progetti di esempio
- esempi, digitare 2 archivi online
- Creazione guidata progetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1ea2382e5852965b246f1ef303e5e70d160cb22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298472"
---
# <a name="compiling-the-sample-project"></a>Compilazione del progetto di esempio

La procedura guidata genera tutti i file necessari per compilare il progetto di esempio, pertanto non è necessario modificare le impostazioni predefinite del progetto. In Visual Studio scegliere **Compila soluzione** dal menu **Compila** per compilare e registrare il componente com. Per impostazione predefinita, la configurazione di debug è attiva.

> [!Note]  
> In Windows Vista e versioni successive il progetto non viene compilato correttamente a meno che non si esegua Visual Studio con un token di accesso amministratore completo. Fare clic con il pulsante destro del mouse sul nome o sull'icona di Visual Studio e scegliere **Esegui come amministratore**.

 

Prima di provare a compilare il progetto, assicurarsi di configurare l'ambiente di sviluppo in modo che punti alle cartelle denominate include e lib in cui è stato installato il Windows SDK. Il compilatore e il linker dovranno accedere ad alcuni file in queste cartelle.

Se è stata eseguita l'utilità di registrazione di Visual Studio fornita con Windows Vista SDK, è probabile che l'ambiente di sviluppo sia già stato configurato in modo da puntare all'Windows SDK includere le cartelle e lib. In caso contrario, è necessario configurare manualmente l'ambiente di sviluppo.

Per configurare manualmente Visual Studio, seguire questa procedura.

1.  Scegliere **Opzioni** dal menu **Strumenti**.
2.  Fare clic su **progetti e soluzioni** e quindi su **directory di VC + +**.
3.  In **Mostra directory per** fare clic su **Includi file** o **file di libreria**.
4.  Aggiungere le directory per i file necessari.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione del plug-in per un negozio online di tipo 2](building-the-plug-in-for-a-type-2-online-store.md)
</dt> </dl>

 

 




