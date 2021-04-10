---
description: Inizialmente è necessario creare un oggetto del programma di installazione per caricare il supporto di automazione necessario per accedere ai componenti del programma di installazione tramite COM.
ms.assetid: 113ed443-a866-43d4-86bd-fc3b244f2edb
title: Informazioni sull'interfaccia di automazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 655a01a4daccb805bec4a858337c1dce48f0fb82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227226"
---
# <a name="about-the-automation-interface"></a>Informazioni sull'interfaccia di automazione

Inizialmente è necessario creare un [**oggetto del programma di installazione**](installer-object.md) per caricare il supporto di automazione necessario per accedere ai componenti del programma di installazione tramite com. Questo oggetto fornisce i wrapper per creare gli oggetti di primo livello e accedere ai relativi metodi. Questi wrapper forniscono semplicemente le traduzioni di parametri per esporre le funzioni del programma di installazione in modo coerente con Microsoft Visual Basic senza modificare il comportamento dei metodi.

Quando possibile, una coppia di metodi get e set C++ vengono esposti per Visual Basic come una singola proprietà. In alcuni casi, i metodi C++ che accettano un argomento di indice vengono esposti come proprietà indicizzata. Molti metodi C++ restituiscono il risultato tramite un parametro poiché il valore restituito viene usato per la restituzione dell'errore. Tuttavia, in Visual Basic, gli errori vengono gestiti da un meccanismo separato e il risultato viene sempre passato nel valore restituito.

Per informazioni sull'uso dell'automazione e sulla creazione dell'oggetto del programma di installazione, vedere [uso dell'interfaccia di automazione](using-the-automation-interface.md).

Per materiale di riferimento per gli oggetti Windows Installer, vedere informazioni di [riferimento sull'interfaccia di automazione](automation-interface-reference.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di script di Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 



