---
description: Il tipo di dati AnyPath è una stringa di testo contenente un percorso completo o relativo.
ms.assetid: fe8a4d2a-1960-40af-a0e4-4d65accdd388
title: AnyPath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ab6265874616bb0bb1a2f61098cdbabfa8ea24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311059"
---
# <a name="anypath"></a>AnyPath

Il tipo di dati AnyPath è una stringa di testo contenente un percorso completo o relativo. Quando si specifica un percorso relativo, è possibile includere un nome di file lungo con il nome di file breve separando i nomi brevi e lunghi con una barra verticale ( \| ). Si noti che in questo modo non è possibile specificare più livelli di una directory o percorsi completi. Il percorso può contenere proprietà racchiuse tra parentesi quadre ( \[ \] ).

Esempi di dati AnyPath validi:

-   \\\\\\temporanea condivisione \\ Server
-   c: \\ Temp
-   \\Temp
-   Stato progetto Project ~ 1 \|

Esempi di dati AnyPath non validi:

-   c: \\ temp \\ Project ~ 1 \| c: \\ stato del \\ progetto Temp One
-   \\\\ \| \\ stato di un \\ progetto Temp Project ~ 1

 

 



