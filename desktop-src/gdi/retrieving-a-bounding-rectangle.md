---
description: Un'applicazione recupera le dimensioni del rettangolo di delimitazione di un'area chiamando la funzione GetRgnBox.
ms.assetid: 3851d0f4-33ec-44db-9cb8-c2afb03ffc25
title: Recupero di un rettangolo di delimitazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b214a3f2e8d4fcd81e7f03ecf6dddc72442e209b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754306"
---
# <a name="retrieving-a-bounding-rectangle"></a>Recupero di un rettangolo di delimitazione

Un'applicazione recupera le dimensioni del rettangolo di delimitazione di un'area chiamando la funzione [**GetRgnBox**](/windows/desktop/api/Wingdi/nf-wingdi-getrgnbox) . Se l'area è rettangolare, **GetRgnBox** restituisce le dimensioni dell'area. Se l'area è ellittica, la funzione restituisce le dimensioni del rettangolo più piccolo che può essere tracciato intorno all'ellisse. I lati lunghi del rettangolo hanno la stessa lunghezza dell'asse principale dell'ellisse e i lati corti del rettangolo hanno la stessa lunghezza dell'asse secondario dell'ellisse. Se l'area è poligonale, **GetRgnBox** restituisce le dimensioni del rettangolo più piccolo che può essere tracciato intorno all'intero poligono.

 

 



