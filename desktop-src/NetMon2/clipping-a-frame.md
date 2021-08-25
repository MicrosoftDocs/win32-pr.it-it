---
description: È possibile specificare che il driver ritaglia i fotogrammi.
ms.assetid: a4f53568-684b-48cf-835b-915cefb45a5d
title: Ritaglio di un frame
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9251fc6f8a1c9612a9fa7301ea8948956291ad0d074f90ff2ccbbf3f799bd2b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911261"
---
# <a name="clipping-a-frame"></a>Ritaglio di un frame

È possibile specificare che il driver ritaglia i fotogrammi. Se le altre sezioni del filtro di acquisizione vengono omesse, questa potrebbe essere l'unica funzione del filtro di acquisizione. Se il **campo nFrameBytesToCopy** è diverso da zero (0), il relativo valore specifica il numero di byte di ogni frame ricevuto da mantenere. Se il campo è zero, viene mantenuto l'intero frame.

> [!Note]  
> È possibile ritagliare qualsiasi fotogramma che passa le altre parti del filtro di acquisizione impostando **nFrameBytesToCopy**.

 

 

 



