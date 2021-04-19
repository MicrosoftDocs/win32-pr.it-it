---
description: È possibile specificare che il driver Ritaglia i frame.
ms.assetid: a4f53568-684b-48cf-835b-915cefb45a5d
title: Ritaglio di un frame
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1507b82ffedeb26939d5d954f116bb009ed0ab41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311631"
---
# <a name="clipping-a-frame"></a>Ritaglio di un frame

È possibile specificare che il driver Ritaglia i frame. Se le altre sezioni del filtro di acquisizione vengono omesse, può trattarsi dell'unica funzione del filtro di acquisizione. Se il campo **nFrameBytesToCopy** è diverso da zero (0), il relativo valore specifica il numero di byte di ogni frame ricevuti da mantenere. Se il campo è zero, viene mantenuto il frame intero.

> [!Note]  
> È possibile ritagliare tutti i frame che passano le altre parti del filtro di acquisizione impostando **nFrameBytesToCopy**.

 

 

 



