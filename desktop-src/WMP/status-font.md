---
title: Carattere stato
description: Carattere stato
ms.assetid: eba697e8-8be5-4692-b7b2-a52c5642022a
keywords:
- Interfacce di Windows Media Player Mobile, visualizzazione dello stato
- interfacce, visualizzazione stato
- informazioni di riferimento per Skins, status display
- visualizzazione dello stato in interfacce, tipi di carattere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5a773f3baaeda0eaa90dfe0702957b5b7888271
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955745"
---
# <a name="status-font"></a>Carattere stato

È necessario definire il tipo di carattere utilizzato dalla visualizzazione di stato che si desidera utilizzare. Il tipo di carattere è definito da tre valori, separati da virgole, che rappresentano la superficie, le dimensioni e il peso del tipo di carattere.

**Valori tipografici**

È possibile utilizzare qualsiasi nome tipografico se è probabile che sia installato nel computer dell'utente. Se un carattere tipografico non viene trovato nel computer, verrà selezionato un alternativo dal sistema operativo. Nella tabella seguente vengono illustrati i caratteri tipografici di solito presenti nei dispositivi basati su Windows Mobile 2003.



| Tipo di carattere       | Descrizione              |
|----------------|--------------------------|
| Tahoma         | Carattere tipografico sans-serif.   |
| Console lucida | Carattere tipografico con Serif quadrato. |



 

**Valori delle dimensioni**

Si tratta della dimensione del carattere tipografico nei punti. Qualsiasi valore intero positivo è valido, ma sono consigliati i numeri compresi tra 10 e 18. Le dimensioni minori di 10 potrebbero essere difficili da leggere e le dimensioni superiori a 18 potrebbero non lasciare spazio sufficiente per la visualizzazione di più lettere alla volta.

**Valori di peso**

Gli unici valori consentiti sono riportati nella tabella seguente.



| Valore | Descrizione |
|-------|-------------|
| B     | Grassetto        |
| N     | Normale      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Stato**](status.md)
</dt> </dl>

 

 




