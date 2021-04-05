---
title: Indicatori di tipo
description: Le proprietà effettive seguono la tabella dei valori del set di proprietà coppie di identificatori di proprietà/offset. Ogni proprietà viene archiviata come DWORD, seguita dal valore del tipo di dati.
ms.assetid: 8523458b-8b1b-4e9f-8f96-d7601e57675c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8383a860f07e908b72a7b25091f3cc2e280e4407
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047105"
---
# <a name="type-indicators"></a>Indicatori di tipo

Le proprietà effettive seguono la tabella dei valori del set di proprietà coppie di identificatori di proprietà/offset. Ogni proprietà viene archiviata come **DWORD**, seguita dal valore del tipo di dati.

Gli indicatori di tipo e i relativi valori associati sono descritti nella struttura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .

Tutte le coppie tipo/valore devono iniziare con un limite di 32 bit. Pertanto, i valori possono essere seguiti con byte null per allineare la coppia successiva in un limite di 32 bit.

Il codice di esempio seguente calcola il numero di byte necessari per l'allineamento su un limite a 32 bit, dato un conteggio di byte.


```C++
cbAdd = (((cbCurrent + 3) >> 2) << 2) - cbCurrent ;
```



All'interno di un vettore di valori, ogni ripetizione di un valore scalare semplice inferiore a 32 bit deve essere allineata con il relativo allineamento naturale anziché con un allineamento a 32 bit. In pratica, questa operazione è significativa solo per i tipi **VT \_ Ui1**, **VT \_ UI2**, **VT \_ I2** e **VT \_ bool** (che hanno un allineamento naturale a un byte o a due byte). Tutti gli altri tipi hanno un allineamento naturale a quattro byte. Alcuni tipi, ad esempio, **VT \_ R8**, hanno effettivamente un allineamento naturale a 8 byte, ma vengono archiviati come se avessero un allineamento a quattro byte.

Un valore della proprietà con l'indicatore di tipo **VT \_ I2** \| **VT \_ vector** include:

-   Conteggio di elementi **DWORD** .
-   Sequenza di interi a due byte compressi senza spaziatura interna null.

> [!IMPORTANT]
> Tutti i conteggi a 32 bit o i tipi di proprietà archiviati come parte di un elemento della proprietà Vector devono anche essere allineati a 32 bit.

 

Il valore della proprietà dell'identificatore di tipo **VT \_ LPSTR** \| **VT \_ vector** include:

-   Un conteggio di elementi **DWORD** (**DWORD** *cElems*).
-   Sequenza di stringhe (**char** *rgch \[ \]*), ognuna preceduta da un **valore DWORD** di lunghezza e possibilmente seguito da una spaziatura interna null per arrotondare a un limite di 32 bit.

 

 