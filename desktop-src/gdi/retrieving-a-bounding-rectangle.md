---
description: Un'applicazione recupera le dimensioni del rettangolo di delimitazione di un'area chiamando la funzione GetRgnBox.
ms.assetid: 3851d0f4-33ec-44db-9cb8-c2afb03ffc25
title: Recupero di un rettangolo di delimitazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9b7182d7c8f48fa8629855849710a601db9f93fd7e9180f9024d798b5ce2ebe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117886148"
---
# <a name="retrieving-a-bounding-rectangle"></a>Recupero di un rettangolo di delimitazione

Un'applicazione recupera le dimensioni del rettangolo di delimitazione di un'area chiamando la [**funzione GetRgnBox.**](/windows/desktop/api/Wingdi/nf-wingdi-getrgnbox) Se l'area è rettangolare, **GetRgnBox** restituisce le dimensioni dell'area. Se l'area è ellittica, la funzione restituisce le dimensioni del rettangolo più piccolo che può essere disegnato intorno all'ellisse. I lati lunghi del rettangolo hanno la stessa lunghezza dell'asse principale dell'ellisse e i lati brevi del rettangolo hanno la stessa lunghezza dell'asse secondario dell'ellisse. Se l'area è poligonale, **GetRgnBox** restituisce le dimensioni del rettangolo più piccolo che può essere disegnato intorno all'intero poligono.

 

 



