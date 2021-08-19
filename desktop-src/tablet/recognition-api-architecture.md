---
description: Un'applicazione abilitata per l'input penna comunica con il sistema di riconoscimento tramite le API della piattaforma Tablet PC.
ms.assetid: 0ea6881f-d2d7-4646-9c41-53d1c03ea55b
title: Architettura dell'API Di riconoscimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59775658bcda2ecafd142476e6ff48ccdda2e82b31af62d5f49b218513f9b326
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966895"
---
# <a name="recognition-api-architecture"></a>Architettura dell'API Di riconoscimento

Un'applicazione abilitata per l'input penna comunica con il sistema di riconoscimento tramite le API della piattaforma Tablet PC. A tale [**scopo, le applicazioni usano l'oggetto IInkRecognizer.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) La piattaforma Tablet PC interagisce con il sistema di riconoscimento usando le interfacce di tipo C documentate in questa sezione. Nella figura seguente l'area all'interno della linea tratteggiata mostra quanto documentato in questa sezione.

![illustrazione dell'architettura di riconoscimento con il riconoscimento evidenziato](images/96ee7367-7b8a-4794-99c1-bcac9daed645.gif)

Un sistema di riconoscimento personalizzato deve includere Recapis.h (installato per impostazione predefinita in C: \\ Programmi Microsoft Tablet PC Platform SDK \\ \\ Include). Tranne dove specificato, la libreria a collegamento dinamico (DLL) deve esportare tutte le funzioni API, anche se si sceglie di fare in modo che alcune restituiranno E \_ NOTIMPL.

In nessuna circostanza il sistema di riconoscimento verrà chiamato direttamente da un'applicazione abilitata per l'input penna. Al contrario, le applicazioni chiameranno le API di Automazione o le API gestite per ottenere risultati dal sistema di riconoscimento.

 

 



