---
description: È necessario creare inizialmente un oggetto Installer per caricare il supporto di automazione necessario per accedere ai componenti del programma di installazione tramite COM.
ms.assetid: 113ed443-a866-43d4-86bd-fc3b244f2edb
title: Informazioni sull'interfaccia di automazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c51469240ad684d6fd32ffbc5466007e73f4e4ff7a870b6878b18f25f54d32c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118382068"
---
# <a name="about-the-automation-interface"></a>Informazioni sull'interfaccia di automazione

È [**necessario creare inizialmente**](installer-object.md) un oggetto Installer per caricare il supporto di automazione necessario per accedere ai componenti del programma di installazione tramite COM. Questo oggetto fornisce wrapper per creare gli oggetti di primo livello e accedere ai relativi metodi. Questi wrapper forniscono semplicemente traduzioni dei parametri per esporre le funzioni del programma di installazione in modo coerente con Microsoft Visual Basic senza modificare il comportamento dei metodi.

Quando possibile, una coppia di metodi Get e Set C++ viene esposta Visual Basic come singola proprietà. In alcuni casi i metodi C++ che prendono un argomento di indice vengono esposti come proprietà indicizzata. Molti metodi C++ restituiscono il risultato tramite un parametro perché il valore restituito viene usato per la restituzione dell'errore. Tuttavia, in Visual Basic, gli errori vengono gestiti da un meccanismo separato e il risultato viene sempre passato nel valore restituito.

Per informazioni sull'uso dell'automazione e sulla creazione dell'oggetto Installer, vedere [Uso dell'interfaccia di automazione.](using-the-automation-interface.md)

Per materiale di riferimento per gli oggetti Windows Installer, vedere Informazioni [di riferimento sull'interfaccia di automazione.](automation-interface-reference.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Esempi di script del programma di installazione](windows-installer-scripting-examples.md)
</dt> </dl>

 

 



