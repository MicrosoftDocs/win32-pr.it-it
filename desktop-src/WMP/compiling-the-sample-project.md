---
title: Compilazione dell'esempio Project
description: Compilazione dell'esempio Project
ms.assetid: c605042e-ec45-44c7-afca-42a874882eab
keywords:
- Windows Media Player online store, compilazione di progetti di esempio
- online store, compilazione di progetti di esempio
- store online di tipo 2, compilazione di progetti di esempio
- Windows Media Player online, progetti di esempio
- negozi online, progetti di esempio
- store online di tipo 2, progetti di esempio
- Windows Media Player online, creazione guidata progetto
- online stores, creazione guidata progetto
- tipo 2 negozi online, creazione guidata progetto
- plug-in, creazione guidata progetto
- Windows Media Player plug-in, Creazione guidata progetto
- compilazione di progetti di esempio
- esempi, tipo 2 negozi online
- Creazione guidata progetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55b2f5a4b6d29b227b08654cfcde2a89cc97b224fc756251ae9554f029f22416
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763941"
---
# <a name="compiling-the-sample-project"></a>Compilazione dell'esempio Project

La procedura guidata genera tutti i file necessari per compilare il progetto di esempio, quindi non è necessario modificare le impostazioni predefinite del progetto. Nel Visual Studio scegliere Compila **soluzione** dal  menu Compila per compilare e registrare il componente COM. Per impostazione predefinita, la configurazione debug è attiva.

> [!Note]  
> In Windows Vista e versioni successive, il progetto verrà compilato correttamente solo se si esegue Visual Studio con un token di accesso amministratore completo. Fare clic con il pulsante destro del Visual Studio nome o sull'icona e scegliere **Esegui come amministratore.**

 

Prima di provare a compilare il progetto, assicurarsi di configurare l'ambiente di sviluppo in modo che punti alle cartelle denominate Include e Lib in cui è stato installato Windows SDK. Il compilatore e il linker dovranno accedere ad alcuni dei file in queste cartelle.

Se è stata eseguita l'utilità Visual Studio Registration fornita con Windows Vista SDK, è probabile che l'ambiente di sviluppo sia già stato configurato in modo da puntare alle cartelle Include e Lib di Windows SDK. In caso contrario, è necessario configurare manualmente l'ambiente di sviluppo.

Per configurare manualmente Visual Studio, seguire questa procedura.

1.  Scegliere **Opzioni** dal menu **Strumenti**.
2.  Fare **clic su Progetti e soluzioni** e quindi su VC++ **directory**.
3.  In **Mostra directory per fare** clic su Includi file **o** File **di libreria**.
4.  Aggiungere le directory per i file necessari.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione del plug-in per uno store online di tipo 2](building-the-plug-in-for-a-type-2-online-store.md)
</dt> </dl>

 

 




