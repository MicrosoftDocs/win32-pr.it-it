---
description: L'attributo pattern specifica il modello di una penna geometrica.
ms.assetid: 5a330416-3b83-4f0f-825c-80e47903966e
title: Modello di penna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 577b5e2cb31e44a4631760c82e678af069322cbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528297"
---
# <a name="pen-pattern"></a>Modello di penna

L'attributo pattern specifica il modello di una penna geometrica.

Nella figura seguente sono illustrate le linee disegnate con diverse penne geometriche. Ogni penna è stata creata usando un attributo del criterio diverso.

![illustrazione che mostra quattro righe, ognuna con una penna diversa](images/cspen-02.png)

La prima riga della figura precedente viene disegnata utilizzando uno dei sei modelli di tratteggio disponibili. Per ulteriori informazioni sui modelli di tratteggio, vedere [Pen Hatch](pen-hatch.md). La riga successiva viene disegnata usando il modello vuoto, identica al modello null. La terza riga viene disegnata usando un modello personalizzato creato da una bitmap da 8 a 8 pixel. Per ulteriori informazioni sulle bitmap e sulla relativa creazione, vedere [bitmap](bitmaps.md). L'ultima riga viene disegnata usando un modello a tinta unita. La creazione di un pennello e il passaggio del relativo handle alla funzione [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) creano un modello.

 

 



