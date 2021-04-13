---
title: Preparare l'ambiente di sviluppo
description: Preparare l'ambiente di sviluppo
ms.assetid: 5a3fd27e-ec8f-41eb-9d31-86d6d9f70862
ms.topic: article
ms.date: 10/03/2019
ms.openlocfilehash: ec42509ea81efce4bb17365d3bf08d36c2a4f415
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337206"
---
# <a name="prepare-your-development-environment"></a>Preparare l'ambiente di sviluppo

Per scrivere un programma Windows in C o C++, è necessario installare Microsoft Windows Software Development Kit (SDK) o Microsoft Visual Studio. Il Windows SDK contiene le intestazioni e le librerie necessarie per la compilazione e il collegamento dell'applicazione. Il Windows SDK contiene anche gli strumenti da riga di comando per la compilazione di applicazioni Windows, tra cui il compilatore Visual C++ e il linker. Sebbene sia possibile compilare e compilare programmi Windows con gli strumenti da riga di comando, è consigliabile usare Microsoft Visual Studio. È possibile scaricare gratuitamente una community di [Visual Studio o](https://visualstudio.microsoft.com/downloads/)versioni di valutazione gratuite di altre versioni di Visual Studio.

Ogni versione del Windows SDK è destinata alla versione più recente di Windows e a diverse versioni precedenti. Nelle note sulla versione sono elencate le piattaforme specifiche supportate, ma a meno che non si stia gestendo un'applicazione per una versione molto vecchia di Windows, è necessario installare la versione più recente del Windows SDK. È possibile scaricare la Windows SDK più recente [qui](https://developer.microsoft.com/windows/downloads/windows-10-sdk).

Il Windows SDK supporta lo sviluppo di applicazioni sia a 32 bit che a 64 bit. Le API di Windows sono progettate in modo che lo stesso codice possa essere compilato per 32 bit o 64 bit senza apportare modifiche.

> [!Note]  
> Il Windows SDK non supporta lo sviluppo di driver hardware e in questa serie non verrà illustrato lo sviluppo di driver. Per informazioni sulla scrittura di un driver hardware, vedere [Introduzione con i driver di Windows](/windows-hardware/drivers/gettingstarted/).

## <a name="next"></a>Prossima

[Convenzioni di codifica Windows](windows-coding-conventions.md)

## <a name="related-topics"></a>Argomenti correlati

* [Download di Visual Studio](https://visualstudio.microsoft.com/downloads/)
* [Scarica Windows SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk)