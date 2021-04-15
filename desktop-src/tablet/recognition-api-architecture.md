---
description: Un'applicazione abilitata per l'input penna comunica con il sistema di riconoscimento tramite le API della piattaforma Tablet PC.
ms.assetid: 0ea6881f-d2d7-4646-9c41-53d1c03ea55b
title: Architettura dell'API di riconoscimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72838b77e11092cacd4adb998c669167940ecad2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104554533"
---
# <a name="recognition-api-architecture"></a>Architettura dell'API di riconoscimento

Un'applicazione abilitata per l'input penna comunica con il sistema di riconoscimento tramite le API della piattaforma Tablet PC. Per eseguire questa operazione, le applicazioni utilizzano l'oggetto [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) . La piattaforma Tablet PC interagisce con il riconoscimento usando le interfacce di tipo C documentate in questa sezione. Nell'illustrazione seguente, l'area all'interno della linea tratteggiata mostra quanto descritto in questa sezione.

![illustrazione dell'architettura di riconoscimento con il riconoscimento evidenziato](images/96ee7367-7b8a-4794-99c1-bcac9daed645.gif)

Un riconoscitore personalizzato deve includere il file recapit. h (installato per impostazione predefinita in C: \\ programmi \\ Microsoft Tablet PC Platform SDK \\ ). Ad eccezione di quanto indicato, la libreria di collegamento dinamico (DLL) deve esportare tutte le funzioni API, anche se si sceglie di fare in modo che vengano restituite E \_ NOTIMPL.

In nessuna circostanza il riconoscimento verrà chiamato direttamente da un'applicazione abilitata per l'input penna. Al contrario, le applicazioni chiamano le API di automazione o le API gestite per ottenere risultati dal riconoscimento.

 

 



