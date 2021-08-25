---
title: Preparare l'ambiente di sviluppo
description: Preparare l'ambiente di sviluppo
ms.assetid: 5a3fd27e-ec8f-41eb-9d31-86d6d9f70862
ms.topic: article
ms.date: 10/03/2019
ms.openlocfilehash: 8245326ba0d7862836336cf050eb3abf1873139873bde8b9bab238ff5a738942
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896971"
---
# <a name="prepare-your-development-environment"></a>Preparare l'ambiente di sviluppo

Per scrivere un programma Windows in C o C++, è necessario installare Microsoft Windows Software Development Kit (SDK) o Microsoft Visual Studio. L Windows SDK contiene le intestazioni e le librerie necessarie per compilare e collegare l'applicazione. L Windows SDK contiene anche strumenti da riga di comando per la compilazione Windows applicazioni, tra cui il compilatore Visual C++ e il linker. Sebbene sia possibile compilare e compilare Windows con gli strumenti da riga di comando, è consigliabile usare Microsoft Visual Studio. È possibile scaricare un download gratuito di Visual Studio Community o versioni di valutazione gratuite di altre versioni di Visual Studio [qui](https://visualstudio.microsoft.com/downloads/).

Ogni versione dell'SDK Windows è destinata alla versione più recente Windows e a diverse versioni precedenti. Le note sulla versione elencano le piattaforme specifiche supportate, ma a meno che non si manteni un'applicazione per una versione molto precedente di Windows, devi installare la versione più recente di Windows SDK. È possibile scaricare la versione più recente Windows SDK [qui.](https://developer.microsoft.com/windows/downloads/windows-10-sdk)

L Windows SDK supporta lo sviluppo di applicazioni a 32 bit e a 64 bit. Le Windows sono progettate in modo che lo stesso codice possa essere compilato per 32 o 64 bit senza modifiche.

> [!Note]  
> L Windows SDK non supporta lo sviluppo di driver hardware e questa serie non descrive lo sviluppo di driver. Per informazioni sulla scrittura di un driver hardware, [vedere Attività iniziali con Windows driver](/windows-hardware/drivers/gettingstarted/).

## <a name="next"></a>Prossima

[Windows Convenzioni di codifica](windows-coding-conventions.md)

## <a name="related-topics"></a>Argomenti correlati

* [Download di Visual Studio](https://visualstudio.microsoft.com/downloads/)
* [Scaricare Windows SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk)